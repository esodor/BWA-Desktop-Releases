# BWA Desktop 0.6.88

Include le correzioni della 0.6.87 e il modulo Food & Beverage cost configurabile per ristorante.

## Come iniziare
1. Aprire Food & Beverage cost.
2. Premere Carica inventario mese precedente e scegliere il file Excel BarBrain con il foglio Summary completo e i risultati delle formule salvati.
3. Il conteggio deve essere dell'ultimo giorno del mese precedente e appartenere al ristorante configurato: per settembre serve il 31 agosto. Il programma verifica entrambi.
4. Controllare che accessi Lightspeed e lettura ordini siano configurati. Premere Aggiorna online per acquisire vendite e ricalcolare.

Le schede Food cost e Beverage cost appaiono nella dashboard. Prima di avere inventario e report validi mostrano un trattino, non uno zero. Il modulo usa quantità e prezzi dell'inventario e dei carichi del ristorante. Non distribuisce inventari, risultati o prezzi di Belval.

Ogni mese ha un'apertura separata. Al cambio mese occorre caricare il nuovo inventario. I calcoli precedenti restano archiviati. Il primo giorno del mese non ci sono ancora giornate concluse da calcolare.

L'inventario caricato con Carica inventario e controlla serve invece al confronto finale con le quantità teoriche. La sostituzione dell'apertura richiede conferma e un nuovo calcolo. Un file non valido non sostituisce l'apertura esistente; un report incoerente non sostituisce l'ultimo calcolo valido.

## Interpretazione
Le percentuali sono stime parziali basate sulle ricette mappate e sui ricavi netti totali del ristorante. Prodotti, conversioni o prezzi non disponibili restano da verificare. Non equivalgono a un inventario fisico certificato e non modificano automaticamente il WaWi operativo.

Aggiornare dal controllo aggiornamenti BWA. Non occorrono versioni intermedie. Il setup è disponibile per nuove postazioni.
