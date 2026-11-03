---
name: word-highlighted-changes
description: "Apply changes marked in a DOCX document or XLSX workbook to the FHIR guide pages in this repository. Use when highlighted changes target guide pages rather than profiles or extensions."
argument-hint: "Path to the DOCX or XLSX document and, if known, the guide or page set to update"
user-invocable: true
---

# Highlighted Guide Changes

Process a DOCX or XLSX change document and apply only its clearly identified instructions to the guide pages under `guides/`. Use `guides/IG-RL-sviluppo/` by default when the document does not specify another guide set. Never apply this skill to FHIR profiles, extensions, examples, or terminology JSON files.

## Required Inputs

Ask for missing information before editing:

- The DOCX or XLSX path or attachment. If none is provided, inspect `.github/DaProcessare/ModificheIG/` and report available `.docx` and `.xlsx` files. Ask which one to use if there is more than one plausible document.
- The guide set or version to update when the document explicitly targets one. Otherwise use `guides/IG-RL-sviluppo/` and report that default.
- For DOCX, confirm that the context clearly identifies highlighted non-strikethrough text as an insertion or an update. Never remove or replace surrounding unhighlighted content unless the context explicitly identifies the existing text being updated.
- For XLSX, identify how highlighted cells and their row/column context express a guide change. If the workbook does not make the proposed change and its target clear, ask rather than assuming the profile-oriented mapping used by the Excel profile skill.
- Whether comments, tracked changes, unhighlighted text, images, formulas, and formatting-only changes should be considered.
- Whether the user wants preview-only or application. Default to preview-only.

## Procedure

1. Inspect the source document without modifying it.
   - For DOCX:
     - Use a structured DOCX reader such as `python-docx`; inspect the underlying Word XML when needed for text boxes, comments, tracked changes, or highlighting not exposed by the high-level reader.
     - Enumerate paragraphs, tables, headings, lists, headers, footers, comments, and tracked changes that contain highlighted runs.
     - Detect yellow highlighting from the run's highlight property and report the detection method. Do not treat font color, shading, or a yellow page background as equivalent unless the user confirms that convention.
     - Preserve run order and combine adjacent highlighted runs only when they form one contiguous logical change.
     - Record whether every highlighted run is strikethrough. A highlighted and strikethrough run is always a deletion request; a highlighted non-strikethrough run is an insertion or update request that must be resolved from context.
   - For XLSX:
     - Use a structured Excel reader such as `openpyxl`. Enumerate worksheets, used ranges, hidden sheets, merged cells, formulas, comments, and cells with yellow fills.
     - Detect yellow from the cell fill's RGB, indexed, or theme color and report the detection method. A yellow cell is a candidate change, not enough on its own to infer an operation or target.
     - Preserve each cell's value and formula separately. Record worksheet, cell address, displayed value, neighboring row/column labels, and relevant surrounding content.
     - Treat yellow strikethrough text as a deletion candidate and other yellow text as a possible insertion or update, but resolve the operation and target guide passage from context. Do not infer a guide target from a worksheet name alone.
     - Do not apply the profile/new-profile conventions of `excel-yellow-changes` to this guide-focused workbook. `.xls` files require a user-confirmed conversion path or an `.xlsx` copy.

2. Build a change inventory without writing guide files.
   - For every change, record its DOCX location or XLSX worksheet/cell, exact highlighted text, strikethrough state when applicable, surrounding context, proposed operation, target guide path, target heading or anchor, and ambiguity.
   - Resolve target pages only within `guides/**/*.page.md` or other explicitly documented guide-page formats. Search by page title, profile/resource name, heading, canonical guide link, and distinctive surrounding text. Use `guides/IG-RL-sviluppo/` unless the source document specifies another guide set.
   - Prefer an explicit page name or guide link in the source. Do not infer a page solely from a profile name when multiple guide pages match.
   - For deletions, locate the exact target text before proposing removal. If it appears more than once, report all matches and ask which occurrence to remove.
   - For insertions or updates, use the surrounding source context to determine the operation. Preserve existing unhighlighted content unless the context explicitly identifies the text to update. If operation or location cannot be determined unambiguously, mark it blocked and ask rather than guessing.
   - Keep changes to different guide versions separate. Never apply a change to every matching page by default.

3. Show a preview and request approval.
   - Present a compact table with source location (DOCX paragraph/table or XLSX sheet/cell), operation (`delete`, `insert`, or `update`), target page, target anchor, existing context, old text when applicable, and inserted/updated/deleted text.
   - Show the exact Markdown context or diff for every proposed change.
   - List unresolved page mappings, repeated matches, unsupported source-document constructs, and interpretation questions separately.
   - Stop after the preview when the user asks for preview-only, dry-run, review, or approval before applying. Do not write, create, rename, or delete guide files in preview-only mode.

4. Apply approved changes to guide pages.
   - Edit only approved target pages and preserve unrelated Markdown, links, front matter, tables, indentation, and line endings as far as practical.
   - For yellow strikethrough text, remove only the exact approved text and clean up resulting whitespace or empty list/table artifacts without rewriting surrounding prose.
   - For approved insertions or updates, preserve the intended Markdown structure. Update existing text only when that exact text and operation were identified and approved in the preview.
   - Do not modify the source DOCX, profiles, extensions, examples, terminology, or generated artifacts.
   - If the target page changed after preview, stop and regenerate the preview instead of overwriting the newer content.

5. Validate the result.
   - Confirm every approved deletion is absent and every approved insertion is present exactly once at the intended page and anchor.
   - Check that modified Markdown pages remain readable and that front matter, links, tables, and fenced code blocks are not malformed.
   - Run any repository documentation build or link checker that is documented or configured. If none is available, perform targeted structural checks and report that a full documentation build was unavailable.
   - Report applied, unchanged, skipped, and blocked changes, including unsupported source-document constructs.

## Decision Rules

- Yellow highlighting in either format identifies candidate changes; it is not permission to guess the target page or operation.
- In DOCX, yellow plus strikethrough means delete the highlighted text from the approved guide location.
- In XLSX, yellow plus strikethrough is a deletion candidate; locate the exact guide text and include it in the preview before applying.
- Yellow without strikethrough means a contextual insertion or update. It must never replace or delete surrounding unhighlighted text unless the context explicitly identifies the target text and the user approves the operation.
- Unhighlighted source text is context only unless the user explicitly says otherwise.
- Tracked deletions and comments are not applied automatically; include them in the inventory and ask for confirmation.
- Never update profiles or extensions because a guide page mentions them.
- Ambiguous mappings, ambiguous insert-versus-update interpretation, duplicate target text, and conflicting instructions remain blocked until resolved.

## Completion Report

End with:

- Source document inspected, format, and highlighted runs/cells detected.
- Guide set and pages inspected.
- Applied, unchanged, skipped, and blocked changes.
- Exact modified guide pages.
- Validation commands and results.
- Assumptions and unsupported source-document features requiring follow-up.