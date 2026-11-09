# RLImmunizationVaccinazioniPSS

- [RLImmunizationVaccinazioniPSS](#RLImmunizationVaccinazioniPSS)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)


## Descrizione
Il profilo RLImmunizationVaccinazioniPSS è stato strutturato a partire dalla risorsa standard FHIR [Immunization](https://hl7.org/fhir/R4/immunization.html) per descrivere le vaccinazioni del paziente nel contesto del Profilo Sanitario Sintetico – Regione Lombardia.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazioniPSS}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazioniPSS, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazioniPSS, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazioniPSS, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazioniPSS, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazioniPSS, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazioniPSS, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Immunization: {{link:Immunization/Example-ImmunizationVaccinazioni-1-PSS}}
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLImmunizationVaccinazioniPSS:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| vaccineCode | Vaccino somministrato | La codifica è definita dal sistema AIC (`urn:oid:2.16.840.1.113883.2.9.6.1.5`) |
