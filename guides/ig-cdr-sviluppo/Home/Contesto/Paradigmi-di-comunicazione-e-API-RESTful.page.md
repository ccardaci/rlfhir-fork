# Paradigmi di comunicazione e API RESTful

[[_TOC_]]

<!--
  NOTA PER LA COMPILAZIONE
  Fonte: Documento Integrazione Broker FSE 2.0, Sogei, v1.9 (25/08/2026).
  I valori [DA DEFINIRE] vanno sostituiti prima della pubblicazione.
-->

# 1. Header e autenticazione

L'accesso ai servizi di consultazione avviene tramite **credenziale**, con una modalità diversa in base al fruitore del servizio:

| Fruitore       | Tipo di credenziale | Descrizione                                   |
| -------------- | ------------------- | --------------------------------------------- |
| Assistito      | Credenziale SAML    | [DA DEFINIRE: modalità di ottenimento]        |
| Professionista | ACTIVCRED           | [DA DEFINIRE: modalità di ottenimento]        |

Le chiamate devono contenere i seguenti header:

| Nome header   | Valore                | Descrizione                                                                   |
| ------------- | --------------------- | ----------------------------------------------------------------------------- |
| [DA DEFINIRE] | `<credenziale>`       | Credenziale SAML (fruitore Assistito) o ACTIVCRED (fruitore Professionista)   |
| Accept        | application/json      | Formato della risposta                                                        |

## 1.1 Fruitore Assistito: credenziale SAML

Gli endpoint con prefisso `assistito-` richiedono una credenziale SAML.


## 1.2 Fruitore Professionista: ACTIVCRED

Gli endpoint con prefisso `professionista-` richiedono una credenziale ACTIVCRED.

# 2. Paradigma FHIR RESTful

Il CDR espone un livello di consultazione basato su risorse FHIR.

Le ricerche avvengono tramite chiamate HTTP GET con parametri di ricerca FHIR e restituiscono un Bundle di tipo `searchset`. Quasi tutti i servizi richiedono i parametri `_revinclude=Composition:entry` e `_revinclude:iterate=DocumentReference:related`, così che il risultato includa anche la Composition e la DocumentReference del documento da cui proviene il dato.

## 2.1 Endpoint FHIR

```
<BASE_PATH> = [DA DEFINIRE]
```

Esempio di chiamata:

```
curl -X GET "<BASE_PATH>/v1/assistito-consultazione-dati-clinici/Condition?patient.identifier=<CODICE_FISCALE>&code=2.16.840.1.113883.6.103|<CODICE>&_sort=-onset-date&_count=10&_revinclude=Composition:entry&_revinclude:iterate=DocumentReference:related" \
  -H "[HEADER CREDENZIALE]: <credenziale SAML>" \
  -H "Accept: application/json"
```

L'elenco delle API di consultazione è il seguente.

