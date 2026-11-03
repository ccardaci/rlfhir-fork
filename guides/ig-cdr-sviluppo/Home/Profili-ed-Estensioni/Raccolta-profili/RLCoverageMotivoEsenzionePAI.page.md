# RLCoveragePAI

- [RLCoveragePAI](#RLCoveragePAI)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLCoveragePAI è stato strutturato a partire dalla risorsa generica FHIR [Coverage](http://hl7.org/fhir/R4/coverage.html) per rappresentare il motivo di esenzione dal co-pagamento dell'assistito nel contesto del Piano Assistenziale Individuale (PAI) – Regione Lombardia.

La risorsa è referenziata dalla sezione Motivo Esenzione dal Co-pagamento della Composition. I codici di esenzione dell'assistito sono riportati in `costToBeneficiary.exception.type`; poiché in FHIR R4 `costToBeneficiary.value[x]` è obbligatorio, in caso di esenzione l'importo a carico dell'assistito è valorizzato a 0 EUR.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCoveragePAI}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCoveragePAI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCoveragePAI, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCoveragePAI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCoveragePAI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCoveragePAI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCoveragePAI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
Esenzione dell'assistito: {{link:Coverage/Example-Coverage-1-PAI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLCoveragePAI:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| costToBeneficiary.exception.type | Codice di esenzione | La codifica è definita dal sistema dei codici di esenzione (OID 2.16.840.1.113883.2.9.2.30.6.22) |