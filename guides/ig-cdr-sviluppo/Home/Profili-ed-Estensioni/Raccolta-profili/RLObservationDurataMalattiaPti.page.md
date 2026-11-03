# RLObservationDurataMalattiaPti

- [RLObservationDurataMalattiaPti](#rlobservationduratamalattiapti)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLObservationDurataMalattiaPti è stato strutturato a partire dalla risorsa generica FHIR [Observation](http://hl7.org/fhir/R4/observation.html) per rappresentare la durata della malattia (BPCO) nel contesto del Piano Terapeutico Individuale – Regione Lombardia. Il codice è fissato a 04 (Durata della malattia) e il valore è espresso in anni.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDurataMalattiaPti}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDurataMalattiaPti, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDurataMalattiaPti, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDurataMalattiaPti, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDurataMalattiaPti, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDurataMalattiaPti, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDurataMalattiaPti, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Durata Malattia (1): {{link:Observation/Example-Observation-DurataMalattia-1-PTI}}
<br>
Durata Malattia (2): {{link:Observation/Example-Observation-DurataMalattia-2-PTI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nessun ValueSet specifico è associato a questo profilo. Il codice `Observation.code` è fissato a `04` (`urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.15.6.8`).