| Metodo | URL | Fruitore | Profilo RL |
| ------ | --- | -------- | ---------- |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-clinici/Condition` | Assistito | RLConditionCore |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-sintesi-eventi/Condition` | Professionista | RLConditionCore |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-ricovero-ps/Condition` | Professionista | RLConditionCore |
| GET | `<BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/Condition` | Professionista | RLConditionCore |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-clinici/AllergyIntolerance` | Assistito | RLAllergyIntoleranceCore |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-dossier-farmaceutico/AllergyIntolerance` | Assistito | RLAllergyIntoleranceCore |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-dossier-farmaceutico/AllergyIntolerance` | Professionista | RLAllergyIntoleranceCore |
| GET | `<BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/AllergyIntolerance` | Professionista | RLAllergyIntoleranceCore |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-clinici/MedicationStatement` | Assistito | RLMedicationStatementTerapiaFarmacologica |
| GET | `<BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/MedicationStatement` | Professionista | RLMedicationStatementTerapiaFarmacologica |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-clinici/MedicationDispense` | Assistito | — |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-dossier-farmaceutico/MedicationDispense` | Assistito | — |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-dossier-farmaceutico/MedicationDispense` | Professionista | — |
| GET | `<BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/MedicationDispense` | Professionista | — |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-dossier-farmaceutico/MedicationRequest` | Assistito | — |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-dossier-farmaceutico/MedicationRequest` | Professionista | — |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-dossier-farmaceutico/MedicationAdministration` | Assistito | — |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-dossier-farmaceutico/MedicationAdministration` | Professionista | — |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-clinici/Observation` | Assistito | RLObservationDecorsoClinico, RLObservationQuesitoDiagnostico, RLObservationComplicanzeRad, RLObservationPrecedentiEsamiEseguitiRad, RLObservationEsameEseguitoRad |
| GET | `<BASE_PATH>/v1/assistito-visualizzazione-andamento-dati-clinici/Observation` | Assistito | RLObservationDecorsoClinico, RLObservationQuesitoDiagnostico, RLObservationComplicanzeRad, RLObservationPrecedentiEsamiEseguitiRad, RLObservationEsameEseguitoRad |
| GET | `<BASE_PATH>/v1/professionista-visualizzazione-andamento-dati-clinici/Observation` | Professionista | RLObservationDecorsoClinico, RLObservationQuesitoDiagnostico, RLObservationComplicanzeRad, RLObservationPrecedentiEsamiEseguitiRad, RLObservationEsameEseguitoRad |
| GET | `<BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/Observation` | Professionista | RLObservationDecorsoClinico, RLObservationQuesitoDiagnostico, RLObservationComplicanzeRad, RLObservationPrecedentiEsamiEseguitiRad, RLObservationEsameEseguitoRad |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-sintesi-eventi-dettaglio/Observation` | Assistito | RLObservationDecorsoClinico, RLObservationQuesitoDiagnostico, RLObservationComplicanzeRad, RLObservationPrecedentiEsamiEseguitiRad, RLObservationEsameEseguitoRad |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-sintesi-eventi-dettaglio/Observation` | Professionista | RLObservationDecorsoClinico, RLObservationQuesitoDiagnostico, RLObservationComplicanzeRad, RLObservationPrecedentiEsamiEseguitiRad, RLObservationEsameEseguitoRad |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-clinici/Procedure` | Assistito | — |
| GET | `<BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/Procedure` | Professionista | — |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-clinici/DiagnosticReport` | Assistito | — |
| GET | `<BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/DiagnosticReport` | Professionista | — |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-clinici/Immunization` | Assistito | — |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-vaccinazioni/Immunization` | Professionista | — |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-sintesi-eventi-dettaglio/Immunization` | Assistito | — |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-sintesi-eventi-dettaglio/Immunization` | Professionista | — |
| GET | `<BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/Immunization` | Professionista | — |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-vaccinazioni/ImmunizationRecommendation` | Professionista | — |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-sintesi-eventi/Encounter` | Assistito | RLEncounterCore |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-sintesi-eventi/Encounter` | Professionista | RLEncounterCore |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-ricovero-ps/Encounter` | Professionista | RLEncounterCore |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-prestazioni/Encounter` | Professionista | RLEncounterCore |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-sintesi-eventi-dettaglio/ImagingStudy` | Assistito | RLImagingStudyRAD |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-sintesi-eventi-dettaglio/ImagingStudy` | Professionista | RLImagingStudyRAD |
| GET | `<BASE_PATH>/v1/professionista-consultazione-dati-ricovero-ps/Location` | Professionista | RLLocationCore |
| GET | `<BASE_PATH>/v1/assistito-consultazione-dati-accesso/AuditEvent` | Assistito | — |

# 3. Dettaglio dei servizi di consultazione

Convenzioni valide per tutte le tabelle:

- `patient.identifier` contiene il codice fiscale dell'assistito;
- i parametri di tipo codice si valorizzano nel formato `[OID]|[codice]`;
- `_count` accetta al massimo 10 risultati per pagina, salvo diversa indicazione;
- "Includi Composition / DocumentReference" indica i parametri `_revinclude=Composition:entry` e `_revinclude:iterate=DocumentReference:related`, obbligatori dove indicato.

## 3.1 Condition

### Dati clinici (Assistito)

`GET <BASE_PATH>/v1/assistito-consultazione-dati-clinici/Condition` — è obbligatorio valorizzare almeno uno tra `onset-date` e `_count`.

| Parametro             | Obbl. | Tipo            | Valori ammessi                          | Descrizione                         |
| --------------------- | ----- | --------------- | --------------------------------------- | ----------------------------------- |
| patient.identifier    | Sì    | String          | Dinamico                                | Codice fiscale del paziente         |
| code                  | Sì    | String          | `2.16.840.1.113883.6.103\|[Code]`       | Codice ICD-9-CM                     |
| _sort                 | Sì    | String          | onset-date, -onset-date                 | Ordinamento                         |
| _revinclude           | Sì    | String          | Composition:entry                       | Includi Composition                 |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related               | Includi DocumentReference           |
| onset-date            | No    | array of String | Dinamico                                | Data di insorgenza (YYYY-MM-DD)     |
| _count                | No    | integer         | max 10                                  | Risultati per pagina                |

### Sintesi eventi (Professionista)

`GET <BASE_PATH>/v1/professionista-consultazione-dati-sintesi-eventi/Condition`

