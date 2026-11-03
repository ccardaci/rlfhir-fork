# {{page-title}}

## Endpoint FHIR

### API Manager
L'API Manager espone i servizi FHIR definiti nell'ecosistema di Regione Lombardia. 
Il base_url con cui accedere a tali servizi è il seguente:
        
        <base_API_Manager> = https://api.servizirl.it/c/operatori.siss/fhir/v1.0.0/npri

L'elenco delle API esposte è:

|Metodo HTTP|URL|Nome profilo|Detentore del dato|
|---|---|---|
|GET|<base_API_Manager>/_CarePlan_|RLCarePlanProgettoIndividuale|SGDT|
|GET|<base_API_Manager>/_QuestionnaireResponse_|RLQuestionnaireResponseValutazione|SGDT|
|GET|<base_API_Manager>/_Organization_|RLOrganizationL1, RLOrganizationL2, RLOrganizationL3 |DDC FHIR Server|
|GET|<base_API_Manager>/_Practitioner_|RLPractitionerMedicoPrescrittore|DDC FHIR Server|
|GET|<base_API_Manager>/_PractitionerRole_|RLPractitionerRoleMedicoPrescrittore|DDC FHIR Server|
|GET|<base_API_Manager>/_Location_|RLLocationPLOLetto|NPRI FHIR Server|
|POST|<base_API_Ente>/_Bundle_|RLBundleNotificaErrori|Ente Erogatore|

### API Enti erogatori
I servizi FHIR esposti dai Sistemi Informativi degli Enti Erogatori sono accessibili attraverso i canali protetti tra ARIAspa e gli Enti stessi.
Il base_url con cui accedere a tali servizi è il seguente:

        <base_API_Ente> = https://<nome_host_Ente>/<contesto_FHIR>/<codice_Cudes_L1>/v1.0.0/<tipologia_servizio_sociosanitario>

dove:
- <nome_host_Ente>: alias corrispondente all’indirizzo IP dell’Ente definito sul canale protetto; la risoluzione dell’alias è inserita nel DNS di ARIAspa
- <contesto_FHIR>: fhir per la Produzione reale; fhirtest per la Produzione virtuale, da utilizzare per i test delle integrazioni propedeutici all’avvio in produzione
- <codice_Cudes_L1>: codice L1 dell’Ente Erogatore, al quale è collegato il canale protetto
- <tipologia_servizio_sociosanitario>: nome della tipologia del servizio sociosanitario offerto dall'erogatore. L’elenco delle tipologie al momento disponibili comprende:
        - `erogazione-adi`

Esempio: `https://fhir.hcmanager.it/fhir/732553/v1.0.0/erogazione-adi`

L'elenco delle API esposte è:

|Metodo HTTP|URL|Nome profilo|Detentore del dato|
|---|---|---|
|GET|<base_API_Ente>/_Procedure_|RLProcedurePrestazione|Ente Erogatore|
|GET|<base_API_Ente>/_ServiceRequest_|RLServiceRequestSospensioneADI, RLServiceRequestRivalutazione|Ente Erogatore|
|POST|<base_API_Ente>/_Bundle_|RLBundleNotificaErrori|Ente Erogatore|
|GET|<base_API_Ente>/_Location_|RLLocationPLOLetto|Ente Erogatore|

## Header 
Le chiamate HTTP relative all'integrazione FHIR devono contenere i seguenti header:

|Nome header|Valore|Descrizione|
|---|---|---|
|Content-Type|application/fhir+json|mime type del formato di scambio|
|Authorization | Bearer \<valore\> | \<valore\>: rappresenta il valore dell’Access Token ottenuto in precedenza invocando i servizi di autenticazione di API Manager |


