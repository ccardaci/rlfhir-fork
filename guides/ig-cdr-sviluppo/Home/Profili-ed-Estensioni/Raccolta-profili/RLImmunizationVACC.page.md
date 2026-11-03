# RLImmunizationVaccinazione

- [RLImmunizationVaccinazione](#RLImmunizationVaccinazione)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)


## Descrizione
Il profilo RLImmunizationVaccinazione è stato strutturato a partire dalla risorsa standard FHIR [ImagingStudy](https://hl7.org/fhir/R4/immunization.html) volto a contenere le vaccinazioni eseguite in Regione Lombardia.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazione}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazione, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazione, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazione, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazione, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazione, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazione, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Vaccinazione 1: {{link:Immunization/immunization-vaccinazione}}
<br>
Vaccinazione 2: {{link:Immunization/immunization-dose1}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Attualmente non sono definiti value set specifici per il profilo RLImmunizationVaccinazione.

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| status | Stato dell'evento di immunizzazione | La codifica è definita dal ValueSet [ImmunizationStatus](http://hl7.org/fhir/ValueSet/immunization-status) |
| vaccineCode | Vaccino somministrato o non somministrato | La codifica è definita dal sistema [AIC](urn:oid:2.16.840.1.113883.2.9.6.1.5) |
| route | Via di somministrazione del vaccino | La codifica è definita dal ValueSet [HL7 RouteOfAdministration](http://terminology.hl7.org/ValueSet/v3-RouteOfAdministration) |
| site | Sede anatomica di somministrazione | La codifica è definita dal ValueSet [ActSite](http://terminology.hl7.org/ValueSet/v3-ActSite) |