| Parametro             | Obbl. | Tipo            | Valori ammessi                                                                                                     | Descrizione                     |
| --------------------- | ----- | --------------- | ------------------------------------------------------------------------------------------------------------------ | ------------------------------- |
| patient.identifier    | Sì    | String          | Dinamico                                                                                                           | Codice fiscale del paziente     |
| _include              | Sì    | String          | Condition:encounter                                                                                                | Includi Encounter               |
| _include:iterate      | Sì    | array of String | Encounter:location, Location:organization, Encounter:participant, PractitionerRole:practitioner, Organization:partof | Inclusioni iterative          |
| _sort                 | Sì    | String          | onset-date, -onset-date                                                                                            | Ordinamento                     |
| _revinclude           | Sì    | String          | Composition:entry                                                                                                  | Includi Composition             |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related                                                                                          | Includi DocumentReference       |
| onset-date            | No    | array of String | Dinamico                                                                                                           | Data di insorgenza (YYYY-MM-DD) |
| _count                | No    | integer         | max 10                                                                                                             | Risultati per pagina            |

### Ricovero/PS (Professionista)

`GET <BASE_PATH>/v1/professionista-consultazione-dati-ricovero-ps/Condition`

| Parametro             | Obbl. | Tipo            | Valori ammessi            | Descrizione                   |
| --------------------- | ----- | --------------- | ------------------------- | ----------------------------- |
| patient.identifier    | Sì    | String          | Dinamico                  | Codice fiscale del paziente   |
| encounter.class       | Sì    | array of String | EMER, IMP                 | Classe dell'Encounter         |
| _revinclude           | Sì    | String          | Composition:entry         | Includi Composition           |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related | Includi DocumentReference     |
| _count                | No    | integer         | Dinamico                  | Risultati per pagina          |

### Parametri clinici rilevanti (Professionista)

`GET <BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/Condition` — restituisce l'ultimo dato disponibile (tipicamente `_sort=-onset-date&_count=1`).

| Parametro             | Obbl. | Tipo            | Valori ammessi                    | Descrizione                           |
| --------------------- | ----- | --------------- | --------------------------------- | ------------------------------------- |
| code                  | Sì    | String          | `2.16.840.1.113883.6.103\|[Code]` | Codice ICD-9-CM                       |
| patient.identifier    | Sì    | String          | Dinamico                          | Codice fiscale del paziente           |
| _sort                 | Sì    | String          | onset-date, -onset-date           | Ordinamento                           |
| _count                | Sì    | integer         | max 10                            | Risultati per pagina                  |
| _revinclude           | Sì    | String          | Composition:entry                 | Includi Composition                   |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related         | Includi DocumentReference             |
| onset-date            | No    | array of String | Dinamico                          | Data di insorgenza (max 5 anni)       |

## 3.2 AllergyIntolerance

System ammessi per `code`: `2.16.840.1.113883.6.73` (WHO ATC), `2.16.840.1.113883.2.9.6.1.5` (AIC), `2.16.840.1.113883.11.22.9` (IPSNoAllergiesInfo).

### Dati clinici (Assistito)

`GET <BASE_PATH>/v1/assistito-consultazione-dati-clinici/AllergyIntolerance`

| Parametro             | Obbl. | Tipo            | Valori ammessi            | Descrizione                         |
| --------------------- | ----- | --------------- | ------------------------- | ----------------------------------- |
| code                  | Sì    | String          | `[SYSTEM]\|[CODE]`        | Codice allergia/intolleranza        |
| patient.identifier    | Sì    | String          | Dinamico                  | Codice fiscale del paziente         |
| _sort                 | Sì    | String          | date, -date               | Ordinamento                         |
| date                  | Sì    | array of String | Dinamico                  | Data (YYYY-MM-DD, max 5 anni)       |
| _revinclude           | Sì    | String          | Composition:entry         | Includi Composition                 |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related | Includi DocumentReference           |
| _count                | No    | integer         | max 10                    | Risultati per pagina                |

### Dossier farmaceutico (Assistito e Professionista)

`GET <BASE_PATH>/v1/assistito-consultazione-dati-dossier-farmaceutico/AllergyIntolerance`
`GET <BASE_PATH>/v1/professionista-consultazione-dati-dossier-farmaceutico/AllergyIntolerance`

| Parametro             | Obbl. | Tipo    | Valori ammessi            | Descrizione                 |
| --------------------- | ----- | ------- | ------------------------- | --------------------------- |
| patient.identifier    | Sì    | String  | Dinamico                  | Codice fiscale del paziente |
| _revinclude           | Sì    | String  | Composition:entry         | Includi Composition         |
| _revinclude:iterate   | Sì    | String  | DocumentReference:related | Includi DocumentReference   |
| _count                | No    | integer | max 10                    | Risultati per pagina        |

### Parametri clinici rilevanti (Professionista)

`GET <BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/AllergyIntolerance`

