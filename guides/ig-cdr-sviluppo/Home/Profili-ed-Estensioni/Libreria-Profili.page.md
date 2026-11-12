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
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlallergyintolerancecore.page.md?version=current">
            RLAllergyIntoleranceCore
      </a>
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
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionRAD.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
          </td>
          <td>
            Profilo che descrive header e body di un documento di radiologia
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionRefertoRadiologia}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlconditioncore.page.md?version=current">
          RLConditionCore
      </a>
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
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlencountercore.page.md?version=current">RLEncounterCore</a>
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
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlfammembhistcore.page.md?version=current">
            RLFamilyMemberHistoryCore
      </a>
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
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLImagingStudyRAD.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/imagingstudy.html">ImagingStudy</a>
          </td>
          <td>
            Profilo che descrive studi dicom
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImagingStudyRAD}}
          </td>
        </tr>
        <tr>
          <td>CORE</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rllocationcore.page.md?version=current">
          RLLocationCore
      </a>
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/location.html">Location</a>
          </td>
          <td>
            Profilo che descrive una struttura fisica per il contesto di Regione Lombardia
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLLocationCore}}
          </td>
        </tr>
        <tr>
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationStatementRAD.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationstatement.html">MedicationStatement</a>
          </td>
          <td>
            Profilo che descrive le terapie del paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationStatementTerapiaFarmacologica}}
          </td>
        </tr>
        <tr>
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationQuesitoDiagnosticoRad.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive il quesito diagnostico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationQuesitoDiagnostico}}
          </td>
        </tr>
        <tr>
          <td>CORE,RAD</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlobservationdecorsoclinico.page.md?version=current">
            RLObservationDecorsoClinico
      </a>
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive il decorso clinico per radiologia
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCoreDecorsoClinico}}
          </td>
        </tr>
        <tr>
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationComplicanzeRad.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive le complicanze
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationComplicanzeRad}}
          </td>
        </tr>
        <tr>
          <td>RAD</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationPrecedentiEsamiEseguitiRad.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive i precedenti esami eseguiti
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRad}}
          </td>
        </tr>
 <td>RAD</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLImagingStudyRad.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/imagingstudy.html">ImagingStudy</a>
 </td>
 <td>
 Profilo che descrive lo studio DICOM associato al referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImagingStudyRad}}
 </td>
</tr>
<tr>
 <td>RAD</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationEsameEseguitoRad.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive l'esame eseguito nel contesto del referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationEsameEseguitoRad}}
 </td>
</tr>
<tr>
 <td>RAD</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationComplicanzeRad.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive le complicanze nel contesto del referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationComplicanzeRad}}
 </td>
</tr>
<tr>
 <td>RAD</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationPrecedentiEsamiEseguitiRad.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive i precedenti esami eseguiti nel contesto del referto di radiologia
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRad}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
 </td>
 <td>
 Profilo che descrive il documento Piano Terapeutico Individuale
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCarePlanPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/careplan.html">CarePlan</a>
 </td>
 <td>
 Profilo che descrive il Piano Terapeutico Individuale: scadenza, flag di prescrizione e condizioni cliniche
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLConditionCondizioniErogabilitaPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/condition.html">Condition</a>
 </td>
 <td>
 Profilo che descrive una condizione di erogabilità del piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCondizioniErogabilitaPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLConditionCriteriEsclusionePti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/condition.html">Condition</a>
 </td>
 <td>
 Profilo che descrive un criterio di esclusione del piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionCriteriEsclusionePti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationPesoPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive il peso del paziente nel piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPesoPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDurataMalattiaPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive la durata della malattia (BPCO) nel piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDurataMalattiaPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
 </td>
 <td>
 Profilo che descrive il programma terapeutico del piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPti}}
 </td>
