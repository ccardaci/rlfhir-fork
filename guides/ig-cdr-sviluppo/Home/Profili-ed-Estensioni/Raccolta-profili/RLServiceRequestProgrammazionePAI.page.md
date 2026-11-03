# RLServiceRequestPAI

- [RLServiceRequestPAI](#RLServiceRequestPAI)
  - [Descrizione](#descrizione)
  - [ValueSet](#valueset)

## Descrizione
Il profilo RLServiceRequestPAI è stato strutturato a partire dalla risorsa generica FHIR [ServiceRequest](http://hl7.org/fhir/R4/servicerequest.html) per rappresentare le prestazioni programmate per il paziente nel contesto del Piano Assistenziale Individuale (PAI) – Regione Lombardia.

Per ciascuna prestazione programmata è prevista una risorsa ServiceRequest, referenziata dalla sezione Programmazione Clinico Assistenziale della Composition e dalla CarePlan del documento tramite `CarePlan.activity.reference`. Oltre alla tipologia e al codice della prestazione, la risorsa riporta il flag di telemedicina (`locationCode`), la quantità, la frequenza e la durata (`occurrenceTiming`), l'erogatore (`performer`), la valutazione (`reasonReference`) e, tramite estensioni, la validità del bisogno e gli intervalli temporali.

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPAI}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPAI, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPAI, diff}}
</div>

<div id="Hybrid View" class="tabcontent" style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPAI, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPAI, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPAI, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPAI, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
 <h3>Esempi</h3>
Prestazione programmata: {{link:ServiceRequest/Example-ServiceRequest-1-PAI}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet
Nella seguente tabella sono elencati i value set e i sistemi di codifica relativi al profilo RLServiceRequestPAI:

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| category | Tipologia prestazione | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.18) |
| code (ambulatoriale) | Prestazione ambulatoriale | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.6.11) |
| code (vaccinale) | Prestazione vaccinale | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.26) |
| code (codice regionale vaccino) | Codice regionale del vaccino | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.6.2) |
| code (ricovero) | Prestazione di ricovero | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.28) |
| code (ADI) | Assistenza domiciliare integrata | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.29) |
| code (cure intermedie) | Cure intermedie | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.30) |
| code (CDI) | Centro diurno integrato | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.32) |
| code (CDD) | Centro diurno per disabili | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.50) |
| code (RIA) | Riabilitazione ambulatoriale | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.39) |
| code (cure palliative) | Cure palliative | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.51) |
| code (intervento educazionale) | Intervento educazionale | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.35) |
| locationCode | Flag telemedicina | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.55) |
| occurrenceTiming.repeat.boundsDuration | Unità di misura della durata | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.43) |
| occurrenceTiming.code | Tipologia frequenza | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.42) |
| extension:validitaBisogno | Validità del bisogno | La codifica è definita dal sistema CRS-SISS (OID 2.16.840.1.113883.2.9.2.30.3.1.3.13.6.41) |