| Parametro             | Obbl. | Tipo    | Valori ammessi            | Descrizione                  |
| --------------------- | ----- | ------- | ------------------------- | ---------------------------- |
| code                  | Sì    | String  | `[SYSTEM]\|[CODE]`        | Codice allergia/intolleranza |
| patient.identifier    | Sì    | String  | Dinamico                  | Codice fiscale del paziente  |
| _sort                 | Sì    | String  | date, -date               | Ordinamento                  |
| _count                | Sì    | integer | max 10                    | Risultati per pagina         |
| _revinclude           | Sì    | String  | Composition:entry         | Includi Composition          |
| _revinclude:iterate   | Sì    | String  | DocumentReference:related | Includi DocumentReference    |
| date                  | No    | String  | Dinamico                  | Data (max 5 anni)            |

## 3.3 MedicationStatement

System ammessi per `code`: `2.16.840.1.113883.6.73` (ATC), `2.16.840.1.113883.2.9.6.1.5` (AIC), `2.16.840.1.113883.2.9.6.1.51` (GE).

### Dati clinici (Assistito)

`GET <BASE_PATH>/v1/assistito-consultazione-dati-clinici/MedicationStatement` — è obbligatorio valorizzare almeno uno tra `effective` e `_count`.

| Parametro             | Obbl. | Tipo    | Valori ammessi            | Descrizione                       |
| --------------------- | ----- | ------- | ------------------------- | --------------------------------- |
| code                  | Sì    | String  | `[SYSTEM]\|[CODE]`        | Codice del farmaco                |
| patient.identifier    | Sì    | String  | Dinamico                  | Codice fiscale del paziente       |
| _sort                 | Sì    | String  | effective, -effective     | Ordinamento                       |
| _revinclude           | Sì    | String  | Composition:entry         | Includi Composition               |
| _revinclude:iterate   | Sì    | String  | DocumentReference:related | Includi DocumentReference         |
| effective             | No    | String  | Dinamico                  | Data di efficacia (YYYY-MM-DD)    |
| _count                | No    | integer | max 10                    | Risultati per pagina              |

### Parametri clinici rilevanti (Professionista)

`GET <BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/MedicationStatement` — stessi parametri della variante Assistito, con `_count` obbligatorio ed `effective` limitato a 5 anni.

## 3.4 MedicationDispense

### Dati clinici (Assistito)

`GET <BASE_PATH>/v1/assistito-consultazione-dati-clinici/MedicationDispense` — è obbligatorio valorizzare almeno uno tra `whenhandedover` e `_count`.

| Parametro             | Obbl. | Tipo    | Valori ammessi                        | Descrizione                    |
| --------------------- | ----- | ------- | ------------------------------------- | ------------------------------ |
| code                  | Sì    | String  | `2.16.840.1.113883.2.9.6.1.5\|[Code]` | Codice AIC                     |
| patient.identifier    | Sì    | String  | Dinamico                              | Codice fiscale del paziente    |
| _sort                 | Sì    | String  | whenhandedover, -whenhandedover       | Ordinamento                    |
| _revinclude           | Sì    | String  | Composition:entry                     | Includi Composition            |
| _revinclude:iterate   | Sì    | String  | DocumentReference:related             | Includi DocumentReference      |
| whenhandedover        | No    | String  | Dinamico                              | Data di consegna (YYYY-MM-DD)  |
| _count                | No    | integer | max 10                                | Risultati per pagina           |

### Dossier farmaceutico (Assistito e Professionista)

`GET <BASE_PATH>/v1/assistito-consultazione-dati-dossier-farmaceutico/MedicationDispense`
`GET <BASE_PATH>/v1/professionista-consultazione-dati-dossier-farmaceutico/MedicationDispense`

È obbligatorio valorizzare almeno uno tra `whenhandedover` e `_count`.

| Parametro             | Obbl. | Tipo            | Valori ammessi                                                 | Descrizione                                  |
| --------------------- | ----- | --------------- | -------------------------------------------------------------- | -------------------------------------------- |
| patient.identifier    | Sì    | String          | Dinamico                                                       | Codice fiscale del paziente                  |
| _sort                 | Sì    | String          | whenhandedover, -whenhandedover                                | Ordinamento                                  |
| _include              | Sì    | array of String | MedicationDispense:medication, MedicationDispense:prescription | Includi risorse correlate                    |
| _revinclude           | Sì    | String          | Composition:entry                                              | Includi Composition                          |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related                                      | Includi DocumentReference                    |
| whenhandedover        | No    | array of String | Dinamico                                                       | Intervallo (geYYYY-MM-DD / leYYYY-MM-DD)     |
| _count                | No    | integer         | max 10                                                         | Risultati per pagina                         |

### Parametri clinici rilevanti (Professionista)

`GET <BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/MedicationDispense` — stessi parametri della variante Dati clinici (Assistito), con `_count` obbligatorio e `whenhandedover` limitato a 5 anni.

## 3.5 MedicationRequest

