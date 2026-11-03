# RLConditionPAI

- [RLConditionPAI](#RLConditionPAI)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLConditionPAI è stato strutturato a partire dalla risorsa generica FHIR [Condition](http://hl7.org/fhir/R4/condition.html) per rappresentare le patologie della presa in carico del paziente nel contesto del Piano Assistenziale Individuale (PAI) – Regione Lombardia.

Per ciascuna patologia (Principale, Secondaria, Addizionale) è prevista una risorsa Condition, referenziata dall'Encounter della presa in carico tramite `Encounter.diagnosis`. La posizione della patologia è indicata in `Encounter.diagnosis.rank` (1 = Principale, 2 = Secondaria, 3 = Addizionale). Il livello di complessità (`severity`) è valorizzato per la Patologia Principale.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionPAI}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionPAI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionPAI, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionPAI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionPAI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionPAI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionPAI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
Patologia principale della presa in carico: {{link:Condition/Example-Condition-1-PAI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLConditionPAI:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| code | Patologia (principale, secondaria, addizionale) | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.10) |
| severity | Livello di complessità | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.49) |