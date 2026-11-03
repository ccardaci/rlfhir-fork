# RLCompositionPAI

- [RLCompositionPAI](#RLCompositionPAI)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLCompositionPAI è stato strutturato a partire dalla risorsa generica FHIR [Composition](http://hl7.org/fhir/R4/composition.html) per rappresentare l'header e il body del Piano Assistenziale Individuale (PAI) – Regione Lombardia.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionPAI}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionPAI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionPAI, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionPAI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionPAI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionPAI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionPAI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
Piano Assistenziale Individuale: {{link:Composition/Example-Composition-1-PAI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLCompositionPAI:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| type | Tipologia di documento | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.6.10), codice 31 "PIANO ASSISTENZIALE INDIVIDUALE" |
| section.code | Codice delle sezioni Attributi di sistema, Obiettivo presa in carico, Presa in carico, Anamnesi Fisiologica e Stili di Vita, Programmazione Clinico Assistenziale, Raccomandazioni Cliniche, Reti di Patologia, Intestazione Programmazione Clinico Assistenziale | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.1) |
| section.code | Codice delle sezioni Allergie e Motivo Esenzione dal co-pagamento | La codifica è definita dal sistema [LOINC](https://loinc.org/) |