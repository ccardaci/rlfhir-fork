# RLProcedurePAI

- [RLProcedurePAI](#RLProcedurePAI)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLProcedurePAI è stato strutturato a partire dalla risorsa generica FHIR [Procedure](http://hl7.org/fhir/R4/procedure.html) per rappresentare le prestazioni correlate alla patologia nel contesto della presa in carico del paziente del Piano Assistenziale Individuale (PAI) – Regione Lombardia.

Per ciascuna prestazione correlata è prevista una risorsa Procedure. Il tipo di prestazione è indicato in `category` (1 = Prestazioni Ambulatoriali; 2 = Prestazioni Farmaceutiche; 3 = Regimi Privati; 4 = Ausili o Presidi Medici; 99 = Altro); la prestazione è codificata in `code.coding` oppure, per il tipo 99 (Altro), descritta in testo libero in `code.text`.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePAI}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePAI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePAI, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePAI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePAI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePAI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePAI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
Prestazione correlata alla patologia: {{link:Procedure/Example-Procedure-1-PAI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLProcedurePAI:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| category | Tipo prestazioni correlate alla patologia | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.60) |
| code | Prestazione correlata | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.61) |