`GET <BASE_PATH>/v1/assistito-consultazione-dati-dossier-farmaceutico/MedicationRequest`
`GET <BASE_PATH>/v1/professionista-consultazione-dati-dossier-farmaceutico/MedicationRequest`

È obbligatorio valorizzare almeno uno tra `authoredon` e `_count`.

| Parametro             | Obbl. | Tipo            | Valori ammessi                                                                        | Descrizione                                 |
| --------------------- | ----- | --------------- | ------------------------------------------------------------------------------------- | ------------------------------------------- |
| patient.identifier    | Sì    | String          | Dinamico                                                                              | Codice fiscale del paziente                 |
| _sort                 | Sì    | String          | authoredon, -authoredon                                                               | Ordinamento                                 |
| _include              | Sì    | array of String | MedicationRequest:medication, MedicationRequest:requester, MedicationRequest:encounter | Includi risorse correlate                   |
| _include:iterate      | Sì    | array of String | Encounter:location, Location:organization                                             | Inclusioni iterative                        |
| _revinclude           | Sì    | String          | Composition:entry                                                                     | Includi Composition                         |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related                                                             | Includi DocumentReference                   |
| authoredon            | No    | array of String | Dinamico                                                                              | Intervallo (geYYYY-MM-DD / leYYYY-MM-DD)    |
| _count                | No    | integer         | max 10                                                                                | Risultati per pagina                        |

## 3.6 MedicationAdministration

`GET <BASE_PATH>/v1/assistito-consultazione-dati-dossier-farmaceutico/MedicationAdministration`
`GET <BASE_PATH>/v1/professionista-consultazione-dati-dossier-farmaceutico/MedicationAdministration`

È obbligatorio valorizzare almeno uno tra `effective-time` e `_count`.

| Parametro             | Obbl. | Tipo            | Valori ammessi                                                                                          | Descrizione                                           |
| --------------------- | ----- | --------------- | ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------- |
| patient.identifier    | Sì    | String          | Dinamico                                                                                                | Codice fiscale del paziente                           |
| _sort                 | Sì    | String          | effective-time, -effective-time                                                                         | Ordinamento                                           |
| _include              | Sì    | array of String | MedicationAdministration:medication, MedicationAdministration:context, MedicationAdministration:request | Includi risorse correlate                             |
| _revinclude           | Sì    | String          | Composition:entry                                                                                       | Includi Composition                                   |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related                                                                               | Includi DocumentReference                             |
| effective-time        | No    | array of String | Dinamico                                                                                                | Intervallo (geYYYY-MM-DD / leYYYY-MM-DD, max 5 anni)  |
| _count                | No    | integer         | max 10                                                                                                  | Risultati per pagina                                  |

## 3.7 Observation

System ammessi per `code`: `2.16.840.1.113883.6.1` o `http://loinc.org` (LOINC), `2.16.840.1.113883.6.103` (ICD-9-CM). Per i Parametri clinici rilevanti è ammesso anche `2.16.840.1.113883.2.9.2.30.4.1` (Nomenclatore tariffario Min./Reg.).

### Dati clinici (Assistito)

`GET <BASE_PATH>/v1/assistito-consultazione-dati-clinici/Observation` — è obbligatorio valorizzare almeno uno tra `date` e `_count`.

| Parametro             | Obbl. | Tipo            | Valori ammessi            | Descrizione                    |
| --------------------- | ----- | --------------- | ------------------------- | ------------------------------ |
| code                  | Sì    | String          | `[SYSTEM]\|[CODE]`        | Codice dell'osservazione       |
| patient.identifier    | Sì    | String          | Dinamico                  | Codice fiscale del paziente    |
| _sort                 | Sì    | String          | date, -date               | Ordinamento                    |
| _revinclude           | Sì    | String          | Composition:entry         | Includi Composition            |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related | Includi DocumentReference      |
| date                  | No    | array of String | Dinamico                  | Data (YYYY-MM-DD, max 5 anni)  |
| _count                | No    | integer         | max 10                    | Risultati per pagina           |

### Andamento dati clinici (Assistito e Professionista)

`GET <BASE_PATH>/v1/assistito-visualizzazione-andamento-dati-clinici/Observation` — intervallo di date pari a 3, 6 o 12 mesi.
`GET <BASE_PATH>/v1/professionista-visualizzazione-andamento-dati-clinici/Observation` — intervallo di date non superiore a 5 anni; con `_count=1` e `_sort=-date` restituisce l'ultimo dato disponibile.

| Parametro             | Obbl. | Tipo            | Valori ammessi            | Descrizione                                 |
| --------------------- | ----- | --------------- | ------------------------- | ------------------------------------------- |
| code                  | Sì    | String          | `[SYSTEM]\|[CODE]`        | Codice dell'osservazione                    |
| date                  | Sì    | array of String | Dinamico                  | Intervallo (geYYYY-MM-DD / leYYYY-MM-DD)    |
| patient.identifier    | Sì    | String          | Dinamico                  | Codice fiscale del paziente                 |
| _sort                 | Sì    | String          | date, -date               | Ordinamento                                 |
| _revinclude           | Sì    | String          | Composition:entry         | Includi Composition                         |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related | Includi DocumentReference                   |
| _count                | No    | integer         | max 10                    | Risultati per pagina                        |

