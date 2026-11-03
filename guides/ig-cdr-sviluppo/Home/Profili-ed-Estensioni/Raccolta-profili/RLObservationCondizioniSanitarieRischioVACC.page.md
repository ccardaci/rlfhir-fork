# RLObservationCondizioniSanitarieRischio

- [RLObservationCondizioniSanitarieRischio](#RLObservationCondizioniSanitarieRischio)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLObservationCondizioniSanitarieRischio è stato strutturato a partire dalla risorsa generica FHIR [Observation](http://hl7.org/fhir/R4/observation.html) per rappresentare le condizioni sanitarie a rischio per una vaccinazione nel contesto del Referto di Radiologia – Regione Lombardia.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCondizioniSanitarieRischio}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCondizioniSanitarieRischio, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCondizioniSanitarieRischio, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCondizioniSanitarieRischio, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCondizioniSanitarieRischio, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCondizioniSanitarieRischio, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCondizioniSanitarieRischio, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
{{link:Observation/observation-condizione}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLObservationCondizioniSanitarieRischio:


| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| code | Codice identificativo dell'osservazione | La codifica è definita dal sistema [LOINC](http://loinc.org) |
| status | Stato dell'osservazione | La codifica è definita dal ValueSet [ObservationStatus](http://hl7.org/fhir/ValueSet/observation-status) |
| valueCodeableConcept | Codice della condizione sanitaria a rischio | La codifica è definita dal sistema [ICD9-CM](urn:oid:2.16.840.1.113883.6.2) oppure dal sistema regionale [AVN: Condizioni sanitarie a rischio](urn:oid:2.16.840.1.113883.2.9.6.1.56.1) |