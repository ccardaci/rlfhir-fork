---
name: excel-yellow-changes
description: "Apply changes marked by yellow-highlighted cells in an Excel workbook to this Regione Lombardia FHIR project. Use when the user provides an .xlsx file containing requested updates, especially changes to StructureDefinition, CodeSystem, ValueSet, examples, or other JSON artifacts."
argument-hint: "Path to the Excel workbook and, if known, the target FHIR area or profile"
user-invocable: true
---

# Excel Yellow Changes

Apply only the changes represented by yellow-highlighted Excel cells to the FHIR project, preserving unrelated content and producing an auditable result.

When no workbook path is provided, look first in `.github/DaProcessare/ModificheProfili/`. This skill is for profile and other FHIR artifact changes; guide-page changes belong in `.github/DaProcessare/ModificheIG/` and use `word-highlighted-changes`, including when their source is an XLSX workbook. Treat source documents as input only; never modify or delete them. Move or archive processed documents only when the user explicitly requests it.

## Required Inputs

Ask for any missing information before editing:

- The workbook path or attachment.
- If no workbook is attached, inspect `.github/DaProcessare/ModificheProfili/` and report the available supported files before selecting one. If there is more than one plausible input, ask the user which document to process.
- Confirmation that the workbook uses explicit columns for target file/profile, JSON path, and changed value. If those columns are absent, ask how the mapping is represented.
- Whether every yellow cell is a requested change, or whether some yellow cells are explanatory/highlighted context.
- Whether any worksheet is highlighted entirely or predominantly in yellow, including a yellow worksheet tab color. Treat such a worksheet as a request to create a new FHIR profile, not as a collection of cell updates.
- The target project area when the workbook does not identify it clearly.
- The interpretation of each blank yellow cell; never apply blank-cell clearing without confirmation for that workbook.
- The expected handling of formulas, merged cells, and comments.
- Whether the user wants preview-only or application of the changes. Default to preview first.

Do not infer a target JSON file from a sheet name alone when more than one file could match. Ask for confirmation or derive the target from an explicit profile/resource identifier in the workbook.

## Procedure

1. Inspect the workbook structure before changing project files.
   - Enumerate worksheets, used ranges, hidden sheets, merged cells, formulas, comments, and columns/rows containing yellow cells.
   - Detect yellow using the cell fill's RGB/indexed/theme color and report the detection method. Treat blank yellow cells as pending decisions until the user confirms whether they mean deletion, clearing, or context.
   - Inspect both the worksheet tab color (`tabColor`) and the cell fills. Detect worksheets whose tab is yellow, whose full used range is yellow, or whose clearly intentional worksheet area is highlighted in yellow. Classify each such worksheet as a new-profile request and keep it separate from ordinary cell-level updates.
   - Preserve the cell's displayed value and formula separately; do not silently replace a formula with its cached value.
   - Use a structured Excel reader such as `openpyxl` for `.xlsx`. If the workbook is `.xls`, ask the user to provide `.xlsx` or confirm an available conversion path.

2. Build a change inventory without writing files.
   - For every candidate, record worksheet, cell address, displayed value, source row/column labels, target file, target JSON path, proposed operation (`insert`, `update`, or `delete`), and any ambiguity.
   - Group related cells into one logical change when the sheet uses a row-based record.
   - Read the explicit target file/profile, JSON path, and changed value columns. Resolve their identifiers against the repository before applying anything by searching profile id, canonical URL, resource type, code, path, or filename.
   - Use the surrounding row/column labels and existing target content to determine whether the yellow value is an insertion or an update. Do not assume that a populated target path must be overwritten.
   - For a yellow worksheet representing a new profile, extract the proposed profile name, id, canonical URL, base resource/profile, differential elements, cardinalities, bindings, fixed/pattern values, descriptions, and any other declared metadata. Identify missing mandatory information before drafting files.
   - Mark unsupported, conflicting, duplicate, or ambiguous records as blocked rather than guessing.

3. Confirm the mapping and show a preview.
   - Present a compact table of proposed changes and unresolved items.
   - For JSON changes, show the exact JSON Pointer/path and old/new value when available.
   - For a new profile, show the intended filename, StructureDefinition metadata, baseDefinition, differential, and any related files that would be created.
   - Stop after this preview when the user asks for preview-only, dry-run, review, or approval before applying. Do not write, create, or delete project files in preview-only mode.
   - Ask for confirmation if the workbook contains more than one plausible mapping, an ambiguous insert-versus-update operation, destructive operations, or changes to invariant FHIR fields.

4. Apply the smallest possible edits after confirmation.
   - Keep JSON valid and preserve the repository's existing indentation and ordering as far as practical.
   - Change only fields supported by the workbook mapping. Do not rewrite all JSON files or normalize unrelated formatting.
   - Treat a value such as `DELETE` or an explicitly defined empty value as deletion/clearing only after confirming that convention; otherwise treat it as literal text.
   - Preserve user changes already present in the working tree and stop if the same target path has changed since the preview.

5. Validate the result.
   - Parse every modified JSON file.
   - Check that each requested change is present at the intended path and that no blocked item was applied.
   - Run the repository's available FHIR/package validation command if one is documented or configured. Otherwise report that semantic FHIR validation was not available.
   - Re-scan the workbook inventory and report applied, skipped, blocked, and unchanged items.
   - Show the final diff summary and list modified files.

## Decision Rules

- Yellow fill is a signal to inspect, not permission to guess. Ambiguous mappings must remain unapplied.
- A yellow cell is a requested change, but its context determines whether it is an insertion or an update to an existing target property.
- A yellow cell must never cause a broad replacement of matching text throughout the repository.
- If the context does not clearly distinguish insertion from update, block the item and ask the user before applying it.
- A yellow cell containing a value already present at the target is reported as unchanged.
- Yellow formatting alone never means deletion. Deletion requires explicit strikethrough or a separately confirmed deletion convention.
- Conflicting yellow cells for the same target path are blocked until the user resolves the conflict.
- A worksheet with a yellow tab, or highlighted entirely or predominantly in yellow, represents a new profile request. Do not treat it as a mass update and do not create the profile until the preview has been reviewed and explicitly approved.
- Do not alter canonical URLs, profile ids, resource types, cardinalities, bindings, or fixed values without explicitly calling out the FHIR impact and obtaining confirmation.
- Never edit generated or unrelated files merely because they contain the same text.

## Completion Report

End with:

- Workbook and worksheets inspected.
- Number of yellow cells detected and logical changes derived.
- Applied, unchanged, skipped, and blocked changes.
- Modified project files.
- Validation commands and their results.
- Any assumptions requiring follow-up.