### Parametri clinici rilevanti (Professionista)

`GET <BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/Observation` — stessi parametri della variante Dati clinici (Assistito), con `_count` obbligatorio e system code estesi (vedi sopra).

### Dettaglio sintesi eventi (Assistito e Professionista)

`GET <BASE_PATH>/v1/assistito-consultazione-dati-sintesi-eventi-dettaglio/Observation`
`GET <BASE_PATH>/v1/professionista-consultazione-dati-sintesi-eventi-dettaglio/Observation`

| Parametro             | Obbl. | Tipo   | Valori ammessi            | Descrizione                  |
| --------------------- | ----- | ------ | ------------------------- | ---------------------------- |
| encounter             | Sì    | String | Dinamico                  | Id dell'Encounter correlato  |
| patient.identifier    | Sì    | String | Dinamico                  | Codice fiscale del paziente  |
| _revinclude           | Sì    | String | Composition:entry         | Includi Composition          |
| _revinclude:iterate   | Sì    | String | DocumentReference:related | Includi DocumentReference    |
| code                  | No    | String | `[SYSTEM]\|[CODE]`        | Codice dell'osservazione     |

## 3.8 Procedure

`GET <BASE_PATH>/v1/assistito-consultazione-dati-clinici/Procedure`
`GET <BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/Procedure` (con `_count` obbligatorio e `date` facoltativo, max 5 anni)

| Parametro             | Obbl. | Tipo            | Valori ammessi                    | Descrizione                    |
| --------------------- | ----- | --------------- | --------------------------------- | ------------------------------ |
| code                  | Sì    | String          | `2.16.840.1.113883.6.104\|[Code]` | Codice ICD-9-CM procedura      |
| patient.identifier    | Sì    | String          | Dinamico                          | Codice fiscale del paziente    |
| _sort                 | Sì    | String          | date, -date                       | Ordinamento                    |
| date                  | Sì    | array of String | Dinamico                          | Data (YYYY-MM-DD, max 5 anni)  |
| _revinclude           | Sì    | String          | Composition:entry                 | Includi Composition            |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related         | Includi DocumentReference      |
| _count                | No    | integer         | max 10                            | Risultati per pagina           |

## 3.9 DiagnosticReport

`GET <BASE_PATH>/v1/assistito-consultazione-dati-clinici/DiagnosticReport` — è obbligatorio valorizzare almeno uno tra `date` e `_count`.
`GET <BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/DiagnosticReport` (con `_count` obbligatorio e `date` max 5 anni)

| Parametro             | Obbl. | Tipo    | Valori ammessi                  | Descrizione                  |
| --------------------- | ----- | ------- | ------------------------------- | ---------------------------- |
| code                  | Sì    | String  | `2.16.840.1.113883.6.1\|[Code]` | Codice LOINC del referto     |
| patient.identifier    | Sì    | String  | Dinamico                        | Codice fiscale del paziente  |
| _sort                 | Sì    | String  | date, -date                     | Ordinamento                  |
| _revinclude           | Sì    | String  | Composition:entry               | Includi Composition          |
| _revinclude:iterate   | Sì    | String  | DocumentReference:related       | Includi DocumentReference    |
| date                  | No    | String  | Dinamico                        | Data (YYYY-MM-DD)            |
| _count                | No    | integer | max 10                          | Risultati per pagina         |

## 3.10 Immunization

System ammessi per `vaccine-code`: `2.16.840.1.113883.2.9.6.1.5` (AIC), `2.16.840.1.113883.6.73` (ATC).

### Dati clinici (Assistito) e Vaccinazioni (Professionista)

`GET <BASE_PATH>/v1/assistito-consultazione-dati-clinici/Immunization`
`GET <BASE_PATH>/v1/professionista-consultazione-dati-vaccinazioni/Immunization` — ammette in più il parametro facoltativo `_include=Immunization:location`.

| Parametro             | Obbl. | Tipo            | Valori ammessi            | Descrizione                  |
| --------------------- | ----- | --------------- | ------------------------- | ---------------------------- |
| patient.identifier    | Sì    | String          | Dinamico                  | Codice fiscale del paziente  |
| vaccine-code          | Sì    | String          | `[SYSTEM]\|[CODE]`        | Codice del vaccino           |
| _sort                 | Sì    | String          | date, -date               | Ordinamento                  |
| _revinclude           | Sì    | String          | Composition:entry         | Includi Composition          |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related | Includi DocumentReference    |
| date                  | No    | array of String | Dinamico                  | Data (YYYY-MM-DD)            |
| _count                | No    | integer         | max 10                    | Risultati per pagina         |

