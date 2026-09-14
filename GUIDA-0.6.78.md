# BWA Desktop 0.6.78 — guida all’aggiornamento

## Aggiornare un PC già configurato

Apri BWA e accetta l’aggiornamento proposto da Mini Matteo, oppure usa **Amministratore → Backup e aggiornamenti → Controlla aggiornamenti**. La 0.6.78 è cumulativa: non occorre installare le versioni intermedie. Il programma verifica firma e contenuto, conserva una copia dei file precedenti e riavvia BWA. Non reinstallare il setup sopra una cartella con dati.

Per una nuova postazione usa `BWA-Desktop-0.6.78-Setup.exe`. Scegli subito la lingua; il modello BWA iniziale è incluso. La preparazione di Ollama e del modello richiede Internet e diversi GB soltanto quando mancano. Ristorante, utilizzatori e accessi si configurano al primo avvio.

## Petty Cash e fatture

Apri **Petty Cash** dalla chiusura o da **Giornata**. Puoi creare più movimenti, aggiungere più ticket a ciascuno e allegare più scansioni allo stesso ticket. Ogni ticket mantiene provenienza, numero e data del documento. La data contabile determina la giornata e il mese in cui viene registrato.

Inserisci importi e aliquote presenti nel documento. Il 20% è disponibile insieme alle aliquote precedenti; non viene scelto automaticamente. Un ticket può avere più aliquote. Le righe incomplete restano in bozza e non contribuiscono agli importi confermati. Un’altra immagine dello stesso ticket non aumenta la spesa.

Modifica, eliminazione e ripristino conservano gli originali. I totali vengono ricalcolati e i documenti precedenti da rigenerare vengono segnalati. In **Chiusura Mese** il modello Excel originale contiene tutti i ticket attivi e prosegue su più pagine. Il PDF riunisce le pagine firmate e i giustificativi.

In **Fatture Bomito** puoi correggere o escludere una fattura. Le scansioni successive mantengono le rettifiche locali; una variazione anche della sorgente viene segnalata per confronto. **Dettaglio IVA** conserva la ripartizione HT/IVA/TTC, anche mista: il WaWi continua a ricevere il netto della categoria, senza scrivere l’IVA acquisti nelle colonne IVA vendite. Se cambia l’importo della fattura, verifica nuovamente il dettaglio.

## Chiusura e attività in corso

Una nuova procedura propone la data odierna del ristorante. Controlla e conferma la data prima di **Cominciamo**, soprattutto per giornate precedenti. La stessa data deve essere usata per report, Nesto, documenti e salvataggio.

La barra inferiore mostra l’attività. Cliccala per aprire il dettaglio dei lavori, con stato, durata ed eventuale errore. **Interrompi** è disponibile solo per le operazioni che possono essere annullate in sicurezza. La minimizzazione conserva il lavoro in corso; il ripristino esplicito da Mini Matteo riapre BWA. **Esci dal programma** conclude le operazioni pendenti prima della chiusura definitiva.

## Mini Matteo e AI locale

Le guide frequenti rispondono senza attendere il modello. La chat libera usa Ollama locale e non può confermare salvataggi, invii o backup senza un risultato del programma.

In **Amministratore → Mini Matteo e AI → Modello AI locale** puoi scegliere `qwen2.5:1.5b`, `qwen2.5:3b` o `qwen2.5:7b`, oltre ai minuti di permanenza in memoria. Un modello più piccolo richiede meno risorse ma può fornire risposte meno accurate. La versione predefinita resta 7B; nessun modello aggiuntivo viene scaricato al solo cambio di scelta. Usa **Prepara AI Mini Matteo** per preparare il modello selezionato quando manca.

**Diagnostica AI → Test** misura una richiesta breve senza dati del ristorante. **Esporta rapporto** conserva versione del runtime, modelli, caricamento CPU/GPU e tempi. Le misure di un PC non dimostrano le prestazioni di un altro.

## Recensioni

Le email Yext già supportate continuano a essere lette dalla casella Outlook configurata. La media riguarda le recensioni importate del mese, non il voto complessivo pubblico. Senza prova di completezza, la copertura resta parziale.

Per un CSV/XLSX usa **Amministratore → Assistenza e diagnostica → Importa export recensioni**. Associa esplicitamente ID stabile, data originale, stelle, fonte Google e ristorante; scegli il formato delle date e il mese. Conferma la completezza soltanto se l’export contiene tutte le recensioni del perimetro, anche senza testo. Righe ambigue o conflitti lasciano invariata la media precedente. Dopo un export completo, importa un nuovo export per riallineare quel periodo.

Non occorrono API recensioni né scraping. Per l’export reale, verifica in Yext ristorante, fonte Google, tutte le stelle, recensioni senza commento e notifiche di aggiornamento. I campioni email verificati sono quelli italiani e tedeschi già forniti; altri layout potrebbero richiedere adattamento.

## Consultazione da un altro PC

Sulla postazione ristorante, **Amministratore → Assistenza e diagnostica → Consultazione da casa** abilita la pubblicazione dei riepiloghi delle chiusure salvate. È necessaria l’attivazione BWA Assistenza tramite codice: una vecchia connessione diretta con token GitHub, da sola, non abilita questa funzione. Non cancellare dati esistenti per tentare una nuova attivazione.

Abilita la pubblicazione e genera il codice di sola lettura `BWAV1`. Sul PC di consultazione apri **BWA Consultazione** dal menu Start, oppure avvia `BWA-Desktop.exe --consultation`, e inserisci il codice. Il codice scade dopo 24 ore; una volta abbinato, l’accesso resta valido fino alla revoca. L’installer normale prepara anche l’AI; il client di sola consultazione non la usa.

Il client mostra lordo, netto, Petty Cash e produttività delle chiusure salvate. Distingue data dei dati, pubblicazione e ultimo contatto. A PC ristorante spento restano gli ultimi dati validi, indicati come non recenti o non raggiungibili. Non sono vendite in tempo reale. Il client non esegue chiusure, bot, email, ripristini o modifiche. Gli accessi si revocano dalla stessa sezione Admin; una sola postazione sorgente è ammessa per ristorante.

## Diagnostica con immagini

Sui PC con connessione privata configurata, gli errori vengono accodati automaticamente con log filtrato e immagine, quando disponibile. Una disattivazione esplicita in Admin viene rispettata. I tentativi non riusciti restano nella coda locale.

La cattura riguarda la pagina del bot con campi oscurati oppure la finestra BWA mascherata. Se non è possibile catturarle, si allega una scheda di contesto chiaramente identificata. Non viene fotografato tutto il desktop. Il servizio accetta anche i PC attivati tramite codice e conserva il formato riconosciuto dall’assistenza. Ricevere un evento non significa che sia già stato analizzato o corretto da una persona.

Il progetto Food Cost teorico, la voce e il personaggio 3D sperimentale rimangono separati da questo aggiornamento.
