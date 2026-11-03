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
      <td>RAD</td>
      <td>MedicationStatement-TerapiaFarmacologica</td>
      <td>Terapia farmacologica precedente del paziente</td>
      <td>{{link:MedicationStatement/rl-medicationstatement-001}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>MedicationStatement-TerapiaFarmacologica</td>
      <td>Terapia farmacologica in atto del paziente</td>
      <td>{{link:MedicationStatement/rl-medicationstatement-002}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Esame Eseguito (1)</td>
      <td>{{link:Observation/Example-Observation-EsameEseguito-1-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Esame Eseguito (2)</td>
      <td>{{link:Observation/Example-Observation-EsameEseguito-2-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Precedenti Esami Eseguiti (1)</td>
      <td>{{link:Observation/Example-Observation-PrecedentiEsamiEseguiti-1-RAD}}</td>
    </tr>
    <tr>
     <td>RAD</td>
     <td>Observation</td>
    <td>Precedenti Esami Eseguiti (2)</td>
    <td>{{link:Observation/Example-Observation-PrecedentiEsamiEseguiti-2-RAD}}</td>
  </tr>
  <tr>
   <td>RAD</td>
   <td>Observation</td>
   <td>Complicanze (1)</td>
   <td>{{link:Observation/Example-Observation-Complicanze-1-RAD}}</td>
  </tr>
  <tr>
   <td>RAD</td>
   <td>Observation</td>
   <td>Complicanze (2)</td>
   <td>{{link:Observation/Example-Observation-Complicanze-2-RAD}}</td>
  </tr>
  <tr>
   <td>RAD</td>
   <td>ImagingStudy</td>
   <td>ImagingStudy (1)</td>
   <td>{{link:ImagingStudy/Example-ImagingStudy-1-RAD}}</td>
  </tr>
  <tr>
   <td>RAD</td>
   <td>ImagingStudy</td>
   <td>ImagingStudy (2)</td>
   <td>{{link:ImagingStudy/Example-ImagingStudy-2-RAD}}</td>
</tr>
<tr>
 <td>RAD</td>
 <td>Observation</td>
 <td>Quesito Diagnostico</td>
 <td>{{link:Observation/Example-Observation-QuesitoDiagnostico-1-RAD}}</td>
</tr>
  <tr>
   <td>PTI</td>
   <td>Composition</td>
   <td>Piano Terapeutico Individuale (1)</td>
   <td>{{link:Composition/Example-Composition-1-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>Composition</td>
   <td>Piano Terapeutico Individuale (2)</td>
   <td>{{link:Composition/Example-Composition-2-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>CarePlan</td>
   <td>Piano Terapeutico (1)</td>
   <td>{{link:CarePlan/Example-CarePlan-1-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>CarePlan</td>
   <td>Piano Terapeutico (2)</td>
   <td>{{link:CarePlan/Example-CarePlan-2-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>Condition</td>
   <td>Condizioni di Erogabilità (1)</td>
   <td>{{link:Condition/Example-Condition-CondizioniErogabilita-1-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>Condition</td>
   <td>Condizioni di Erogabilità (2)</td>
   <td>{{link:Condition/Example-Condition-CondizioniErogabilita-2-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>Condition</td>
   <td>Criteri di Esclusione (1)</td>
   <td>{{link:Condition/Example-Condition-CriteriEsclusione-1-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>Condition</td>
   <td>Criteri di Esclusione (2)</td>
   <td>{{link:Condition/Example-Condition-CriteriEsclusione-2-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>Observation</td>
   <td>Peso (1)</td>
   <td>{{link:Observation/Example-Observation-Peso-1-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>Observation</td>
   <td>Peso (2)</td>
   <td>{{link:Observation/Example-Observation-Peso-2-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>Observation</td>
   <td>Durata Malattia (1)</td>
   <td>{{link:Observation/Example-Observation-DurataMalattia-1-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>Observation</td>
   <td>Durata Malattia (2)</td>
   <td>{{link:Observation/Example-Observation-DurataMalattia-2-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>MedicationRequest</td>
   <td>Programma Terapeutico (1)</td>
   <td>{{link:MedicationRequest/Example-MedicationRequest-1-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>MedicationRequest</td>
   <td>Programma Terapeutico (2)</td>
   <td>{{link:MedicationRequest/Example-MedicationRequest-2-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>Medication</td>
   <td>Farmaco (1)</td>
   <td>{{link:Medication/Example-Medication-1-PTI}}</td>
  </tr>
  <tr>
   <td>PTI</td>
   <td>Medication</td>
   <td>Farmaco (2)</td>
   <td>{{link:Medication/Example-Medication-2-PTI}}</td>
  </tr>
    <tr>
   <td>LDO</td>
   <td>Composition</td>
   <td>Lettera di Dimissione Ospedaliera</td>
   <td>{{link:Composition/Example-Composition-LDO}}</td>
  </tr>
  <tr>
   <td>LDO</td>
   <td>MedicationAdministration</td>
   <td>Terapia Farmacologica somministrata durante il Ricovero</td>
   <td>{{link:MedicationAdministration/Example-MedicationAdministration-Ricovero-LDO}}</td>
  </tr>
  <tr>
   <td>LDO</td>
   <td>MedicationRequest</td>
   <td>Terapia Farmacologica alla Dimissione</td>
   <td>{{link:MedicationRequest/Example-MedicationRequest-Dimissione-LDO}}</td>
  </tr>
  <tr>
   <td>LDO</td>
   <td>MedicationRequest</td>
   <td>Terapia Farmacologica prescritta durante il Ricovero</td>
   <td>{{link:MedicationRequest/Example-MedicationRequest-Ricovero-LDO}}</td>
  </tr>
  <tr>
   <td>LDO</td>
   <td>Observation</td>
   <td>Complicanze</td>
   <td>{{link:Observation/Example-Observation-Complicanze-LDO}}</td>
  </tr>
  <tr>
   <td>LDO</td>
   <td>Observation</td>
   <td>Consulenza</td>
   <td>{{link:Observation/Example-Observation-Consulenza-LDO}}</td>
  </tr>
  <tr>
   <td>LDO</td>
   <td>Observation</td>
   <td>Decorso Clinico</td>
   <td>{{link:Observation/Example-Observation-DecorsoClinico-LDO}}</td>
  </tr>
  <tr>
   <td>LDO</td>
   <td>Observation</td>
   <td>Diagnosi alla Dimissione</td>
   <td>{{link:Observation/Example-Observation-DiagnosiDimissione-LDO}}</td>
  </tr>
  <tr>
   <td>LDO</td>
   <td>Observation</td>
   <td>Esami Eseguiti durante il Ricovero</td>
   <td>{{link:Observation/Example-Observation-EsamiEseguitiRicovero-LDO}}</td>
  </tr>
  <tr>
   <td>LDO</td>
   <td>Observation</td>
   <td>Motivo del Ricovero</td>
   <td>{{link:Observation/Example-Observation-MotivoRicovero-LDO}}</td>
  </tr>
  <tr>
   <td>LDO</td>
   <td>Observation</td>
   <td>Procedure durante il Ricovero</td>
   <td>{{link:Observation/Example-Observation-ProcedureRicovero-LDO}}</td>
  </tr>
  <tr>
   <td>LDO</td>
   <td>Procedure</td>
   <td>Procedure Eseguite durante il Ricovero</td>
   <td>{{link:Procedure/Example-Procedure-LDO}}</td>
  </tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Precedenti Esami Eseguiti (2)</td>
      <td>{{link:Observation/Example-Observation-PrecedentiEsamiEseguiti-2-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Complicanze (1)</td>
      <td>{{link:Observation/Example-Observation-Complicanze-1-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Complicanze (2)</td>
      <td>{{link:Observation/Example-Observation-Complicanze-2-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Composition</td>
      <td>Informazioni mediche paziente</td>
      <td>{{link:Composition/referto-radiologia-0451-20260922}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>ImagingStudy</td>
      <td>ImagingStudy (1)</td>
      <td>{{link:ImagingStudy/Example-ImagingStudy-1-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>ImagingStudy</td>
      <td>ImagingStudy (2)</td>
      <td>{{link:ImagingStudy/Example-ImagingStudy-2-RAD}}</td>
    </tr>
    <tr>
      <td>RAD</td>
      <td>Observation</td>
      <td>Quesito Diagnostico</td>
      <td>{{link:Observation/Example-Observation-QuesitoDiagnostico-1-RAD}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Composition</td>
      <td>Verbale di Pronto Soccorso</td>
      <td>{{link:Composition/Example-Composition-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>CarePlan</td>
      <td>Piano di cura alla dimissione</td>
      <td>{{link:CarePlan/Example-CarePlan-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>MedicationAdministration</td>
      <td>Terapia farmacologica somministrata in Pronto Soccorso</td>
      <td>{{link:MedicationAdministration/Example-MedicationAdministration-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>MedicationRequest</td>
      <td>Richiesta di terapia farmacologica in Pronto Soccorso</td>
      <td>{{link:MedicationRequest/Example-MedicationRequestTerapiaPS-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>MedicationRequest</td>
      <td>Terapia farmacologica prescritta alla dimissione</td>
      <td>{{link:MedicationRequest/Example-MedicationRequestTerapiaDimissione-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Accertamenti</td>
      <td>{{link:Observation/Example-ObservationAccertamenti-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Complicanze</td>
      <td>{{link:Observation/Example-ObservationComplicanze-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Dimissione - Data decesso</td>
      <td>{{link:Observation/Example-ObservationDataDecesso-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Dimissione - Livello appropriatezza</td>
      <td>{{link:Observation/Example-ObservationLivelloAppropriatezza-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Dimissione - Prognosi</td>
      <td>{{link:Observation/Example-ObservationPrognosi-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Dimissione - Richiesta autopsia</td>
      <td>{{link:Observation/Example-ObservationRichiestaAutopsia-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Motivo della visita - Problema all'accesso</td>
      <td>{{link:Observation/Example-ObservationProblemaAccesso-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Motivo della visita - Ragione della visita</td>
      <td>{{link:Observation/Example-ObservationRagioneVisita-1-VPS}}</td>
    </tr>
    <tr>
      <td>VPS</td>
      <td>Observation</td>
      <td>Triage - Valutazione acutezza</td>
      <td>{{link:Observation/Example-ObservationTriage-1-VPS}}</td>
    </tr>
    <tr>
      <td>TPI</td>
      <td>Composition</td>
      <td>Tessera per il portatore di impianto</td>
      <td>{{link:Composition/tpi-example}}</td>
    </tr>
    <tr>
      <td>TPI</td>
      <td>Device</td>
      <td>Dispositivo impiantato (pacemaker)</td>
      <td>{{link:Device/example-device-impianto}}</td>
    </tr>
    <tr>
      <td>TPI</td>
      <td>DeviceUseStatement</td>
      <td>Impianto del dispositivo (pacemaker) nel paziente</td>
      <td>{{link:DeviceUseStatement/example-deviceusestatement-tpi}}</td>
    </tr>
    <tr>
      <td>VACC</td>
      <td>Composition</td>
      <td>Certificato Vaccinale</td>
      <td>{{link:Composition/composition-certificato-vaccinale}}</td>
    </tr>
    <tr>
      <td>SchedaVACC</td>
      <td>Composition</td>
      <td>Scheda della singola vaccinazione (esonero)</td>
      <td>{{link:Composition/composition-esonero-2}}</td>
    </tr>
    <tr>
      <td>VACC</td>
      <td>Immunization</td>
      <td>Vaccinazione MPR non somministrata per esonero</td>
      <td>{{link:Immunization/immunization-esonero}}</td>
    </tr>
    <tr>
    <td>SchedaVACC</td>
      <td>Immunization</td>
      <td>Vaccinazione MPR somministrata (dose 1)</td>
      <td>{{link:Immunization/immunization-vaccinazione}}</td>
    </tr>
    <tr>
      <td>VACC</td>
      <td>Immunization</td>
      <td>Vaccinazione MPR somministrata - dose 1 (Certificato Vaccinale)</td>
      <td>{{link:Immunization/immunization-dose1}}</td>
    </tr>
    <tr>
      <td>VACC</td>
      <td>Observation</td>
      <td>Categoria a rischio per la vaccinazione</td>
      <td>{{link:Observation/observation-rischio}}</td>
    </tr>
    <tr>
      <td>VACC</td>
      <td>Observation</td>
      <td>Condizione sanitaria a rischio per la vaccinazione</td>
      <td>{{link:Observation/observation-condizione}}</td>
    </tr>
    <tr>
      <td>VACC,SchedaVACC</td>
      <td>Observation</td>
      <td>Reazione avversa alla vaccinazione</td>
      <td>{{link:Observation/observation-reazione}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>Composition</td>
      <td>Referto di Specialistica Ambulatoriale</td>
      <td>{{link:Composition/Example-Composition-1-RSA}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>Observation</td>
      <td>Quesito Diagnostico</td>
      <td>{{link:Observation/Example-ObservationQuesitoDiagnostico-1-RSA}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>Observation</td>
      <td>Storia Clinica</td>
      <td>{{link:Observation/Example-ObservationStoriaClinica-1-RSA}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>Observation</td>
      <td>Precedenti Esami Eseguiti</td>
      <td>{{link:Observation/Example-ObservationPrecedentiEsamiEseguiti-1-RSA}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>Observation</td>
      <td>Diagnosi</td>
      <td>{{link:Observation/Example-ObservationDiagnosi-1-RSA}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>Observation</td>
      <td>Accertamenti e Controlli Consigliati</td>
      <td>{{link:Observation/Example-ObservationAccertamentiControlliConsigliati-1-RSA}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>Observation</td>
      <td>Prestazioni</td>
      <td>{{link:Observation/Example-ObservationPrestazioni-1-RSA}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>MedicationStatement</td>
      <td>Terapia farmacologica in atto</td>
      <td>{{link:MedicationStatement/Example-MedicationStatementTerapiaInAtto-1-RSA}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>MedicationAdministration</td>
      <td>Somministrazione di farmaci durante la prestazione</td>
      <td>{{link:MedicationAdministration/Example-MedicationAdministrationPrestazioni-1-RSA}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>MedicationAdministration</td>
      <td>Terapia farmacologica consigliata</td>
      <td>{{link:MedicationAdministration/Example-MedicationAdministrationTerapiaConsigliata-1-RSA}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>MedicationRequest</td>
      <td>Terapia farmacologica consigliata</td>
      <td>{{link:MedicationRequest/Example-MedicationRequestTerapiaConsigliata-1-RSA}}</td>
    </tr>
    <tr>
      <td>RSA</td>
      <td>Medication</td>
      <td>Medicinale della terapia farmacologica consigliata</td>
      <td>{{link:Medication/Example-MedicationTerapiaConsigliata-1-RSA}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Composition</td>
      <td>Piano Assistenziale Individuale - paziente cronico iperteso</td>
      <td>{{link:Composition/Example-Composition-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>CarePlan</td>
      <td>Piano assistenziale del paziente cronico iperteso</td>
      <td>{{link:CarePlan/Example-CarePlan-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Goal</td>
      <td>Obiettivo della presa in carico - controllo dei valori pressori</td>
      <td>{{link:Goal/Example-Goal-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>ChargeItem</td>
      <td>Ambito di cura della presa in carico - cronicità</td>
      <td>{{link:ChargeItem/Example-ChargeItem-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Encounter</td>
      <td>Presa in carico del paziente cronico iperteso</td>
      <td>{{link:Encounter/9f0a1b2c-3d4e-4f5a-8b6c-7d8e9f0a1b2c}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Condition</td>
      <td>Patologia principale della presa in carico - ipertensione arteriosa essenziale</td>
      <td>{{link:Condition/Example-Condition-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Procedure</td>
      <td>Prestazione ambulatoriale correlata alla patologia - visita cardiologica di controllo</td>
      <td>{{link:Procedure/Example-Procedure-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Observation</td>
      <td>Stile di vita - Fumo: ex fumatore</td>
      <td>{{link:Observation/Example-ObservationFumo-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Observation</td>
      <td>Stile di vita - Alcol: consumo occasionale</td>
      <td>{{link:Observation/Example-ObservationAlcol-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Observation</td>
      <td>Stile di vita - Sedentarietà: attività fisica moderata</td>
      <td>{{link:Observation/Example-ObservationSedentarieta-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Observation</td>
      <td>Caratterizzazione clinica - paziente con pluripatologia cronica</td>
      <td>{{link:Observation/Example-ObservationCaratterizzazioniCliniche-1-PAI}}</td>
    </tr>
    <tr>
      <td>CRS-SISS - Programmazione (codici osservazioni)</td>
      <td>Codici delle osservazioni della programmazione clinico assistenziale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.17</td>
    </tr>
    <tr>
      <td>CRS-SISS - Indicatore di gravità</td>
      <td>Indicatore di gravità della programmazione clinico assistenziale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.40</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Observation</td>
      <td>Raccomandazione clinica - riduzione del consumo di sale e controllo pressorio domiciliare</td>
      <td>{{link:Observation/Example-ObservationRaccomandazione-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>AllergyIntolerance</td>
      <td>Allergia alla penicillina</td>
      <td>{{link:AllergyIntolerance/Example-AllergyIntolerance-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>ServiceRequest</td>
      <td>Prestazione programmata - visita cardiologica di controllo annuale</td>
      <td>{{link:ServiceRequest/Example-ServiceRequest-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>MedicationRequest</td>
      <td>Terapia farmacologica programmata - Ramipril 5 mg, 1 compressa al mattino</td>
      <td>{{link:MedicationRequest/Example-MedicationRequest-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Medication</td>
      <td>Farmaco programmato - Ramipril 5 mg compresse (ATC C09AA05)</td>
      <td>{{link:Medication/Example-Medication-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>DeviceRequest</td>
      <td>Richiesta di ausilio - misuratore di pressione arteriosa automatico</td>
      <td>{{link:DeviceRequest/Example-DeviceRequest-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>CommunicationRequest</td>
      <td>Contatto telefonico programmato mensile</td>
      <td>{{link:CommunicationRequest/Example-CommunicationRequest-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>OrganizationAffiliation</td>
      <td>Rete di patologia - rete cardiovascolare</td>
      <td>{{link:OrganizationAffiliation/Example-OrganizationAffiliation-1-PAI}}</td>
    </tr>
    <tr>
      <td>PAI</td>
      <td>Organization</td>
      <td>Erogatore della prestazione programmata - ente erogatore ADI</td>
      <td>{{link:Organization/Example-OrganizationErogatore-1-PAI}}</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
