# RLCarePlanProgettoIndividuale

- [RLCarePlanProgettoIndividuale](#rlcareplanprogettoindividuale)
  - [Descrizione](#descrizione)
  - [Tipologie di ricerca](#tipologie-di-ricerca)
    - [1. Progetti individuali attivi](#1-progetti-individuali-attivi)
    - [2. Progetti individuali di un paziente](#2-progetti-individuali-di-un-paziente)
  - [Search parameter](#search-parameter)
  - [ValueSet](#valueset)


## Descrizione

Il profilo RLCarePlanProgettoIndividuale è stato strutturato a partire dalla risorsa generica FHIR [CarePlan](http://hl7.org/fhir/R4/careplan.html) per descrivere il progetto individuale di un assistito. Il contenuto informativo contiene i dettagli delle attività e dei servizi sanitari, socioassistenziali, infermieristici e sociali che devono essere attivati al paziente. Inoltre, sono riportate varie informazioni generali quali: durata del progetto, obiettivi di salute, case manager, esiti delle valutazioni, patologie principali, secondarie e ulteriori, allergie, esenzioni e stili di vita dell’assistito. 

Di seguito è presentato il contenuto del profilo in diversi formati. La corrispondente definizione è consultabile al seguente link: {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale}}.

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
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, snapshot}}
</div>

<div id="Differential View" class="tabcontent">
  <h3>Differential View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, diff}}
</div>

<div id="Hybrid View" class="tabcontent"  style="display:block">
  <h3>Hybrid View</h3>
{{tree:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, hybrid}}
</div>

<div id="Table View" class="tabcontent">
  <h3>Table View</h3>
{{table:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, snapshot}}
</div>

<div id="XML View" class="tabcontent">
  <h3>XML View</h3>
{{xml:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, snapshot}}
</div>

<div id="JSON View" class="tabcontent">
  <h3>JSON View</h3>
{{json:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale, snapshot}}
</div>

<div id="Esempi" class="tabcontent">
  <h3>Esempi</h3>
{{link:esempio-CarePlan-Progetto-Individuale}}
<br>
</div>

<!-- ===================================================FINE SEZIONE=================================================== -->

## Tipologie di ricerca

###	1. Progetti individuali attivi

Questa ricerca deve essere effettuata dagli Enti Erogatori di servizi socioassistenziali con lo scopo di ottenere l’elenco dei progetti individuali prodotti da un’ASST per gli assistiti che necessitano dell’attivazione di un servizio sociosanitario presso l’Ente Erogatore stesso. 

Premesso che esiste un'unica versione del progetto individuale in stato “attivo” e quindi in corso di validità, all’Ente Erogatore verrà restituito solo ed esclusivamente il dettaglio informativo del servizio socioassistenziale da attivare al cittadino. Inoltre, tra le informazioni disponibili riportate nel bundle saranno presenti anche i dettagli delle valutazioni effettuate dagli assistititi e gli eventuali esiti delle stesse. 

I parametri da valorizzare obbligatoriamente per effettuare la ricerca sono:
-	status: da compilare con il valore “active”
-	activity.reference(RLServiceRequestServiziSocioAssistenziali).code.coding.code: codice del servizio socioassistenziale d’interesse
-	author.reference(RLOrgnizationL1).identifier: codice L1 dell’ASST che ha prodotto il progetto individuale

Inoltre, è possibile valorizzare il seguente parametro:
-	lastUpdated: data e ora dell’ultimo aggiornamento dei dati

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

|     SCOPE    | Progetti individuali attivi |
|---|---|
| VERB | GET |
| BASE_URL | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
| PARAMETRI | CarePlan?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale<br>&activity-reference:ServiceRequest.code=C-DOM<br>&author:Organization.identifier={codiceLivelloL1}<br>&_lastUpdated=gt{dataLimiteIntervalloInferiore}<br>&_lastUpdated=lt{dataLimiteIntervalloSuperiore}<br>&status=active<br>&_include=* |

Esempio chiamata:

  https://api.servizirl.it/c/operatori.siss/nea/v1.0.0/npri/CarePlan?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale&activity-reference:ServiceRequest.code=C-DOM&author:Organization.identifier=030701&_lastUpdated=gt2022-11-18&_lastUpdated=lt2022-11-30&status=active&_include=*

Restituirà tutti i Progetti Individuali attivi contenenti esclusivamente i dettagli del ricovero domiciliare in carico all’ente con codice livello 1 "030701" e creati e/o modificati tra il giorno 18-11-2022 e il giorno 30-11-2022. Il risultato della ricerca conterrà anche tutte le informazioni associate referenziate nel profilo.

Un esempio di Bundle di risposta può essere consultato qui: {{link:esempio-ricerca-pi-attivi}}.

<em><font style="color:green">
_Criterio di ricerca applicato per le funzionalità descritte nei documenti:_
- _DC-COOP-FHIR#01 (Specifiche di cooperazione applicativa nell’ambito delle cure domiciliari)_</font></em>.

### 2. Progetti individuali di un paziente

Questa ricerca deve essere effettuata dagli Enti Erogatori di servizi socioassistenziali con lo scopo di fruire dello storico dei progetti individuali di un assistito che contengono l’attivazione di un determinato servizio socioassistenziale.

L’elenco dei progetti individuali conterrà solo ed esclusivamente i dettagli dell’attivazione di un servizio socioassistenziale affidato all’Ente Erogatore chiamante. In virtù di ciò, lo scopo della ricerca è quello di consentire all’Ente Erogatore il confronto tra le versioni del progetto individuale precedentemente salvate e quelle restituite dalla ricerca.

I parametri da valorizzare obbligatoriamente per effettuare la ricerca sono:
-	activity.reference(RLServiceRequestServiziSocioAssistenziali).identifier: codice identificativo del servizio sociosanitario attivato/da attivare all’assistito
-	subject.reference(RLPatientCittadino).identifier: codice fiscale dell’assistito

Nella tabella di seguito vengono riportati i dettagli tecnici per l’implementazione della ricerca:

|     SCOPE    |Progetti individuali di un paziente|
|---|---|
|     VERB    |     GET    |
| BASE_APIMANAGER | https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri |
|     URL    | CarePlan?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale<br>&activity-reference:ServiceRequest.identifier=\{_numeroPratica_\}<br>&subject:Patient.identifier=\{_codiceFiscale_\}<br>&_include=CarePlan:activity-reference<br>&_include=CarePlan:subject |

A titolo esemplificativo, la chiamata: 

    CarePlan?_profile=https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanProgettoIndividuale&activity-reference:ServiceRequest.identifier=2022000001&subject:Patient.identifier=RSSMRA80A01F205X&_include=CarePlan:activity-reference&_include=CarePlan:subject

Restituirà lo storico dei progetti contenenti esclusivamente i dettagli del ricovero domiciliare dell’assistito con codice fiscale “RSSMRA80A01F205X”, afferente alla pratica numero "2022000001". Il risultato della ricerca conterrà anche le informazioni inerenti al servizio sociosanitario attivo e al paziente stesso.

Un esempio di Bundle di risposta può essere consultato qui: {{link:esempio-ricerca-storico-pi}}.

<em><font style="color:green">
_Criterio di ricerca applicato per le funzionalità descritte nei documenti:_
- _DC-COOP-FHIR#01 (Specifiche di cooperazione applicativa nell’ambito delle cure domiciliari)_</font></em>.


<!-- ===================================================FINE SEZIONE=================================================== -->

## Search parameter
Sulla base di quanto descritto nelle tipologie di ricerca sono riportati di seguito i parametri di ricerca del profilo RLCarePlanProgettoIndividuale: 
- _include
- _lastUpdated
- _profile
- activity-reference
- status
- subject

<!-- ===================================================FINE SEZIONE=================================================== -->

## ValueSet

Attualmente non sono presenti value set nei campi del profilo RLCarePlanProgettoIndividuale.

<br> 
