# Collaudo BWA Desktop 0.6.78

Data: 14 settembre 2026. Questo rapporto distingue prove automatizzate, servizi reali e verifiche non eseguite. Non è una garanzia di assenza di ogni possibile errore.

## Identità del pacchetto

Applicazione collaudata e inclusa nel pacchetto: SHA256 `30EC53B6EFF13D4878DCB20DF6F4F6DB3EC52AFF0A1CA75D954DB4F7BF9D44DE`.

- Setup: `BWA-Desktop-0.6.78-Setup.exe`, 25.311.744 byte, SHA256 `ca17bb18c781253a4e24f24f375ba4b2d279af96cfe3afce0555690e8ae73ed8`.
- Aggiornamento: `BWA-Desktop-0.6.78-update.zip`, 25.195.228 byte, SHA256 `669eeb351ffc55132897d8c54781c4d40ca6519e4b81f39e0643d728aec7285e`.
- Indice: `bwa-connessione.json`, firma RSA/SHA256 verificata dal programma.

Il controllo del pacchetto confronta tutte le 163 voci con l'indice firmato. Nessun archivio di ristorante, credenziale, token, database operativo o chiave privata incluso. La firma dell'indice di aggiornamento è distinta dalla firma Authenticode: il setup BWA non ha una firma commerciale del produttore.

Verificata anche la compatibilità con l'aggiornatore estratto dal pacchetto pubblico 0.6.74: con il suo codice originale verifica la firma della 0.6.78 ed estrae tutti i file nella cartella di preparazione. Non sono necessari passaggi intermedi.

## Prove superate

| Area | Risultato e confine della prova |
|---|---|
| Regressione | 20 gruppi di verifica del candidato, inclusa la suite generale di 59 controlli. |
| Installazione | 44 verifiche su cartelle nuove nelle quattro lingue: modello iniziale incorporato, archivio pulito, identità, export senza Excel e conservazione di un modello esistente. Dipendenze dell'installer simulate dove indicato. |
| Aggiornamento | Tutti i file corrispondono alla firma; dati, credenziali, modelli e scansioni conservati; copia dei file precedenti presente. Indice, ZIP e staging alterati rifiutati prima della scrittura. |
| Interfaccia | 44 rendering pagina/lingua e 15 cicli espliciti nascondi/ripristina con stati di lavoro attivi. Altri 30 cambi lingua conservano l'input non salvato; p95 446,76 ms sul PC di sviluppo, senza bot di rete attivi. |
| Petty Cash | 23 ticket attivi nella prova di carico; importi attesi indipendenti, ticket misti, bozze incomplete, più scansioni, cancellazione/ripristino, spostamento atomico, originale mensile multipagina, PDF, allegati email senza invio e backup/ripristino. |
| Calcoli | Caso 24 + 36 + 12 TTC al 20%: HT 60, IVA 12, TTC 72; eliminazione e ripristino senza duplicati; modifica a TTC 78. Fatture con IVA mista, note di credito e mismatch segnalati, senza cambiare l'IVA delle vendite. |
| Fatture | Correzioni persistenti dopo reimportazione, eliminazioni non riattivate, conflitti della sorgente, stesso acquisto come documento e pagamento senza doppio costo. |
| Dashboard | Dati assenti distinti da zero, cache per mese, produttività indisponibile senza ore, storico incompleto e confini temporali. |
| Recensioni | Fixture CSV/XLSX: mapping esplicito, duplicati, aggiornamenti, rimozioni, conflitti, mese/ristorante/fonte, date e formule ambigue, limiti dei file. Campioni email reali compatibili: italiano e tedesco già forniti. |
| Consultazione | Fixture separate sorgente/lettore: sola lettura, isolamento tenant, revisione e ordine, dati corrotti, revoca, cache offline, scadenza e riutilizzo del codice, tentativo di nuovo abbinamento senza perdere quello valido. |
| Diagnostica | Cattura e mascheramento, dimensioni e hash, filtraggio, configurazione automatica e opt-out, autenticazione server, isolamento e compatibilità del nome file con il monitor esistente. |
| Bot e script | Contratti dei 14 punti di avvio dei bot coerenti con i parametri PowerShell. Sintassi dei 12 script PowerShell e degli 84 file Python del pacchetto verificata. |

I test di calcolo, scrittura e ripristino utilizzano copie e dati sintetici; non sono state inviate email di chiusura reali.

## Lettura reale dei servizi

La verifica online del candidato 0.6.78 ha completato Nesto (12 valori), Lightspeed (tre report, controlli data/ristorante/totali) e Bomito (lettura del mese). Applicazione del risultato al modello soltanto in memoria: nessuna registrazione contabile del ristorante salvata dalla prova.

Questa prova precede gli ultimi ritocchi a traduzioni, conoscenze di Mini Matteo e client di consultazione. Gli script dei bot e il percorso di lettura sono rimasti invariati; la regressione finale copre l'eseguibile identificato sopra. Non dimostra che ogni account o pagina futura dei fornitori avrà lo stesso comportamento.