</tr>
<tr>
 <td>PTI</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationPti.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/medication.html">Medication</a>
 </td>
 <td>
 Profilo che descrive il farmaco prescritto nel piano terapeutico
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationPti}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
 </td>
 <td>
 Profilo che descrive il documento lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationAdministrationRicoveroLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/medicationadministration.html">MedicationAdministration</a>
 </td>
 <td>
 Profilo che descrive la terapia farmacologica somministrata durante il ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationAdministrationRicoveroLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestDimissioneLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
 </td>
 <td>
 Profilo che descrive la terapia farmacologica alla dimissione nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestDimissioneLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestRicoveroLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
 </td>
 <td>
 Profilo che descrive la terapia farmacologica prescritta durante il ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestRicoveroLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationComplicanzeLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive le complicanze nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationComplicanzeLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationConsulenzaLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive la consulenza nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationConsulenzaLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDecorsoClinicoLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive il decorso clinico nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDecorsoClinicoLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDiagnosiDimissioneLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive la diagnosi alla dimissione nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDiagnosiDimissioneLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationEsamiEseguitiRicoveroLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive gli esami eseguiti durante il ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationEsamiEseguitiRicoveroLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationMotivoRicoveroLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive il motivo del ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationMotivoRicoveroLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationProcedureRicoveroLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
 </td>
 <td>
 Profilo che descrive le procedure durante il ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationProcedureRicoveroLdo}}
 </td>
</tr>
<tr>
 <td>LDO</td>
 <td>
 {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLProcedureLdo.page.md}}
 </td>
 <td>
 <a href="http://hl7.org/fhir/R4/procedure.html">Procedure</a>
 </td>
 <td>
 Profilo che descrive le procedure eseguite durante il ricovero nel contesto della lettera di dimissione ospedaliera
 </td>
 <td>
 {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedureLdo}}
 </td>
