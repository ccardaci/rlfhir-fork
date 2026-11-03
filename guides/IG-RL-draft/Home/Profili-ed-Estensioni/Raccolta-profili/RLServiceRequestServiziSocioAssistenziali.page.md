# RLServiceRequestServiziSocioAssistenziali

- [RLServiceRequestServiziSocioAssistenziali](#rlservicerequestservizisocioassistenziali)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [1. Stato della richiesta](#1-stato-della-richiesta)
      - [Endpoint dedicato](#endpoint-dedicato)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione
Il profilo RLServiceRequestServiziSocioAssistenziali è stato strutturato a partire dalla risorsa generica FHIR [ServiceRequest](http://hl7.org/fhir/R4/servicerequest.html) e definisce i dettagli relativi all’attivazione di un servizio socioassistenziale per un assistito. Se già noto, all’interno del profilo verrà riportato l’Ente Erogatore della rete territoriale responsabile della presa in carico. 

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:Examples-Example-ServiceRequest-ServiziSocioAssistenziali}}
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

### 1. Stato della richiesta NEA

Le ricerche su questo tipo di risorsa FHIR vengono eseguite tramite API esposte dal componente API Manager (vedi la pagina Paradigmi di comunicazione e API RESTful nella sezione Contesto).

Questa ricerca deve essere effettuata dall'applicativo di Gestione 116117 NEA con lo scopo di ottenere lo stato della richiesta dalla piattaforma SGDT.

I parametri da valorizzare obbligatoriamente per effettuare la ricerca sono:

- **Identifier** con system `https://fhir.siss.regione.lombardia.it/sid/codiceIdentificativoNEA`: è l'identificativo univoco generato dall'applicativo di gestione 116117 NEA quando invia la richiesta a SGDT e associato al profilo RLServiceRequestServiziSocioAssistenziali;
- **Identifier** con system `https://fhir.siss.regione.lombardia.it/sid/codiceIdentificativoSGDT`: è l'identificativo univoco generato da SGDT quando la richiesta è stata ricevuta correttamente e associato al profilo RLServiceRequestServiziSocioAssistenziali.

La tabella seguente riassume le modalità di utilizzo dell’API.

| Voce | Valore |
|---|---|
| **VERB** | GET |
| **BASE URL** | https://api.servizirl.it/c/operatori.siss/nea/v1.0.0/verifica-stato-segnalazione |
| **PARAMETRI** | `/ServiceRequest?codiceNEA=<identificativo richiesta in NEA>&codiceSGDT=<identificativo segnalazione in SGDT>` |

# Endpoint dedicato

Esempio chiamata:    
https://api.servizirl.it/c/operatori.siss/nea/v1.0.0/verifica-stato-segnalazione/ServiceRequest?codiceNEA=NEA-2026-00001&codiceSGDT=SOC-00000001

### 2. Stato di altri tipi di richiesta generica per pazienti in carico a MMG

Le ricerche su questo tipo di risorsa FHIR vengono eseguite tramite API esposte dal componente API Manager (vedi la pagina Paradigmi di comunicazione e API RESTful nella sezione Contesto).
Questa ricerca deve essere effettuata dagli applicativi utilizzati da MMG che hanno inviato a SGDT una richiesta di attivazione di un setting assistenziale.
Lo scopo della ricerca è quello di ottenere lo stato della Richiesta di Transizione COT generata in SGDT per il paziente oggetto della richiesta stessa.
La tabella seguente riassume le modalità di utilizzo dell’API.

| Voce | Valore |
|---|---|
| **VERB** | GET |
| **BASE URL** | https://api.servizirl.it/c/operatori.siss/portaleMMG/v1.0.0/stato-segnalazione |
| **PARAMETRI** | `ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali&identifier=`<br>`https://fhir.siss.regione.lombardia.it/sid/codiceIdentificativoPortaleMMG\|<identificativo Portale>&identifier=https://fhir.siss.regione.lombardia.it/sid/codiceIdentificativoSGDT\|<identificativo SGDT>` |

# Endpoint dedicato
```text
Esempio chiamata:        
https://api.servizirl.it/c/operatori.siss/portaleMMG/v1.0.0/stato-segnalazione/ServiceRequest?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestServiziSocioAssistenziali&identifier=https://fhir.siss.regione.lombardia.it/sid/codiceIdentificativoPortaleMMG|PPP0001&identifier=https://fhir.siss.regione.lombardia.it/sid/codiceIdentificativoSGDT|SOC_0000002
```
<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Nella seguente tabella sono elencati i value-set relativi al profilo RLServiceRequestServiziSocioAssistenziali.

| Nome | Descrizione | Riferimento al dettaglio della codifica |
|---|---|---|
| Code | Codice e descrizione del servizio sociosanitario da attivare |  La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/DDC-DescL2}}| 
| ReasonCode | Codice e descrizione dei percorsi di cure domiciliari |  La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-PercorsiCDom}}| 
| ReasonCode | Motivo della segnalazione |  La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SGDT-MotivoSegnalazione}}| 
| causaleDimissione  | Codice e descrizione della causale di dimissione |  La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-CausaleDimissione}}| 
| soggettoProponentePIC | Codice e descrizione del soggetto che ha proposto la presa in carico dell'assistito |  La codifica è definita dal ValueSet {{link:https://fhir.siss.regione.lombardia.it/ValueSet/SIAD-ProponentePIC}}| 