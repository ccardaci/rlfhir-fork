# RLEncounterPAI

- [RLEncounterPAI](#RLEncounterPAI)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLEncounterPAI è stato strutturato a partire dal profilo {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLEncounterCore.page.md}}, a sua volta derivato dalla risorsa generica FHIR [Encounter](http://hl7.org/fhir/R4/encounter.html), per rappresentare la presa in carico del paziente nel contesto del Piano Assistenziale Individuale (PAI) – Regione Lombardia.

Nel documento è presente un'unica risorsa Encounter, referenziata sia dall'header della Composition (`Composition.encounter`) sia dalla sezione Presa in Carico. Il profilo aggiunge la modalità di accesso (`hospitalization.admitSource`) e le patologie della presa in carico (`diagnosis`): Patologia Principale (rank 1), Patologia Secondaria (rank 2) e Patologia Addizionale (rank 3).

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterPAI}}.

<br>
<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Hybrid View')">Hybrid View</button>
  <button class="tablinks" onclick="openTab(event, 'Snapshot View')">Snapshot View</button>
  <button class="tablinks" onclick="openTab(event, 'Differential View')">Differential View</button>
  <button class="tablinks" onclick="openTab(event, 'Table View')">Table View</button>
  <button class="tablinks" onclick="openTab(event, 'XML View')">XML View</button>
  <button class="tablinks" onclick="openTab(event, 'JSON View')">JSON View</button>
  <button class="tablinks" onclick="openTab(event, 'Esempi')">Esempi applicati al profilo</button>
</div>

<div id="Snapshot View" class="tabcontent">
  <h3>Snapshot View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterPAI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterPAI, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterPAI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterPAI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterPAI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterPAI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
Presa in carico del paziente: {{link:Encounter/9f0a1b2c-3d4e-4f5a-8b6c-7d8e9f0a1b2c}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLEncounterPAI:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| hospitalization.admitSource | Modalità di accesso | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.9) |