</tr>
        <tr>
          <td>CORE</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlservicerequestcore.page.md?version=current">
            RLServiceRequestCore
          </a>
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
          </td>
          <td>
            Profilo che descrive una richiesta
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestCore}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCarePlanPianoCuraDimissioneVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/careplan.html">CarePlan</a>
          </td>
          <td>
            Profilo che descrive il piano di cura alla dimissione dal Pronto Soccorso
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
          </td>
          <td>
            Profilo che descrive header e body del Verbale di Pronto Soccorso
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationAdministrationTerapiaFarmacoInPSVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationadministration.html">MedicationAdministration</a>
          </td>
          <td>
            Profilo che descrive la terapia farmacologica somministrata in Pronto Soccorso
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationAdministrationVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestTerapiaFarmacoDimissioneVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
          </td>
          <td>
            Profilo che descrive la richiesta di terapia farmacologica in Pronto Soccorso
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestTerapiaPSVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestTerapiaFarmacoInPSVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
          </td>
          <td>
            Profilo che descrive la terapia farmacologica prescritta alla dimissione
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationAccertamentiVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive gli accertamenti eseguiti in Pronto Soccorso
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationAccertamentiVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationComplicanzeVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive le complicanze insorte durante l'episodio di Pronto Soccorso
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationComplicanzeVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDimissioneDataDecessoVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive la data e ora del decesso
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDataDecessoVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDimissioneLivelloAppropriatezzaVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive il livello di appropriatezza dell'accesso alla dimissione
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationLivelloAppropriatezzaVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationMotivoVisitaProblemaAccessoVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive il problema principale all'accesso in Pronto Soccorso
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationProblemaAccessoVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDimissionePrognosiVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive la prognosi alla dimissione
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrognosiVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationMotivoVisitaRagioneVisitaVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive la ragione della visita in Pronto Soccorso
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationRagioneVisitaVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDimissioneRichiestaAutopsiaVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive la richiesta di autopsia
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationRichiestaAutopsiaVPS}}
          </td>
        </tr>
        <tr>
          <td>VPS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationTriageValutazioneAcutezzaVPS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive la valutazione di acutezza (codice) assegnata al triage
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationTriageVPS}}
          </td>
        </tr>
        <tr>
          <td>VACC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionCertificatoVACC.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
          </td>
          <td>
            Profilo che descrive header e body del Certificato Vaccinale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionCertificatoVaccinale}}
          </td>
        </tr>
        <tr>
          <td>SchedaVACC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionSchedaVACC.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
          </td>
          <td>
            Profilo che descrive header e body della Scheda della singola Vaccinazione
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionSchedaSingolaVaccinazione}}
          </td>
        </tr>
        <tr>
          <td>VACC,SchedaVACC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationReazioniAvverseVACC.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive le reazioni e manifestazioni avverse al vaccino
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationReazioniAvverse}}
          </td>
        </tr>
        <tr>
          <td>VACC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationCondizioniSanitarieRischioVACC.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive le condizioni sanitarie a rischio correlate alla vaccinazione
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCondizioniSanitarieRischio}}
          </td>
        </tr>
        <tr>
          <td>VACC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationCategorieRischioVACC.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive le categorie di soggetti a rischio ai fini vaccinali
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCategorieRischio}}
          </td>
        </tr>
        <tr>
          <td>VACC,SchedaVACC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLImmunizationEsoneroVACC.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/immunization.html">Immunization</a>
          </td>
          <td>
            Profilo che descrive la mancata somministrazione del vaccino per esonero, omissione o differimento
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationEsonero}}
          </td>
        </tr>
        <tr>
          <td>VACC,SchedaVACC</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLImmunizationVACC.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/immunization.html">Immunization</a>
          </td>
          <td>
            Profilo che descrive l'evento di somministrazione del vaccino
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazione}}
          </td>
        </tr>
        <tr>
          <td>TPI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionTPI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
          </td>
          <td>
            Profilo che descrive header e body della Tessera per il Portatore di Impianto
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionTesseraPortatoreImpianto}}
          </td>
        </tr>
        <tr>
          <td>TPI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLDeviceTPI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/device.html">Device</a>
          </td>
          <td>
            Profilo che descrive il dispositivo medico impiantato
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceImpianto}}
          </td>
        </tr>
        <tr>
          <td>TPI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLDeviceUseStatementTPI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/deviceusestatement.html">DeviceUseStatement</a>
          </td>
          <td>
            Profilo che descrive l'impianto di un dispositivo medico nel paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceUseStatementTPI}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
          </td>
          <td>
            Profilo che descrive header e body del Referto di Specialistica Ambulatoriale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionRSA}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationQuesitoDiagnosticoRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive il quesito diagnostico del Referto di Specialistica Ambulatoriale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationQuesitoDiagnosticoRSA}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationStoriaClinicaRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive la storia clinica del paziente nel Referto di Specialistica Ambulatoriale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationStoriaClinicaRSA}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationPrecedentiEsamiEseguitiRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive i precedenti esami eseguiti dal paziente nel Referto di Specialistica Ambulatoriale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrecedentiEsamiEseguitiRSA}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationDiagnosiRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive la diagnosi nel Referto di Specialistica Ambulatoriale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationDiagnosiRSA}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationAccertamentiEControlliConsigliatiRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive gli accertamenti e i controlli consigliati nel Referto di Specialistica Ambulatoriale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationAccertamentiControlliConsigliatiRSA}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationPrestazioniRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive le prestazioni eseguite nel Referto di Specialistica Ambulatoriale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationPrestazioniRSA}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationStatementTerapiaInAttoRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationstatement.html">MedicationStatement</a>
          </td>
          <td>
            Profilo che descrive la terapia farmacologica in atto del paziente nel Referto di Specialistica Ambulatoriale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationStatementTerapiaInAttoRSA}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationAdministrationPrestazioniRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationadministration.html">MedicationAdministration</a>
          </td>
          <td>
            Profilo che descrive la somministrazione di farmaci nell'ambito delle prestazioni del Referto di Specialistica Ambulatoriale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationAdministrationPrestazioniRSA}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationAdministrationTerapiaFarmacologicaConsigliataRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationadministration.html">MedicationAdministration</a>
          </td>
          <td>
            Profilo che descrive la terapia farmacologica consigliata al paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationAdministrationTerapiaConsigliataRSA}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestTerapiaFarmacologicaConsigliataRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
          </td>
          <td>
            Profilo che descrive la terapia farmacologica consigliata al paziente
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestTerapiaConsigliataRSA}}
          </td>
        </tr>
        <tr>
          <td>RSA</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationTerapiaFarmacologicaConsigliataRSA.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medication.html">Medication</a>
          </td>
          <td>
            Profilo che descrive il medicinale oggetto della terapia farmacologica consigliata
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationTerapiaConsigliataRSA}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionPAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
          </td>
          <td>
            Profilo che descrive header e body del Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCarePlanPAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/careplan.html">CarePlan</a>
          </td>
          <td>
            Profilo che descrive il piano assistenziale del paziente nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLGoalPAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/goal.html">Goal</a>
          </td>
          <td>
            Profilo che descrive gli obiettivi della presa in carico del paziente nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLGoalPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLChargeItemPAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/chargeitem.html">ChargeItem</a>
          </td>
          <td>
            Profilo che descrive l'ambito di cura della presa in carico nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLChargeItemPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLEncounterPAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/encounter.html">Encounter</a>
          </td>
          <td>
            Profilo che descrive la presa in carico del paziente (modalità di accesso e patologie) nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLEncounterPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLConditionPAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/condition.html">Condition</a>
          </td>
          <td>
            Profilo che descrive le patologie della presa in carico (principale, secondaria, addizionale) nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLConditionPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLProcedurePAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/procedure.html">Procedure</a>
          </td>
          <td>
            Profilo che descrive le prestazioni correlate alla patologia nella presa in carico del Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedurePAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationAnamnesiFumoPAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive lo stile di vita del paziente relativo al fumo nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationFumoPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationAnamnesiAlcoolPAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive lo stile di vita del paziente relativo al consumo di alcol nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationAlcolPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationAnamnesiSedentarietaPAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive lo stile di vita del paziente relativo alla sedentarietà nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationSedentarietaPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationPresaInCaricoCaratterizzazioniClinichePAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive le caratterizzazioni cliniche del paziente nella presa in carico del Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCaratterizzazioniClinichePAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationProgrammazioneValutazionePAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive la data dell'ultima valutazione e l'indicatore di gravità di una prestazione programmata nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationValutazionePAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationRaccomandazioniClinichePAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive le raccomandazioni cliniche rivolte al paziente nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationRaccomandazionePAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLAllergyIntolerancePAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/allergyintolerance.html">AllergyIntolerance</a>
          </td>
          <td>
            Profilo che descrive le allergie del paziente nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLAllergyIntolerancePAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLServiceRequestProgrammazionePAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/servicerequest.html">ServiceRequest</a>
          </td>
          <td>
            Profilo che descrive le prestazioni programmate per il paziente nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLServiceRequestPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestProgrammazione_PAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
          </td>
          <td>
            Profilo che descrive la terapia farmacologica programmata per il paziente nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationProgrammazionePAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medication.html">Medication</a>
          </td>
          <td>
            Profilo che descrive il farmaco della terapia farmacologica programmata (codici ATC, AIC, GE) nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLDeviceRequestProgrammazionePAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/devicerequest.html">DeviceRequest</a>
          </td>
          <td>
            Profilo che descrive le richieste di protesi o ausili programmate per il paziente nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDeviceRequestPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCommunicationRequestProgrammazionePAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/communicationrequest.html">CommunicationRequest</a>
          </td>
          <td>
            Profilo che descrive i contatti telefonici programmati con il paziente nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCommunicationRequestPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationAffiliationRetiPatologiaPAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/organizationaffiliation.html">OrganizationAffiliation</a>
          </td>
          <td>
            Profilo che descrive le reti di patologia in cui è inserito il paziente nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationAffiliationPAI}}
          </td>
        </tr>
        <tr>
          <td>PAI</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLOrganizationErogatorePAI.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/organization.html">Organization</a>
          </td>
          <td>
            Profilo che descrive l'erogatore delle prestazioni programmate (ADI, Cure Intermedie, CDI, CDD, RIA, Cure Palliative) nel Piano Assistenziale Individuale
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationErogatorePAI}}
          </td>
        </tr>
                <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCompositionPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/composition.html">Composition</a>
          </td>
          <td>
            Profilo che descrive il documento Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCompositionPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationStatementTerapieFarmacologichePSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationstatement.html">MedicationStatement</a>
          </td>
          <td>
            Profilo che descrive le terapie farmacologiche del paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationStatementTerapieFarmacologichePSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationStatementAssenzaTerapiePSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationstatement.html">MedicationStatement</a>
          </td>
          <td>
            Profilo che descrive l'assenza o la non conoscenza di terapie farmacologiche del paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationStatementAssenzaTerapiePSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLImmunizationVaccinazioniPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/immunization.html">Immunization</a>
          </td>
          <td>
            Profilo che descrive le vaccinazioni del paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLImmunizationVaccinazioniPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationReazioniAvversePSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive le reazioni avverse alle vaccinazioni nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationReazioniAvversePSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationAssenzaAnamnesiFamiliarePSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive l'assenza o la non conoscenza di informazioni di anamnesi familiare nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationAssenzaAnamnesiFamiliarePSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationStileDiVitaPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive lo stile di vita e i fattori di rischio del paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationStileDiVitaPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationGravidanzePartoPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive gravidanze, parti e stato mestruale della paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationGravidanzePartoPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationStatoFunzionalePSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive lo stato funzionale del paziente, raggruppando capacità motoria, regime di assistenza e altre informazioni nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationStatoFunzionalePSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationCapacitaMotoriaPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive la capacità motoria del paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationCapacitaMotoriaPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationRegimeAssistenzaPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive il regime di assistenza domiciliare (ADI/ADP) del paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationRegimeAssistenzaPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationAltreInformazioniPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive altre informazioni sullo stato funzionale (stato mentale) del paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationAltreInformazioniPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationEsamiLaboratorioPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive i risultati di indagini diagnostiche ed esami di laboratorio nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationEsamiLaboratorioPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLObservationAssensoDissensoDonazioneOrganiPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/observation.html">Observation</a>
          </td>
          <td>
            Profilo che descrive l'assenso o il dissenso alla donazione degli organi nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLObservationAssensoDissensoDonazioneOrganiPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLProcedureProtesiImpiantiAusiliPSS.page.md}}
        <tr>
          <td>PAI</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlprocedurepai.page.md?version=current">RLProcedurePAI</a>
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/procedure.html">Procedure</a>
          </td>
          <td>
            Profilo che descrive protesi, impianti e ausili del paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedureProtesiImpiantiAusiliPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLProcedureTrattamentiPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/procedure.html">Procedure</a>
          </td>
          <td>
            Profilo che descrive i trattamenti e le procedure terapeutiche, chirurgiche e diagnostiche del paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLProcedureTrattamentiPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCarePlanPianoDiCuraPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/careplan.html">CarePlan</a>
          </td>
          <td>
            Profilo che descrive il piano di cura del paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCarePlanPianoDiCuraPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLMedicationRequestPianoDiCuraPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/medicationrequest.html">MedicationRequest</a>
          </td>
          <td>
            Profilo che descrive le terapie farmacologiche previste dal piano di cura nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLMedicationRequestPianoDiCuraPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLDiagnosticReportEsamiLaboratorioPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/diagnosticreport.html">DiagnosticReport</a>
          </td>
          <td>
            Profilo che descrive il referto di indagini diagnostiche ed esami di laboratorio nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLDiagnosticReportEsamiLaboratorioPSS}}
          </td>
        </tr>
        <tr>
          <td>PSS</td>
          <td>
            {{pagelink:Home/Profili-ed-Estensioni/Raccolta-profili/RLCoverageEsenzioniPSS.page.md}}
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/coverage.html">Coverage</a>
          </td>
          <td>
            Profilo che descrive le esenzioni del paziente nel contesto del Profilo Sanitario Sintetico
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLCoverageEsenzioniPSS}}
          </td>
        </tr>
        <tr>
        <td>PAI</td>
          <td><a href="https://simplifier.net/guide/progetto-fhir-rl-core-sviluppo/home/profili-ed-estensioni/raccolta-profili/rlorganizationerogatorepai.page.md?version=current">RLOrganizationErogatorePAI</a>
          </td>
          <td>
            <a href="http://hl7.org/fhir/R4/organization.html">Organization</a>
          </td>
          <td>
            Profilo che descrive gli erogatori delle prestazioni programmate nel Piano Assistenziale Individuale (ADI, Cure intermedie, CDI, CDD, RIA, Cure palliative)
          </td>
          <td>
            {{link:https://fhir.siss.regione.lombardia.it/StructureDefinition/RLOrganizationErogatorePAI}}
          </td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
