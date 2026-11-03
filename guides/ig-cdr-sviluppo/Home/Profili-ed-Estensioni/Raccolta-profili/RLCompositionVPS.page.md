# RLCompositionVPS

- [RLCompositionVPS](#RLCompositionVPS)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)


## Descrizione
Il profilo RLCompositionVPS è stato strutturato a partire dalla risorsa standard FHIR [Composition](https://hl7.org/fhir/R4/composition.html) volta a descrivere header e body del Verbale di Pronto Soccorso di un paziente in Regione Lombardia.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionVPS}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionVPS, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionVPS, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionVPS, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionVPS, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionVPS, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionVPS, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
CarePlan: {{link:CarePlan/Example-CarePlan-1-VPS}}
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLCompositionVPS:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| type | Tipologia di documento | La codifica è definita dal sistema [LOINC](http://loinc.org) |
| status | Stato del documento | La codifica è definita dal ValueSet [CompositionStatus](http://hl7.org/fhir/ValueSet/composition-status). status = final |
| attester.mode | Modalità di attestazione del documento | La codifica è definita dal ValueSet [CompositionAttestationMode](http://hl7.org/fhir/ValueSet/composition-attestation-mode) |
| section.code | Codice identificativo di ciascuna sezione e sotto-sezione del documento | La codifica è definita dal sistema [LOINC](http://loinc.org) |