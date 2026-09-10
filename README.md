# BWA Desktop Releases

Canale ufficiale degli aggiornamenti firmati di BWA Desktop.

- [Installa BWA Desktop 0.6.68](BWA-Desktop-0.6.68-Setup.exe)
- [Installa BWA Assistenza 1.5](BWA-Assistenza-1.5-Setup.exe)

La nuova attivazione permette al responsabile di generare un codice monouso per i nuovi PC:
collega backup e assistenza senza inserire il token GitHub sul PC del ristorante.
I PC gia configurati mantengono le connessioni e i dati esistenti.

I pacchetti includono il modello BWA pulito, senza dati o credenziali dei ristoranti.

Novita 0.6.57: ordini GVS e Munhowen, controlli Outlook ogni 5 minuti e Bomito ogni 30 minuti mentre BWA e in esecuzione, importazione automatica senza doppioni, categorie da fatture Bomito e segnalazioni dettagliate. Sono supportate le conferme GVS in francese e inglese. Selezionare la casella Outlook nella sezione Ordini; gli accessi Bomito restano in Admin.







Novita 0.6.58: il pagamento Uber Eats viene riconosciuto come Uber Eats External nella chiusura automatica e nel controllo mensile. La correzione mantiene i controlli sui totali e usa la stessa riga 55 di Cash Reconciliation. Il progetto Food Cost sperimentale non e incluso.

Novita 0.6.59: Nesto apre separatamente i dettagli Crew e Manager con il pulsante della rispettiva riga e ritenta solo se il dettaglio e ancora chiuso. Bomito seleziona il ristorante anche fuori dalla parte visibile della pagina, attende la conferma della navigazione e riconosce la vista contabile anche senza movimenti Food. Il progetto Food Cost sperimentale resta escluso.

Novita 0.6.60: selezione dei mesi Bomito tramite i collegamenti precedenti/successivi del periodo, indipendentemente dalla posizione dei pulsanti. Verifica del mese richiesto prima dell'estrazione. Collaudato il passaggio da settembre ad agosto.

Novita 0.6.61: Nesto attiva la voce Wage evaluation direttamente attraverso il controllo della pagina, una sola volta, senza dipendere dalla posizione sullo schermo. Se il menu e gia aperto viene mantenuto. Collaudo reale completato con lettura Crew, Manager, Holiday e sick.

Novita 0.6.62: Nesto riconosce la colonna della data giornaliera indipendentemente dal separatore data impostato in Windows. Risolto il blocco daily-header-not-found durante la lettura Manager, conservando i controlli sulla data richiesta e sulla colonna cumulata.

Novita 0.6.63: diagnostica GitHub con estratto tecnico del log (ultimi 96 KiB per errore), filtrato per credenziali, link, email e percorsi locali. Invio automatico dopo gli errori per i PC con diagnostica GitHub attiva; gli invii non riusciti restano in attesa. I dettagli possono contenere date e importi utili alla diagnosi. I nuovi dettagli sono disponibili per gli errori successivi all'aggiornamento.

Novita 0.6.64: Bomito non segnala piu un ristorante errato quando il risultato verificato non contiene fatture da importare. Gli importi archiviati restano invariati. La scansione manuale mostra un messaggio informativo; il controllo automatico continua senza avvisi ripetuti. I controlli su mese, completezza e ristorante delle fatture presenti restano attivi.

Novita 0.6.66: corretto il riconoscimento Munhowen con nome ristorante su due righe. Controlli sugli importi, esclusione cauzioni e doppioni mantenuti. La correzione non include il catalogo condiviso in preparazione.

Novita 0.6.67: il setup prepara Ollama e il modello locale qwen2.5:7b prima di dichiarare conclusa l'installazione. Download iniziale di diversi GB, connessione Internet necessaria. Riutilizza componenti gia presenti; verifica checksum ufficiale e firma dell'installer. Se fallisce si puo riprovare senza reinstallare BWA. Per PC gia installati: Admin > Prepara AI Mini Matteo. Flusso collaudato con dipendenze simulate; prova completa su PC pulito ancora da confermare. Nessun catalogo condiviso incluso.

Novita 0.6.68: Admin > Carica modello Word fatture clienti. Il modello compatibile del ristorante viene conservato localmente e nei backup, quindi riutilizzato nelle fatture automatiche. Date, ticket, IVA e totali aggiornati senza modificare intestazione e coordinate bancarie. Righe IVA in ordine diverso supportate; corretti i campi data automatici Word. Il testo libero del modello resta invariato. Nessun modello privato aggiunto al pacchetto.
