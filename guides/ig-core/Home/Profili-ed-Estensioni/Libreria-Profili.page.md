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
    <h1>Raccolta profili in uso</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolti tutti i profili attivi; ad ogni
        profilo è associato un tema di utilizzo (si veda la pagina
        {{pagelink:Home/Contesto/Panoramica-di-progetto.page.md}}).
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
          <th>Tag</th>
          <th>Nome profilo e pagina di dettaglio</th>
          <th>Risorsa base</th>
          <th>Descrizione</th>
          <th>Link Simplifier</th>
        </tr>
      </thead>
      <tbody id="myTable">
       <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLAllergyIntoleranceCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/allergyintolerance.html">AllergyIntolerance</a>
          </td>
          <td>
            Profilo che descrive le allergie e le intolleranze
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntoleranceCore}}
          </td>
        </tr>
       <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLConditionProblem.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/condition.html">Condition</a>
          </td>
          <td>
            Profilo che descrive le patologie di un paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCore}}
          </td>
        </tr>
       <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLEncounterCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/encounter.html">Encounter</a>
          </td>
          <td>
            Profilo che descrive gli episodi clinici
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterCore}}
          </td>
        </tr>     
       <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLFamMembHistCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/familymemberhistory.html">FamilyMemberHistory</a>
          </td>
          <td>
            Profilo che descrive l'anamnesi familiare
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLFamilyMemberHistoryCore}}
          </td>
        </tr>     
        <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLLocationCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/location.html">Location</a>
          </td>
          <td>
            Profilo che descrive una struttura fisica 
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationCore}}
          </td>    
        </tr>           
        <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationPrecedentiEsami.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive i precedenti esami eseguiti
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCorePrecedentiEsamiEseguiti}}
          </td>    
        </tr>          
        <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDecorsoClinico.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive il decorso clinico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCoreDecorsoClinico}}
          </td>    
        </tr>      
        <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/organization.html">Organization</a>
          </td>
          <td>
            Profilo che descrive un'azienda
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationCore}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPatientCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/patient.html">Patient</a>
          </td>
          <td>
            Profilo che descrive un paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPatientCore}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/practitioner.html">Practitioner</a>
          </td>
          <td>
            Profilo che descrive un operatore sanitario
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerCore}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLPractitionerRoleCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/practitionerrole.html">PractitionerRole</a>
          </td>
          <td>
            Profilo che descrive il ruolo associato ad un operatore sanitario e la struttura a cui afferisce
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLPractitionerRoleCore}}
          </td>
        </tr>   
        <tr>
          <td>CORE</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestCore.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/organization.html">ServiceRequest</a>
          </td>
          <td>
            Profilo che descrive una richiesta
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestCore}}
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