### Dettaglio sintesi eventi (Assistito e Professionista)

`GET <BASE_PATH>/v1/assistito-consultazione-dati-sintesi-eventi-dettaglio/Immunization`
`GET <BASE_PATH>/v1/professionista-consultazione-dati-sintesi-eventi-dettaglio/Immunization`

| Parametro             | Obbl. | Tipo   | Valori ammessi            | Descrizione                  |
| --------------------- | ----- | ------ | ------------------------- | ---------------------------- |
| patient.identifier    | Sì    | String | Dinamico                  | Codice fiscale del paziente  |
| encounter             | Sì    | String | Dinamico                  | Id dell'Encounter            |
| _revinclude           | Sì    | String | Composition:entry         | Includi Composition          |
| _revinclude:iterate   | Sì    | String | DocumentReference:related | Includi DocumentReference    |

### Parametri clinici rilevanti (Professionista)

`GET <BASE_PATH>/v1/professionista-parametri-clinici-rilevanti/Immunization` — stessi parametri della variante Dati clinici, con `_count` obbligatorio e fisso a `1` e `date` limitato a 5 anni.

## 3.11 ImmunizationRecommendation

`GET <BASE_PATH>/v1/professionista-consultazione-dati-vaccinazioni/ImmunizationRecommendation`

| Parametro          | Obbl. | Tipo            | Valori ammessi                 | Descrizione                  |
| ------------------ | ----- | --------------- | ------------------------------ | ---------------------------- |
| patient.identifier | Sì    | String          | Dinamico                       | Codice fiscale del paziente  |
| _sort              | No    | String          | date, -date                    | Ordinamento                  |
| date               | No    | array of String | Dinamico                       | Data (max 5 anni)            |
| vaccine-type       | No    | String          | AIC, ATC (`[SYSTEM]\|[CODE]`)  | Tipo di vaccino              |
| _count             | No    | integer         | min 1, max 10, default 10      | Risultati per pagina         |

## 3.12 Encounter

### Sintesi eventi (Assistito e Professionista)

`GET <BASE_PATH>/v1/assistito-consultazione-dati-sintesi-eventi/Encounter`
`GET <BASE_PATH>/v1/professionista-consultazione-dati-sintesi-eventi/Encounter`

È obbligatorio valorizzare almeno uno tra `date` e `_count`.

| Parametro             | Obbl. | Tipo            | Valori ammessi                                                                             | Descrizione                    |
| --------------------- | ----- | --------------- | ------------------------------------------------------------------------------------------ | ------------------------------ |
| patient.identifier    | Sì    | String          | Dinamico                                                                                   | Codice fiscale del paziente    |
| _sort                 | Sì    | String          | date, -date                                                                                | Ordinamento                    |
| _revinclude           | Sì    | array           | Composition:entry                                                                          | Includi Composition            |
| _revinclude:iterate   | Sì    | String          | DocumentReference:related                                                                  | Includi DocumentReference      |
| _include              | Sì    | array of String | Encounter:location, Encounter:participant                                                  | Includi risorse correlate      |
| _include:iterate      | Sì    | array of String | Location:organization, PractitionerRole:practitioner, Organization:partof, Composition:author | Inclusioni iterative        |
| date                  | No    | String          | Dinamico                                                                                   | Data (YYYY-MM-DD, max 5 anni)  |
| _count                | No    | integer         | max 10                                                                                     | Risultati per pagina           |

### Ricovero/PS (Professionista)

`GET <BASE_PATH>/v1/professionista-consultazione-dati-ricovero-ps/Encounter`

| Parametro                                 | Obbl. | Tipo            | Valori ammessi                                                                             | Descrizione                          |
| ----------------------------------------- | ----- | --------------- | ------------------------------------------------------------------------------------------ | ------------------------------------ |
| class                                     | Sì    | array of String | EMER, IMP                                                                                  | Classe dell'Encounter                |
| date                                      | Sì    | array of String | Dinamico                                                                                   | Data (YYYY-MM-DD, max 5 anni)        |
| patient.identifier                        | Sì    | String          | Dinamico                                                                                   | Codice fiscale del paziente          |
| _sort                                     | Sì    | String          | date, -date                                                                                | Ordinamento                          |
| _revinclude                               | Sì    | array of String | Composition:entry, Composition:encounter, Condition:encounter                              | Includi risorse correlate            |
| _revinclude:iterate                       | Sì    | String          | DocumentReference:related                                                                  | Includi DocumentReference            |
| _include                                  | Sì    | array of String | Encounter:location, Encounter:participant                                                  | Includi risorse correlate            |
| _include:iterate                          | Sì    | array of String | Location:organization, PractitionerRole:practitioner, Organization:partof, Composition:author | Inclusioni iterative              |
| location.organization.identifier          | No    | String          | Dinamico                                                                                   | Filtro per struttura sanitaria       |
| _has:Observation:encounter:value-concept  | No    | String          | Dinamico                                                                                   | Filtro per valore di Observation     |
| _has:Condition:encounter:code             | No    | String          | Dinamico                                                                                   | Filtro per codice di Condition       |
| _count                                    | No    | integer         | max 10                                                                                     | Risultati per pagina                 |

