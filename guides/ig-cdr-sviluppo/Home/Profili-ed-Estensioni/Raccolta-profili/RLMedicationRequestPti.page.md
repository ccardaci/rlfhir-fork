# RLMedicationRequestPti

- [RLMedicationRequestPti](#rlmedicationrequestpti)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLMedicationRequestPti è stato strutturato a partire dalla risorsa generica FHIR [MedicationRequest](http://hl7.org/fhir/R4/medicationrequest.html) per rappresentare il programma terapeutico nel contesto del Piano Terapeutico Individuale – Regione Lombardia. Contiene farmaco, durata del trattamento, via di somministrazione, dosaggio e frequenza; il dosaggio di carico è identificato dal tipo 04.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPti}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPti, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPti, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPti, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPti, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPti, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPti, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Programma Terapeutico (1): {{link:MedicationRequest/Example-MedicationRequest-1-PTI}}
<br>
Programma Terapeutico (2): {{link:MedicationRequest/Example-MedicationRequest-2-PTI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nessun ValueSet specifico è associato a questo profilo. La via di somministrazione usa HL7 RouteOfAdministration (`http://terminology.hl7.org/CodeSystem/v3-RouteOfAdministration`).