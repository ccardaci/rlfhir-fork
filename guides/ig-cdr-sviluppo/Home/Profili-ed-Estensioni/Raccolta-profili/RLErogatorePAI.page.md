# RLOrganizationErogatorePAI

- [RLOrganizationErogatorePAI](#RLOrganizationErogatorePAI)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLOrganizationErogatorePAI è stato strutturato a partire dalla risorsa generica FHIR [Organization](http://hl7.org/fhir/R4/organization.html) per rappresentare l'erogatore di una prestazione programmata nel contesto del Piano Assistenziale Individuale (PAI) – Regione Lombardia.

La risorsa è referenziata dalla ServiceRequest della sezione Programmazione Clinico Assistenziale tramite `ServiceRequest.performer`. Il codice dell'erogatore è riportato in `identifier`, con una slice per ciascuna tipologia di erogatore (ADI, Cure Intermedie, CDI, CDD, RIA, Cure Palliative) distinta dal sistema di identificazione; la descrizione dell'erogatore è riportata in `identifier.type.text`.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationErogatorePAI}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationErogatorePAI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationErogatorePAI, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationErogatorePAI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationErogatorePAI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationErogatorePAI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationErogatorePAI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
Erogatore della prestazione programmata: {{link:Organization/Example-OrganizationErogatore-1-PAI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLOrganizationErogatorePAI:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| identifier:erogatoreADI | Erogatore ADI | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.44) |
| identifier:erogatoreCureIntermedie | Erogatore Cure Intermedie | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.47) |
| identifier:erogatoreCDI | Erogatore CDI | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.45) |
| identifier:erogatoreCDD | Erogatore CDD | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.46) |
| identifier:erogatoreRIA | Erogatore RIA | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.48) |
| identifier:erogatoreCurePalliative | Erogatore Cure Palliative | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.52) |