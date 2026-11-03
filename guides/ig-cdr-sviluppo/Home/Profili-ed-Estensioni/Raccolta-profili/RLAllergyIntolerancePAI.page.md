# RLAllergyIntolerancePAI

- [RLAllergyIntolerancePAI](#RLAllergyIntolerancePAI)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLAllergyIntolerancePAI è stato strutturato a partire dalla risorsa generica FHIR [AllergyIntolerance](http://hl7.org/fhir/R4/allergyintolerance.html) per rappresentare le allergie del paziente nel contesto del Piano Assistenziale Individuale (PAI) – Regione Lombardia.

Per ciascuna allergia è prevista una risorsa AllergyIntolerance, referenziata dalla sezione Allergie della Composition. La descrizione dell'allergia è riportata in testo libero in `code.text`; lo stato clinico è sempre `active`.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntolerancePAI}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntolerancePAI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntolerancePAI, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntolerancePAI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntolerancePAI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntolerancePAI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntolerancePAI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
Allergia del paziente: {{link:AllergyIntolerance/Example-AllergyIntolerance-1-PAI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLAllergyIntolerancePAI:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| clinicalStatus | Stato clinico dell'allergia (valore fisso: active) | La codifica è definita dal ValueSet [AllergyIntoleranceClinicalStatusCodes](https://www.hl7.org/fhir/R4/valueset-allergyintolerance-clinical.html) |