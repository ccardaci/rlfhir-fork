<html>
  <head>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
    <script>
      $(document).ready(function () {
        $("#myInput").on("keyup", function () {
          var value = $(this).val().toLowerCase();
          $("#myTable tr").filter(function () {
            $(this).toggle($(this).text().toLowerCase().indexOf(value) > -1);
          });
        });
      });
    </script>
  </head>
  <body>
    <h1>Raccolta esempi</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolti tutti gli esempi creati per il progetto.
        <br />
        Usare la casella di ricerca sottostante per filtrare le informazioni
        desiderate.
      </p>
      <input id="myInput" type="text" placeholder="Cerca.." />
    </div>
    <br/>
    <table style="width: fit-content">
  <thead>
    <tr>
      <th>Tag</th>
      <th>ResourceType</th>
      <th>Descrizione</th>
      <th>Link Simplifier</th>
    </tr>
  </thead>
  <tbody id="myTable">
    <tr>
      <td>C-DOM</td>
      <td>Bundle</td>
      <td>Ricerca prestazioni erogate</td>
      <td>{{link:Bundle/esempio-ricerca-prestazioni-erogate}}</td>
    </tr>
    <tr>
      <td>C-DOM</td>
      <td>Bundle</td>
      <td>Ricerca progetti individuali attivi</td>
      <td>{{link:Bundle/esempio-ricerca-pi-attivi}}</td>
    </tr>
    <tr>
      <td>C-DOM</td>
      <td>Bundle</td>
      <td>Ricerca rivalutazioni e sospensioni</td>
      <td>{{link:Bundle/esempio-ricerca-rivalutazioni-sospensioni}}</td>
    </tr>
    <tr>
      <td>C-DOM</td>
      <td>Bundle</td>
      <td>Ricerca rivalutazioni</td>
      <td>{{link:Bundle/esempio-ricerca-rivalutazioni}}</td>
    </tr>
    <tr>
      <td>C-DOM</td>
      <td>Bundle</td>
      <td>Ricerca sospensioni</td>
      <td>{{link:Bundle/esempio-ricerca-sospensione}}</td>
    </tr>
    <tr>
      <td>C-DOM</td>
      <td>Bundle</td>
      <td>Ricerca storico progetti individuali</td>
      <td>{{link:Bundle/esempio-ricerca-storico-pi}}</td>
    </tr>
    <tr>
      <td>C-DOM</td>
      <td>Bundle</td>
      <td>Ricerca valutazioni</td>
      <td>{{link:Bundle/esempio-ricerca-valutazioni}}</td>
    </tr>
    <tr>
      <td>C-DOM</td>
      <td>Bundle</td>
      <td>Ricerca enti erogatori accreditati ambito territoriale ASST tipo C-DOM</td>
      <td>{{link:Bundle/esempio-RicercaEntiErogatoriAccreditatiAmbitoTerritorialeASST-CDOM}}</td>
    </tr>
    <tr>
      <td>C-DOM</td>
      <td>Patient</td>
      <td>Esempio del profilo RLPatientCittadino</td>
      <td>{{link:Patient/esempio-Patient-Cittadino}}</td>
    </tr>
    <tr>
      <td>C-DOM</td>
      <td>PractitionerRole</td>
      <td>Esempio del profilo RLPractitionerRoleOperatoreADI</td>
      <td>{{link:PractitionerRole/esempio-PractitionerRole-OperatoreADI}}</td>
    </tr>
    <tr>
      <td>DDC</td>
      <td>Organization</td>
      <td>Esempio del profilo RLOrganizationL1</td>
      <td>{{link:Organization/esempio-RLOrganizationL1}}</td>
    </tr>
    <tr>
      <td>DDC</td>
      <td>Organization</td>
      <td>Esempio del profilo RLOrganizationL2</td>
      <td>{{link:Organization/esempio-RLOrganizationL2}}</td>
    </tr>
    <tr>
      <td>DDC</td>
      <td>Organization</td>
      <td>Esempio del profilo RLOrganizationL3</td>
      <td>{{link:Organization/esempio-RLOrganizationL3}}</td>
    </tr>
    <tr>
      <td>DDC</td>
      <td>Practitioner</td>
      <td>Esempio del profilo Practitioner</td>
      <td>{{link:Practitioner/esempio-Practitioner}}</td>
    </tr>
    <tr>
      <td>DDC</td>
      <td>PractitionerRole</td>
      <td>Esempio del profilo PractitionerRole</td>
      <td>{{link:PractitionerRole/esempio-PractitionerRole}}</td>
    </tr>
    <tr>
      <td>Errori</td>
      <td>Bundle</td>
      <td>
        Esempio di messaggio di notifica errore di coerenza in caso di ricerca
        tramite parametri
      </td>
      <td>{{link:Bundle/esempio-bundle-notifica-errori-bundle}}</td>
    </tr>
    <tr>
      <td>Errori</td>
      <td>Bundle</td>
      <td>
        Esempio di messaggio di notifica errore di coerenza in caso di ricerca
        tramite ID
      </td>
      <td>{{link:Bundle/esempio-bundle-notifica-errori-resource}}</td>
    </tr>
    <tr>
      <td>Errori, C-DOM</td>
      <td>OperationOutcome</td>
      <td>OperationOutcome: parametro non supportato</td>
      <td>{{link:OperationOutcome/esempio-searchfail}}</td>
    </tr>
    <tr>
      <td>Errori, C-DOM</td>
      <td>OperationOutcome</td>
      <td>OperationOutcome: eccezione generica</td>
      <td>{{link:OperationOutcome/esempio-exception}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>CarePlan</td>
      <td>Esempio del profilo RLCarePlanProgettoIndividuale</td>
      <td>{{link:CarePlan/esempio-CarePlan-Progetto-Individuale}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>CareTeam</td>
      <td>Esempio del profilo RLCareTeamTeamEquipe</td>
      <td>{{link:CareTeam/esempio-CareTeam-Equipe}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>Condition</td>
      <td>
        Esempio del profilo RLConditionProblemiSalute - Patologia Primaria
      </td>
      <td>{{link:Condition/esempio-Condition-PatologiaPrimaria}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>Condition</td>
      <td>
        Esempio del profilo RLConditionProblemiSalute - Condizione Clinica
        Prevalente
      </td>
      <td>{{link:Condition/esempio-Condition-CondizioneClinicaPrevalente}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>Condition</td>
      <td>
        Esempio del profilo RLConditionProblemiSalute - Problema Infermieristico
      </td>
      <td>{{link:Condition/esempio-Condition-ProblemaInfermieristico}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>DeviceRequest</td>
      <td>Esempio del profilo RLDeviceRequestProtesiAusili</td>
      <td>{{link:DeviceRequest/esempio-DeviceRequest-ProtesiAusili}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>Encounter</td>
      <td>Esempio del profilo RLEncounterEncounterAccesso</td>
      <td>{{link:Encounter/esempio-Encounter-Accesso}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>Goal</td>
      <td>Esempio del profilo RLGoalObiettiviSalute</td>
      <td>{{link:Goal/esempio-Goal-ObiettiviSalute}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>Location</td>
      <td>Esempio del profilo RLLocationLuogoPrestazioneCureDom</td>
      <td>{{link:Location/esempio-Location-LuogoPrestazioneCureDom}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>MedicationRequest</td>
      <td>Esempio del profilo RLMedicationRequestTerapiaFarmacologica</td>
      <td>
        {{link:MedicationRequest/esempio-MedicationRequest-TerapiaFarmacologica}}
      </td>
    </tr>
    <tr>
      <td>PI</td>
      <td>MedicationRequest</td>
      <td>Esempio del profilo RLMedicationRequestRequestOssigenoterapia</td>
      <td>
        {{link:MedicationRequest/esempio-MedicationRequest-Ossigenoterapia}}
      </td>
    </tr>
    <tr>
      <td>PI</td>
      <td>Observation</td>
      <td>Esempio del profilo RLObservationEsitoValutazione (scheda triage)</td>
      <td>{{link:Observation/esempio-Observation-EsitoValutazione-triage}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>Observation</td>
      <td>Esempio del profilo RLObservationEsitoValutazione (interRAI)</td>
      <td>
        {{link:Observation/esempio-Observation-EsitoValutazione-interRAI}}
      </td>
    </tr>
    <tr>
      <td>PI</td>
      <td>Practitioner</td>
      <td>Esempio del profilo RLPractitionerProfessionistaSanitario</td>
      <td>
        {{link:Practitioner/esempio-Practitioner-ProfessionistaSanitario}}
      </td>
    </tr>
    <tr>
      <td>PI</td>
      <td>PractitionerRole</td>
      <td>Esempio del profilo RLPractitionerRoleProfessionistaSanitario</td>
      <td>
        {{link:PractitionerRole/esempio-PractitionerRole-ProfessionistaSanitario}}
      </td>
    </tr>
    <tr>
      <td>PI</td>
      <td>Procedure</td>
      <td>Esempio del profilo RLProcedurePrestazione</td>
      <td>{{link:Procedure/esempio-Procedure-Prestazione}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>ServiceRequest</td>
      <td>Esempio del profilo RLServiceRequestInterventoEducazionale</td>
      <td>
        {{link:ServiceRequest/esempio-ServiceRequest-InterventoEducazionale}}
      </td>
    </tr>
    <tr>
      <td>PI</td>
      <td>ServiceRequest</td>
      <td>Esempio del profilo RLServiceRequestPrestazioniInfermieristiche</td>
      <td>
        {{link:ServiceRequest/esempio-ServiceRequest-PrestazioniInfermieristiche}}
      </td>
    </tr>
    <tr>
      <td>PI</td>
      <td>ServiceRequest</td>
      <td>Esempio del profilo RLServiceRequestPrestazioniSpecialistiche</td>
      <td>
        {{link:ServiceRequest/esempio-ServiceRequest-PrestazioniSpecialistiche}}
      </td>
    </tr>
    <tr>
      <td>PI</td>
      <td>ServiceRequest</td>
      <td>Esempio del profilo RLServiceRequestRivalutazione</td>
      <td>{{link:ServiceRequest/esempio-ServiceRequest-Rivalutazione}}</td>
    </tr>
    <tr>
      <td>PI</td>
      <td>ServiceRequest</td>
      <td>Esempio del profilo RLServiceRequestServiziSocioAssistenziali</td>
      <td>
        {{link:ServiceRequest/esempio-ServiceRequest-ServiziSocioAssistenziali}}
      </td>
    </tr>
    <tr>
      <td>PI</td>
      <td>ServiceRequest</td>
      <td>Esempio del profilo RLServiceRequestSospensioneADI</td>
      <td>{{link:ServiceRequest/esempio-ServiceRequest-SospensioneADI}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Bundle</td>
      <td>Esempio dei posti letto occupati (risorsa Location)</td>
      <td>{{link:Bundle/esempio-PLO-Location}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Location</td>
      <td>Esempio del profilo RLLocationPLOEdificio</td>
      <td>{{link:Location/esempio-Location-PLO-Edificio}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Location</td>
      <td>Esempio del profilo RLLocationPLOLetto</td>
      <td>{{link:Location/esempio-Location-PLO-Letto}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Location</td>
      <td>Esempio del profilo RLLocationPLOPiano</td>
      <td>{{link:Location/esempio-Location-PLO-Piano}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Location</td>
      <td>Esempio del profilo RLLocationPLOStanza</td>
      <td>{{link:Location/esempio-Location-PLO-Stanza}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>Measure</td>
      <td>Esempio del profilo RLMeasurePLO</td>
      <td>{{link:Measure/esempio-measure-PLO}}</td>
    </tr>
    <tr>
      <td>PLO</td>
      <td>MeasureReport</td>
      <td>Esempio del profilo RLMeasureReportPLO</td>
      <td>{{link:MeasureReport/esempio-measureReport-PLO}}</td>
    </tr>
    <tr>
      <td>PIC</td>
      <td>Bundle</td>
      <td>Esempio Bundle di attivazione dei servizi di presa in carico dei pazienti cronici da parte del MMG</td>
      <td>{{link:RLBundleMMGpicMMG}}</td>
    </tr>
    <tr>
      <td>PIC</td>
      <td>Bundle</td>
      <td>Esempio RLBundleMOST per una valutazione di dimissioni protette con due allegati</td>
      <td>{{link:Examples/Example_RL_Bundle_MOST_DimissioniProtette.json}}</td>
    </tr>
    <tr>
      <td>PIC</td>
      <td>Bundle</td>
      <td>Esempio Bundle Risposta del messaggio con esito positivo</td>
      <td>{{link:Bundle/RLBundleRispostaMMGPositiva}}</td>
    </tr>
    <tr>
      <td>PIC</td>
      <td>Bundle</td>
      <td>Esempio Bundle Risposta del messaggio con errore</td>
      <td>{{link:Bundle/RLBundleRispostaMMGNegativa}}</td>
    </tr>
        <tr>
      <td>PIC</td>
      <td>Patient</td>
      <td>Esempio profilo RLPatientBase</td>
      <td>{{link:esempio-patient-base}}</td>
    </tr>
            <tr>
      <td>PIC</td>
      <td>MedicationRequest</td>
      <td>Esempio profilo RLMedicationRequestTerapiaFarmacologica</td>
      <td>{{link:esempio-medicationRequest-TerapiaFarmacologica-PIC}}</td>
    </tr>
     <tr>
      <td>PIC</td>
      <td>Condition</td>
      <td>Esempio profilo RLConditionProblemiSalute</td>
      <td>{{link:esempio-condition-problemiSalute-PIC}}</td>
    </tr>
         <tr>
      <td>PIC</td>
      <td>OperationOutcome</td>
      <td>Esempio profilo RLOperationOutcomeMMG risposta positiva</td>
      <td>{{link:Examples/Example_RL_OperationOutcomeMMG_Positiva.json}}</td>
    </tr>
         <tr>
      <td>PIC</td>
      <td>OperationOutcome</td>
      <td>Esempio profilo RLOperationOutcomeMMG risposta negativa</td>
      <td>{{link:Examples/Example_RL_OperationOutcomeMMG_Negativa.json}}</td>
    </tr>
    <tr>
      <td>PIC</td>
      <td>MessageHeader</td>
      <td>Esempio profilo RLMessageHeaderMMG risposta negativa</td>
      <td>{{link:Examples/Example_RLMessageHeaderMMG_negativa.json}}</td>
    </tr>
    <tr>
      <td>PIC</td>
      <td>MessageHeader</td>
      <td>Esempio profilo RLMessageHeaderMMG risposta positiva</td>
      <td>{{link:Examples/Example_RLMessageHeaderMMG_positiva.json}}</td>
    </tr>
    <tr>
      <td>PIC</td>
      <td>MessageHeader</td>
      <td>Esempio profilo RLMessageHeaderMMG MMGpicMMG</td>
      <td>{{link:Examples/Example_RLMessageHeaderMMG_MMGpicMMG.json}}</td>
    </tr>
    <tr>
      <td>NEA</td>
      <td>Bundle</td>
      <td>Esempio Bundle di richiesta inviato dall'applicativo di gestione 116117 NEA a SGDT</td>
      <td>{{link:Examples/Example_Bundle_NEA.json}}</td>
    </tr>
    <tr>
      <td>NEA</td>
      <td>Bundle</td>
      <td>Esempio Bundle Risposta del messaggio con esito positivo</td>
      <td>{{link:Examples/Example_Bundle_Risposta_NEA_ok.json}}</td>
    </tr>
    <tr>
      <td>NEA</td>
      <td>Bundle</td>
      <td>Esempio Bundle Risposta del messaggio con errore</td>
      <td>{{link:Examples/Example_Bundle_Risposta_NEA_ko.json}}</td>
    </tr>
    <tr>
      <td>NEA</td>
      <td>Bundle</td>
      <td>Esempio Bundle di stato con richiesta attiva</td>
      <td>{{link:Examples/Example_Bundle_StatoNEA_attiva.json}}</td>
    </tr>
    <tr>
      <td>NEA</td>
      <td>Bundle</td>
      <td>Esempio Bundle di stato con richiesta chiusa</td>
      <td>{{link:Examples/Example_Bundle_StatoNEA_chiusa.json}}</td>
    </tr>
    <tr>
      <td>NEA</td>
      <td>OperationOutcome</td>
      <td>Esempio profilo RLOperationOutcomeNEA risposta positiva</td>
      <td>{{link:Examples/Example_RL_OperationOutcomeNEA_Positiva.json}}</td>
    </tr>
    <tr>
      <td>NEA</td>
      <td>OperationOutcome</td>
      <td>Esempio profilo RLOperationOutcomeNEA risposta negativa</td>
      <td>{{link:Examples/Example_RL_OperationOutcomeNEA_Negativa.json}}</td>
    </tr>
    <tr>
      <td>NEA</td>
      <td>MessageHeader</td>
      <td>Esempio profilo RLMessageHeaderNEA risposta positiva</td>
      <td>{{link:Examples/Example_RLMessageHeaderNEA_positiva.json}}</td>
    </tr>
    <tr>
      <td>NEA</td>
      <td>MessageHeader</td>
      <td>Esempio profilo RLMessageHeaderNEA risposta negativa</td>
      <td>{{link:Examples/Example_RLMessageHeaderNEA_negativa.json}}</td>
    </tr>
    <tr>
      <td>NEA</td>
      <td>DocumentReference</td>
      <td>Esempio del profilo RLDocumentReferenceDocumento</td>
      <td>{{link:Examples/Example_RL_DocumentReference_Documento.json}}</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
