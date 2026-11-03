# RLMedicationPAI

- [RLMedicationPAI](#RLMedicationPAI)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLMedicationPAI è stato strutturato a partire dalla risorsa generica FHIR [Medication](http://hl7.org/fhir/R4/medication.html) per rappresentare il farmaco della terapia farmacologica programmata nel contesto del Piano Assistenziale Individuale (PAI) – Regione Lombardia.

La risorsa è referenziata dalla MedicationRequest della sezione Programmazione Clinico Assistenziale tramite `medicationReference`. Il farmaco è identificato da una coding per ciascun codice disponibile: ATC, AIC e GE (gruppo di equivalenza).

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationPAI}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationPAI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationPAI, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationPAI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationPAI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationPAI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationPAI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
Farmaco programmato: {{link:Medication/Example-Medication-1-PAI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLMedicationPAI:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| code.coding:atc | Codice ATC | La codifica è definita dal sistema ATC (http://www.whocc.no/atc, OID 2.16.840.1.113883.6.73) |
| code.coding:aic | Codice AIC | La codifica è definita dal sistema AIC (OID 2.16.840.1.113883.2.9.6.1.5) |
| code.coding:ge | Codice GE | La codifica è definita dal sistema dei Gruppi di Equivalenza AIFA (OID 2.16.840.1.113883.2.9.6.1.51) |