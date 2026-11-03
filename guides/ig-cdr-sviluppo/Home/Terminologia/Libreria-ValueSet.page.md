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
    <h1>Raccolta ValueSet in uso</h1>
    <div>
      <p>
        Nella tabella sottostante sono raccolti i ValueSet sviluppati
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
      <th>Nome e Link Simplifier</th>
      <th>Descrizione</th>
      <th>URL</th>
    </tr>
  </thead>
  <tbody id="myTable">
    <tr>
      <td>
        {{link:http://loinc.org}}
      </td>
      <td>Tipologia di documento</td>
      <td>http://loinc.org</td>
    </tr>
    <tr>
      <td>
        <a href="https://terminology.hl7.org/7.4.0/en/ValueSet-v3-DiagnosisICD9CM.html">DiagnosisICD9CM</a>
      </td>
      <td>Classificazione internazionale delle malattie ICD-9-CM</td>
      <td>urn:oid:2.16.840.1.113883.6.103</td>
    </tr>
    <tr>
      <td>
        <a href="https://www.fascicolosanitario.gov.it/portale/sistema-di-codifica-aic">Codifica AIC</a>
      </td>
      <td>Codici AIC dei medicinali</td>
      <td>https://www.fascicolosanitario.gov.it/portale/sistema-di-codifica-aic/</td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.org/fhir/ValueSet/composition-status}}
      </td>
      <td>Stato del documento</td>
      <td>http://hl7.org/fhir/ValueSet/composition-status</td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.org/fhir/ValueSet/composition-attestation-mode}}
      </td>
      <td>Modalità di attestazione del documento</td>
      <td>http://hl7.org/fhir/ValueSet/composition-attestation-mode</td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.it/fhir/lab-report/CodeSystem/istat-unitaAmministrativeTerritoriali}}
      </td>
      <td>Codice identificativo di ciascuna sezione del documento</td>
      <td>http://loinc.org
      </td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.it/fhir/lab-report/CodeSystem/istat-unitaAmministrativeTerritoriali}}
      </td>
      <td>Codice identificativo di ciascuna sezione del documento</td>
      <td>urn:oid:1.2.840.10008.2.16.4
      </td>
    </tr>
    <tr>
      <td>
        {{link:http://terminology.hl7.org/CodeSystem/v3-RouteOfAdministration}}
      </td>
      <td>Via di somministrazione di farmaci e vaccini</td>
      <td>urn:oid:2.16.840.1.113883.5.112
      </td>
    </tr>
    <tr>
      <td>
        {{link:http://terminology.hl7.org/CodeSystem/v3-ActSite}}
      </td>
      <td>Sede anatomica di somministrazione di farmaci e vaccini</td>
      <td>urn:oid:2.16.840.1.113883.5.1052
      </td>
    </tr>
    <tr>
      <td>
        Classificazione regionale delle patologie croniche
      </td>
      <td>Codifica delle patologie croniche del paziente (storia clinica)</td>
      <td>urn:oid:2.16.840.1.113883.2.9.77.22.11.10</td>
    </tr>
    <tr>
      <td>
        <a href="https://www.hl7.org/fhir/R4/valueset-medicationrequest-intent.html">MedicationRequestIntent</a>
      </td>
      <td>Grado di formalità e vincolatività della richiesta di farmaco</td>
      <td>https://www.hl7.org/fhir/R4/valueset-medicationrequest-intent.html</td>
    </tr>
    <tr>
      <td>CRS-SISS - Tipologia documento</td>
      <td>Tipologia di documento (31 = Piano Assistenziale Individuale)</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.6.10</td>
    </tr>
    <tr>
      <td>CRS-SISS - Sezioni PAI</td>
      <td>Codici delle sezioni del Piano Assistenziale Individuale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.1</td>
    </tr>
    <tr>
      <td>CRS-SISS - Obiettivo presa in carico</td>
      <td>Obiettivi della presa in carico del Piano Assistenziale Individuale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.8</td>
    </tr>
    <tr>
      <td>CRS-SISS - Ambito di cura</td>
      <td>Ambito di cura della presa in carico del Piano Assistenziale Individuale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.2</td>
    </tr>
    <tr>
      <td>CRS-SISS - Modalità di accesso</td>
      <td>Modalità di accesso alla presa in carico del Piano Assistenziale Individuale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.9</td>
    </tr>
    <tr>
      <td>CRS-SISS - Patologie</td>
      <td>Patologie della presa in carico del Piano Assistenziale Individuale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.10</td>
    </tr>
    <tr>
      <td>CRS-SISS - Livello di complessità</td>
      <td>Livello di complessità della patologia principale del Piano Assistenziale Individuale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.49</td>
    </tr>
    <tr>
      <td>CRS-SISS - Tipo prestazioni correlate alla patologia</td>
      <td>Tipo di prestazioni correlate alla patologia del Piano Assistenziale Individuale (1 = Ambulatoriali, 2 = Farmaceutiche, 3 = Regimi Privati, 4 = Ausili o Presidi Medici, 99 = Altro)</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.60</td>
    </tr>
    <tr>
      <td>CRS-SISS - Prestazioni correlate alla patologia</td>
      <td>Prestazioni correlate alla patologia del Piano Assistenziale Individuale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.61</td>
    </tr>
    <tr>
      <td>CRS-SISS - Stili di vita</td>
      <td>Tipologia di stile di vita del Piano Assistenziale Individuale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.12</td>
    </tr>
    <tr>
      <td>CRS-SISS - Stile di vita Fumo</td>
      <td>Valori dello stile di vita relativo al fumo</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.13</td>
    </tr>
    <tr>
      <td>CRS-SISS - Stile di vita Alcol</td>
      <td>Valori dello stile di vita relativo al consumo di alcol</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.14</td>
    </tr>
    <tr>
      <td>CRS-SISS - Stile di vita Sedentarietà</td>
      <td>Valori dello stile di vita relativo alla sedentarietà</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.15</td>
    </tr>
    <tr>
      <td>CRS-SISS - Presa in carico</td>
      <td>Codici delle osservazioni della presa in carico del Piano Assistenziale Individuale (1 = Caratterizzazioni Cliniche)</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.7</td>
    </tr>
    <tr>
      <td>CRS-SISS - Programmazione</td>
      <td>Codici delle osservazioni della programmazione clinico assistenziale </td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.17</td>
    </tr>
    <tr>
      <td>CRS-SISS - Indicatore di gravità</td>
      <td>Indicatore di gravità della programmazione clinico assistenziale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.40</td>
    </tr>
    <tr>
      <td>CRS-SISS - Raccomandazioni cliniche</td>
      <td>Codici delle raccomandazioni cliniche del Piano Assistenziale Individuale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.37</td>
    </tr>
    <tr>
      <td>
        {{link:http://hl7.org/fhir/ValueSet/allergyintolerance-clinical}}
      </td>
      <td>Stato clinico dell'allergia o intolleranza</td>
      <td>http://hl7.org/fhir/ValueSet/allergyintolerance-clinical</td>
    </tr>
    <tr>
      <td>CRS-SISS - Tipologia prestazione</td>
      <td>Tipologia della prestazione programmata del Piano Assistenziale Individuale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.18</td>
    </tr>
    <tr>
      <td>Nomenclatore prestazioni ambulatoriali</td>
      <td>Prestazioni ambulatoriali</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.6.11</td>
    </tr>
    <tr>
      <td>CRS-SISS - Prestazione vaccinale</td>
      <td>Prestazioni vaccinali programmate</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.26</td>
    </tr>
    <tr>
      <td>Codice regionale vaccino</td>
      <td>Codice regionale del vaccino</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.6.2</td>
    </tr>
    <tr>
      <td>CRS-SISS - Prestazione ricovero</td>
      <td>Prestazioni di ricovero programmate</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.28</td>
    </tr>
    <tr>
      <td>CRS-SISS - ADI</td>
      <td>Prestazioni di assistenza domiciliare integrata</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.29</td>
    </tr>
    <tr>
      <td>CRS-SISS - Cure intermedie</td>
      <td>Prestazioni di cure intermedie</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.30</td>
    </tr>
    <tr>
      <td>CRS-SISS - CDI</td>
      <td>Prestazioni del centro diurno integrato</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.32</td>
    </tr>
    <tr>
      <td>CRS-SISS - CDD</td>
      <td>Prestazioni del centro diurno per disabili</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.50</td>
    </tr>
    <tr>
      <td>CRS-SISS - RIA</td>
      <td>Prestazioni di riabilitazione ambulatoriale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.39</td>
    </tr>
    <tr>
      <td>CRS-SISS - Cure palliative</td>
      <td>Prestazioni di cure palliative</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.51</td>
    </tr>
    <tr>
      <td>CRS-SISS - Intervento educazionale</td>
      <td>Interventi educazionali programmati</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.35</td>
    </tr>
    <tr>
      <td>CRS-SISS - Flag telemedicina</td>
      <td>Indicazione di erogazione in telemedicina</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.55</td>
    </tr>
    <tr>
      <td>CRS-SISS - Validità</td>
      <td>Validità del bisogno della prestazione programmata</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.41</td>
    </tr>
    <tr>
      <td>CRS-SISS - Tipologia frequenza</td>
      <td>Tipologia di frequenza della prestazione programmata</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.42</td>
    </tr>
    <tr>
      <td>CRS-SISS - Unità di misura</td>
      <td>Unità di misura della durata della prestazione programmata</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.43</td>
    </tr>
    <tr>
      <td>CRS-SISS - Frequenza assunzione farmaco</td>
      <td>Frequenza di assunzione del farmaco programmato</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.57</td>
    </tr>
    <tr>
      <td>
        <a href="https://www.who.int/tools/atc-ddd-toolkit/atc-classification">ATC</a>
      </td>
      <td>Classificazione Anatomica Terapeutica Chimica dei farmaci</td>
      <td>http://www.whocc.no/atc</td>
    </tr>
    <tr>
      <td>AIFA - Gruppi di Equivalenza</td>
      <td>Gruppi di equivalenza dei farmaci (AIFA)</td>
      <td>urn:oid:2.16.840.1.113883.2.9.6.1.51</td>
    </tr>
    <tr>
      <td>CRS-SISS - Flag protesica</td>
      <td>Flag protesica della richiesta di protesi o ausili</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.23</td>
    </tr>
    <tr>
      <td>CRS-SISS - Codifica ISO protesica</td>
      <td>Codifica ISO delle protesi e degli ausili</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.25</td>
    </tr>
    <tr>
      <td>CRS-SISS - Contatto telefonico programmato</td>
      <td>Tipologia di contatto telefonico programmato con il paziente</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.34</td>
    </tr>
    <tr>
      <td>CRS-SISS - Reti di patologia</td>
      <td>Reti di patologia del Piano Assistenziale Individuale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.27</td>
    </tr>
    <tr>
      <td>CRS-SISS - Erogatori ADI</td>
      <td>Codici degli erogatori di assistenza domiciliare integrata</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.44</td>
    </tr>
    <tr>
      <td>CRS-SISS - Erogatori Cure Intermedie</td>
      <td>Codici degli erogatori di cure intermedie</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.47</td>
    </tr>
    <tr>
      <td>CRS-SISS - Erogatori CDI</td>
      <td>Codici degli erogatori dei centri diurni integrati</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.45</td>
    </tr>
    <tr>
      <td>CRS-SISS - Erogatori CDD</td>
      <td>Codici degli erogatori dei centri diurni per disabili</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.46</td>
    </tr>
    <tr>
      <td>CRS-SISS - Erogatori RIA</td>
      <td>Codici degli erogatori di riabilitazione ambulatoriale</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.48</td>
    </tr>
    <tr>
      <td>CRS-SISS - Erogatori Cure Palliative</td>
      <td>Codici degli erogatori di cure palliative</td>
      <td>urn:oid:2.16.840.1.113883.2.9.2.30.3.1.3.13.6.52</td>
    </tr>
  </tbody>
</table>
  </body>
</html>