### Prestazioni (Professionista)

`GET <BASE_PATH>/v1/professionista-consultazione-dati-prestazioni/Encounter`

| Parametro                               | Obbl. | Tipo            | Valori ammessi                                                                                   | Descrizione                                |
| --------------------------------------- | ----- | --------------- | ------------------------------------------------------------------------------------------------ | ------------------------------------------ |
| class                                   | Sì    | String          | AMB                                                                                              | Classe dell'Encounter                      |
| date                                    | Sì    | array of String | Dinamico                                                                                         | Data (YYYY-MM-DD, max 5 anni)              |
| patient.identifier                      | Sì    | String          | Dinamico                                                                                         | Codice fiscale del paziente                |
| _sort                                   | Sì    | String          | date, -date                                                                                      | Ordinamento                                |
| _revinclude                             | Sì    | array of String | Composition:entry, Composition:encounter, ServiceRequest:encounter, Condition:encounter          | Includi risorse correlate                  |
| _revinclude:iterate                     | Sì    | String          | DocumentReference:related                                                                        | Includi DocumentReference                  |
| _include                                | Sì    | array of String | Encounter:location, Encounter:participant                                                        | Includi risorse correlate                  |
| _include:iterate                        | Sì    | array of String | Location:organization, PractitionerRole:practitioner, Organization:partof, Composition:author    | Inclusioni iterative                       |
| _has:ServiceRequest:encounter:category  | Sì    | String          | `[System]\|[COD_BRANCA]`                                                                         | Filtro per categoria di ServiceRequest     |
| _count                                  | No    | integer         | max 10                                                                                           | Risultati per pagina                       |

## 3.13 ImagingStudy

`GET <BASE_PATH>/v1/assistito-consultazione-dati-sintesi-eventi-dettaglio/ImagingStudy`
`GET <BASE_PATH>/v1/professionista-consultazione-dati-sintesi-eventi-dettaglio/ImagingStudy`

| Parametro             | Obbl. | Tipo   | Valori ammessi            | Descrizione                  |
| --------------------- | ----- | ------ | ------------------------- | ---------------------------- |
| patient.identifier    | Sì    | String | Dinamico                  | Codice fiscale del paziente  |
| encounter             | Sì    | String | Dinamico                  | Id dell'Encounter            |
| _revinclude           | Sì    | String | Composition:entry         | Includi Composition          |
| _revinclude:iterate   | Sì    | String | DocumentReference:related | Includi DocumentReference    |

## 3.14 Location

`GET <BASE_PATH>/v1/professionista-consultazione-dati-ricovero-ps/Location` — restituisce strutture e reparti associati a Encounter di ricovero o pronto soccorso.

| Parametro                                    | Obbl. | Tipo            | Valori ammessi            | Descrizione                        |
| -------------------------------------------- | ----- | --------------- | ------------------------- | ---------------------------------- |
| _has:Encounter:location:patient.identifier   | Sì    | String          | Dinamico                  | Codice fiscale del paziente        |
| _has:Encounter:location:class                | Sì    | String          | Dinamico                  | Classe dell'Encounter associato    |
| _include                                     | Sì    | array of String | Location:organization     | Includi Organization               |
| _revinclude                                  | Sì    | String          | Composition:entry         | Includi Composition                |
| _revinclude:iterate                          | Sì    | String          | DocumentReference:related | Includi DocumentReference          |
| _count                                       | No    | integer         | max 10                    | Risultati per pagina               |

## 3.15 AuditEvent

`GET <BASE_PATH>/v1/assistito-consultazione-dati-accesso/AuditEvent` — eventi di accesso ai dati dell'assistito. È obbligatorio valorizzare almeno uno tra `date` e `_count`.

| Parametro          | Obbl. | Tipo            | Valori ammessi | Descrizione                    |
| ------------------ | ----- | --------------- | -------------- | ------------------------------ |
| patient.identifier | Sì    | String          | Dinamico       | Codice fiscale del paziente    |
| _sort              | Sì    | String          | date, -date    | Ordinamento                    |
| entity             | No    | String          | Dinamico       | Entità coinvolta nell'evento   |
| date               | No    | array of String | Dinamico       | Data (YYYY-MM-DD)              |
| _count             | No    | integer         | max 10         | Risultati per pagina           |