# RLDeviceRequestPAI

- [RLDeviceRequestPAI](#RLDeviceRequestPAI)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLDeviceRequestPAI è stato strutturato a partire dalla risorsa generica FHIR [DeviceRequest](http://hl7.org/fhir/R4/devicerequest.html) per rappresentare le richieste di protesi o ausili programmate per il paziente nel contesto del Piano Assistenziale Individuale (PAI) – Regione Lombardia.

La risorsa è referenziata dalla sezione Programmazione Clinico Assistenziale della Composition e dalla CarePlan del documento tramite `CarePlan.activity.reference`. Il flag protesica è riportato nell'estensione flagProtesica, la codifica ISO della protesi in `codeCodeableConcept`.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestPAI}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestPAI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestPAI, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestPAI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestPAI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestPAI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestPAI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
Richiesta di protesi o ausili: {{link:DeviceRequest/Example-DeviceRequest-1-PAI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLDeviceRequestPAI:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| extension:flagProtesica | Flag protesica | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.23) |
| code[x] | Codifica ISO protesica | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.25) |