Il servizio centrale aggiornato risponde a `/health`; gli endpoint protetti rifiutano richieste prive di credenziali. L'attivazione e il catalogo preesistenti hanno superato le rispettive regressioni locali.

## Prestazioni e AI

PC di sviluppo: Intel Core i7-1360P, 12 core/16 processori logici, circa 15,7 GiB di RAM visibile; Windows 11 Home, build 26200. Ollama 0.34.0. Nei campioni il modello era caricato sulla CPU (`size_vram=0`); la presenza di una GPU nel PC non significa che sia stata usata.

Otto richieste brevi reali, quattro lingue per modello, contesto 8192 e quantizzazione Q4_K_M:

| Modello | Primo testo dall'inizio della richiesta | Durata totale | Generazione |
|---|---|---|---|
| qwen2.5:7b | 18,9–36,8 s | 22,5–49,1 s | 7,8–8,3 token/s |
| qwen2.5:1.5b | 4,4–8,8 s | 5,3–9,5 s | 28–30 token/s |

Il primo caricamento dei rispettivi gruppi ha richiesto 8,66 s e 2,72 s; i campioni successivi hanno riutilizzato il modello. Sono intervalli di pochi campioni locali, non prestazioni garantite. La metrica esterna considera il vero primo testo dall'avvio della richiesta; una metrica interna che parte dopo gli header HTTP non è equivalente.

Le risposte libere hanno mostrato errori anche con 7B. Per le procedure comuni l'app usa guide deterministiche immediate e impedisce alla chat di dichiarare riuscite azioni contabili che non ha eseguito. Il modello ridotto resta una scelta esplicita; non è stata dichiarata risolta o misurata la velocità sul PC della collega.

Interruzione verificata anche contro Ollama reale con prompt sintetici brevi: richiesta concorrente rifiutata, annullamento prima della risposta completato in 8 ms lato applicazione, annullamento dopo il primo testo e richiesta successiva riusciti. È una verifica della cancellazione HTTP e del recupero del client, non una misura del tempo esatto di arresto di ogni elaborazione interna del runtime.

## Prova prolungata

**SUPERATA:** 3600.1 secondi continuativi, 323 campioni. MainWindow reale, archivio sintetico isolato, navigazione, cambi lingua e lavori in background simulati. Nessun bot reale, invio email o salvataggio contabile del ristorante in questa prova.

| Misura | Primo campione | Ultimo campione | Massimo osservato |
|---|---:|---:|---:|
| Working set (MiB) | 108.8 | 160.6 | 200.1 |
| Memoria privata (MiB) | 74.7 | 127.7 | 167.7 |
| Handle | 624.0 | 609.0 | 624.0 |
| Oggetti GDI | 84.0 | 113.0 | 113.0 |
| Oggetti USER | 187.0 | 387.0 | 391.0 |

CPU media del processo: 3.35% di un core, circa 0.21% della capacità dei 16 processori logici; non è la CPU totale del PC. I campioni iniziali precedono il caricamento di tutte le pagine e non rappresentano lo stesso stato del campione finale. Altre verifiche sono state eseguite contemporaneamente su questo PC.

Esito integrale del test: `One-hour synthetic UI/model/job soak completed. seconds=3600.0575702 language_samples=53 language_p95_ms=547.0268 interval_peak_p95_ms=1468. No real service, accounting or email actions.`

Nessun arresto o perdita dell’input non salvato rilevato. Un’ora senza errori non esclude problemi futuri e non dimostra le prestazioni della postazione della collega.

Reattività: inizializzazione della finestra di prova 2.482 ms; p95 dei 53 cambi lingua 547 ms. I picchi di ritardo del timer UI, misurati per intervalli di circa 10 secondi durante navigazione/rendering e catture, hanno p95 1.468 ms e massimo 2.567 ms. Questi picchi indicano pause ancora osservabili nelle operazioni più pesanti: la prova dimostra il completamento senza blocchi permanenti, non un'interfaccia sempre istantanea.

## Verifiche ancora necessarie nell'ambiente destinatario

- Abbinamento reale tra due PC fisici per la consultazione: il servizio e i test sono pronti, ma nessun nuovo collegamento del ristorante è stato attivato durante il collaudo. Occorre un'attivazione centrale BWA valida; il solo vecchio token GitHub non basta.
- Primo errore reale successivo all'aggiornamento per osservare l'intero percorso screenshot → invio privato → lettura in assistenza. I test locali e di autenticazione non sostituiscono questo evento.
- Installazione completa di Ollama/modello su un PC fisico completamente nuovo e misure sul PC della collega.
- Layout Yext non presenti nei campioni e completezza effettiva della casella/export del singolo ristorante.
- Altre risoluzioni e scale DPI non coperte dalle schermate del collaudo. Alle dimensioni ridotte l'interfaccia mantiene lo scorrimento per raggiungere i controlli.

Food Cost sperimentale, voce e personaggio 3D non fanno parte di questa release.
