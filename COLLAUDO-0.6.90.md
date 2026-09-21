# Verifiche BWA Desktop 0.6.90

- Riprodotto il precedente rifiuto di Regional Voucher con il lettore 0.6.89 su report sintetico.
- Nove test del lettore: pagamento misto con contanti, assenza del voucher, normalizzazione del nome, rimborso, duplicati, metodo sconosciuto, totale incoerente, controllo Gift Card e quadratura mensile.
- Sei verifiche integrate nel programma compilato: totale nel foglio Voucher, formula originale della riga 39 conservata, importo corretto in riga 39, contanti separati, esportazione XLSX effettiva e compatibilità dei voucher manuali nelle vecchie chiusure.
- Firma del feed verificata dai client 0.6.85 e 0.6.90; payload dell'installer identico al pacchetto aggiornamento.
- Aggiornamento provato su installazione sintetica: conservazione archivio, configurazioni, credenziali fittizie, modello e scansioni; copia di ripristino; rifiuto di firma, pacchetto e staging alterati.
- Quarantaquattro verifiche di installazione nuova nelle lingue italiano, inglese, francese e tedesco.
- Audit dei 376 file: percorsi e hash verificati, sintassi di 290 file Python, esclusione di archivi e credenziali. Risorse incorporate confrontate con la base pubblica. Rispetto al pacchetto 0.6.89 cambiano soltanto BWA-Desktop.exe e reader/lightspeed_reader.py.
- Scansione Microsoft Defender dei pacchetti completata senza rilevamenti relativi a questi artefatti.

Limiti: le prove contabili usano dati sintetici; non sono stati riscritti dati operativi né ripetuta una chiusura reale su un PC remoto. La prima analisi del report originale dopo l'aggiornamento resta da verificare. Le prove di installazione usano cartelle temporanee corte, per rispettare il limite dei percorsi del runtime Windows.
