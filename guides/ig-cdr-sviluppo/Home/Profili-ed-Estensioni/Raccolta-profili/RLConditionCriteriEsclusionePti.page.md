# RLConditionCriteriEsclusionePti

- [RLConditionCriteriEsclusionePti](#rlconditioncriteriesclusionepti)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLConditionCriteriEsclusionePti è stato strutturato a partire dalla risorsa generica FHIR [Condition](http://hl7.org/fhir/R4/condition.html) per rappresentare i criteri di esclusione nel contesto del Piano Terapeutico Individuale – Regione Lombardia. Il criterio di esclusione è in `category`, il suo stato in `code`.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCriteriEsclusionePti}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCriteriEsclusionePti, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCriteriEsclusionePti, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCriteriEsclusionePti, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCriteriEsclusionePti, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCriteriEsclusionePti, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCriteriEsclusionePti, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
Criteri di Esclusione (1): {{link:Condition/Example-Condition-CriteriEsclusione-1-PTI}}
<br>
Criteri di Esclusione (2): {{link:Condition/Example-Condition-CriteriEsclusione-2-PTI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nessun ValueSet specifico è associato a questo profilo. Il sistema di codifica di `category` dipende dal piano (dizionari Criteri Esclusione PT); `code` usa il dizionario Stato Criteri Esclusione (`urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.15.6.2`).