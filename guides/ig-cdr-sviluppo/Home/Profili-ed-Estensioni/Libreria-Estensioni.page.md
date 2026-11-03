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
    <h1>Raccolta estensioni in uso</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolte tutte le estensioni sviluppate
        per i profili del progetto.
        <br />
        Usare la casella di ricerca sottostante per filtrare le informazioni
        desiderate.
      </p>
      <input id="myInput" type="text" placeholder="Cerca.." />
    </div>
    <br />
    <table style="width: fit-content">
      <thead>
        <tr>
          <th>Nome estensione</th>
          <th>Base</th>
          <th>Descrizione</th>
          <th>Link simplifier</th>
        </tr>
      </thead>
      <tbody id="myTable">        
      <tr>
          <td>dataEnterer</td>
          <td>Composition</td>
          <td>Persona o dispositivo che trasforma un testo dettato nel documento FHIR</td>
          <td>
            {{link:http://hl7.it/fhir/StructureDefinition/composition-dataenterer-it}}
          </td>
        </tr>
        <tr>
          <td>information-recipient</td>
          <td>Composition</td>
          <td>Professionisti sanitari che ricevono una copia del documento (es. MMG/PLS)</td>
          <td>
            {{link:http://hl7.eu/fhir/StructureDefinition/information-recipient}}
          </td>
        </tr>
        <tr>
          <td>basedOnOrderOrRequisition</td>
          <td>Composition</td>
          <td>Richiesta che ha determinato la produzione del documento (ricetta, CUP, ordine interno, accession number, studio DICOM)</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLBasedOnOrderOrRequisition}}
          </td>
        </tr>
        <tr>
          <td>versionNumber</td>
          <td>Composition</td>
          <td>Identificatore specifico della versione della composizione, assegnato quando ciascuna versione viene creata o aggiornata</td>
          <td>
            {{link:http://hl7.org/fhir/StructureDefinition/composition-clinicaldocument-versionNumber}}
          </td>
        </tr>
        <tr>
          <td>StrutturaImpianto</td>
          <td>DeviceUseStatement</td>
          <td>Rappresenta la struttura sanitaria che ha effettuato l'impianto del dispositivo.</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceUseStatementStrutturaImpianto}}
          </td>
        </tr>
        <tr>
          <td>dataChiusura</td>
          <td>CarePlan</td>
          <td>Data di chiusura della programmazione del Piano Assistenziale Individuale</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanDataChiusura}}
          </td>
        </tr>
        <tr>
          <td>validitaBisogno</td>
          <td>ServiceRequest</td>
          <td>Validità del bisogno della prestazione programmata nel Piano Assistenziale Individuale</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestValiditaBisogno}}
          </td>
        </tr>
        <tr>
          <td>intervalloTemporale</td>
          <td>ServiceRequest</td>
          <td>Intervallo temporale (data inizio e data fine) della prestazione programmata nel Piano Assistenziale Individuale</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestIntervalloTemporale}}
          </td>
        </tr>
        <tr>
          <td>flagProtesica</td>
          <td>DeviceRequest</td>
          <td>Flag protesica della richiesta di protesi o ausili nel Piano Assistenziale Individuale</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestFlagProtesica}}
          </td>
        </tr>
                <tr>
          <td>RLCarePlanFlagPrescrizione</td>
          <td>CarePlan</td>
          <td>Flag prescrizione del piano terapeutico (dizionario Flag Prescrizione)</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanFlagPrescrizione}}
          </td>
        </tr>
        <tr>
          <td>RLCarePlanFlagModificaPrescrizione</td>
          <td>CarePlan</td>
          <td>Flag modifica prescrizione del piano terapeutico (dizionario Flag Modifica Prescrizione)</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanFlagModificaPrescrizione}}
          </td>
        </tr>
        <tr>
          <td>RLCarePlanMotivoProsecuzione</td>
          <td>CarePlan</td>
          <td>Motivo della prosecuzione del piano terapeutico (testo libero)</td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanMotivoProsecuzione}}
          </td>
        </tr>
                <tr>
          <td>information-recipient</td>
          <td>Composition</td>
          <td>Professionisti sanitari che ricevono una copia del documento</td>
          <td>
            {{link:http://hl7.eu/fhir/StructureDefinition/information-recipient}}
          </td>
        </tr>
        <tr>
          <td>composition-clinicaldocument-versionNumber</td>
          <td>Composition</td>
          <td>Versione del documento</td>
          <td>
            {{link:http://hl7.org/fhir/StructureDefinition/composition-clinicaldocument-versionNumber}}
          </td>
        </tr>
        <tr>
          <td>composition-dataenterer-it</td>
          <td>Composition</td>
          <td>Persona che ha trascritto il documento</td>
          <td>
            {{link:http://hl7.it/fhir/StructureDefinition/composition-dataenterer-it}}
          </td>
        </tr>
        </tbody>
    </table>
  </body>
</html>
