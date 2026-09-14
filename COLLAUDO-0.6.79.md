# Collaudo BWA Desktop 0.6.79 — 14 settembre 2026

## Esito

Candidato compilato, installato sul Desktop mediante il normale aggiornamento firmato. Verificato l'archivio invariato e conservata la copia dei file precedenti. Eseguibile installato identico a quello del pacchetto: SHA256 30f5f7bfc2b40184074971250bb69076bbe6dc75eea1ea7b6a64d76d56e24bec.

## Verifiche eseguite

- Gate finale di 20 gruppi: regressione generale (59 controlli), quattro lingue, cache dashboard/storico, grafici, export, controlli Mini Matteo e animazioni, Petty Cash, IVA e rettifiche fatture, diagnostica con immagini.
- Installer in quattro lingue: 44 verifiche con archivi temporanei; modello iniziale incluso, nessun destinatario email privato, nessuna sovrascrittura del modello esistente, esportazione senza Excel.
- Interfaccia: 44 rendering pagina/lingua e 15 cicli nascondi/ripristina con indicatori di operazione attiva. Verificata la tabella del modello dopo il completamento del ridisegno. Sono prove su dati sintetici; gli indicatori non equivalgono a bot reali in esecuzione.
- Modello asincrono: ultima selezione richiesta, invalidazione dopo salvataggio, riuso della cache e formule protette. Test con message loop reale per 600 secondi: 672 cicli, p95 del gestore comandi 44 ms, p95 ritardo del timer UI 57 ms, massimo 735 ms. Controllo degli accessi UI da thread errati attivo, nessun errore. Nessun servizio di rete attivo in questa prova.
- Cambio lingua: 30 passaggi, input non salvati conservati; p95 424,39 ms sulla MainWindow prima dell'accesso, senza bot. Non è una misura delle prestazioni del PC della collega.
- Nuovi campi di consultazione: importi e coperti esatti, fatture escluse fuori dal totale, note di credito sottratte, dati assenti mostrati come non disponibili. Il client 0.6.78 accetta lo schema esteso.
- Collegamento separato: credenziale protetta, nome ristorante verificato, codice di altro ristorante rifiutato, precedente connessione conservata, dati e impostazioni backup invariati. Verificato anche un archivio senza impostazioni di backup.
- Servizio di consultazione: test isolati di autorizzazione, schema, versione, revoca e tentativi ripetuti. Distribuzione aggiornata; health HTTP 200 e accesso non autenticato al riepilogo HTTP 401.
- Client di consultazione: quattro lingue, tabella di sola lettura, credenziale riusata dopo tentativo incompleto e vecchia connessione conservata.
- Aggiornamento: verifica firma/hash, rifiuto di manifest, ZIP e staging alterati; conservazione di archivio, credenziali, scansioni, modelli e impostazioni browser in installazione sintetica, con copia di ripristino. L'aggiornatore pubblicato 0.6.74 prepara direttamente la 0.6.79.
- Pacchetto: 163 elementi confrontati con la selezione ammessa; nessun archivio ristorante, email, database, credenziale o chiave privata incluso. Sintassi verificata per 84 file Python.

## Problemi intercettati durante il collaudo

Una prova precedente di chiusura della finestra durante un callback ha segnalato un problema di Dispose/CreateHandle: aggiunto il controllo Disposing e verificato il candidato finale con il message loop reale. Una prova dell'animazione richiedeva la propria cartella di output, assente nella nuova copia: ripristinata la directory di test e ripetuto il gate. Una prima immagine della tabella è stata acquisita prima del ridisegno; verificati visibilità, dimensioni e 630 righe, poi acquisita nuovamente dopo l'elaborazione degli eventi. Nessuna modifica del calcolo finanziario per questi controlli.

## Limiti e verifiche operative restanti

Il test di un'ora e le letture reali Lightspeed/Nesto/Bomito appartengono alla base 0.6.78. In questo aggiornamento non sono stati ripetuti né presentati come nuovi: i bot sono invariati. Il test continuativo della 0.6.79 dura dieci minuti e riguarda il modello/UI su dati sintetici.

Resta da effettuare l'abbinamento con codice e il controllo operativo tra due PC reali del ristorante, con pubblicazione esplicitamente abilitata. Non sono state inviate email o chiusure, né caricati dati finanziari reali per collaudare la nuova consultazione. Le prestazioni dell'AI sulla postazione della collega dipendono dal suo hardware. Il flusso completo di download iniziale Ollama su un PC Windows appena preparato non è stato ripetuto.

Food Cost teorico, voce e personaggio 3D restano separati come richiesto. Il superamento dei test non garantisce assenza di ogni possibile errore futuro.