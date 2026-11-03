# Documenti da processare

Inserire i documenti nelle sottocartelle in base all'ambito:

- `ModificheIG/`: modifiche alle pagine della Implementation Guide, in formato `.docx` o `.xlsx`; usare la skill `word-highlighted-changes`.
- `ModificheProfili/`: modifiche ai profili e agli altri artefatti FHIR, in formato `.xlsx`; usare la skill `excel-yellow-changes`.

Quando non viene indicato un file specifico, ciascuna skill cerca i documenti solo nella propria sottocartella. Non inserire documenti direttamente in `DaProcessare`.

I documenti originali non vengono modificati o eliminati. Prima dell'applicazione, le skill mostrano un'anteprima delle modifiche e attendono l'approvazione.