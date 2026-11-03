# RLObservationPrecedentiEsamiEseguitiRSA

- [RLObservationPrecedentiEsamiEseguitiRSA](#RLObservationPrecedentiEsamiEseguitiRSA)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLObservationPrecedentiEsamiEseguitiRSA è stato strutturato a partire dalla risorsa generica FHIR [Observation](http://hl7.org/fhir/R4/observation.html) per rappresentare i precedenti esami eseguiti nel contesto del Referto di Specialistica Ambulatoriale – Regione Lombardia.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRSA}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRSA, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRSA, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRSA, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRSA, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRSA, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRSA, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
Precedenti Esami Eseguiti: {{link:Observation/Example-ObservationPrecedentiEsamiEseguiti-1-RSA}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLObservationPrecedentiEsamiEseguitiRSA:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| status | Stato dell'osservazione | La codifica è definita dal ValueSet [ObservationStatus](http://hl7.org/fhir/ValueSet/observation-status) |
| code | Codice dell'esame eseguito | La codifica è definita dal sistema [LOINC](http://loinc.org) oppure dal ValueSet [ICD-9-CM](https://terminology.hl7.org/7.4.0/en/ValueSet-v3-DiagnosisICD9CM.html) (OID 2.16.840.1.113883.6.103) |