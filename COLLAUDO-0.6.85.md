# Verifica BWA Desktop 0.6.85

La release usa lo stesso eseguibile 0.6.85 verificato e installato sul PC di sviluppo dopo l'annullamento della funzione Outlook della 0.6.86. I lettori e i bot restano quelli del pacchetto pubblico 0.6.80, inclusa la correzione dei budget Belval e Kirchberg.

Verifiche effettuate sulla candidata:

- 65 controlli del riconoscimento dei promemoria, degli orari e dei chiarimenti nelle quattro lingue.
- 44 controlli di agenda, separazione degli utilizzatori, persistenza cifrata e password personali.
- 41 controlli dei comandi di chiusura, delle date, delle conferme e della protezione dai doppi avvii, con scaricamento e analisi sostituiti da dati sintetici.
- 5 controlli della schermata reale di accesso con password.
- 14 controlli della chat e delle notifiche reali di Mini Matteo su un archivio sintetico, compresa la notifica con la finestra principale nascosta.
- Scansione dei 164 file del pacchetto: elenco consentito e hash coerenti, nessun archivio, email, database, credenziali, chiave privata o percorso personale noto. Sintassi verificata per gli 85 file Python.
- Firma dell'indice verificata sia dal client 0.6.80 sia dal client 0.6.85. Il payload dell'installer corrisponde al pacchetto di aggiornamento. Modello iniziale, icone, animazioni, moduli e chiavi pubbliche invariati rispetto alla precedente release.
- 9 verifiche del percorso di aggiornamento: applicazione del pacchetto firmato, corrispondenza dei file, backup della versione precedente, conservazione di archivio, credenziali, modelli, scansioni, agenda, memoria e password; rifiuto di indice, pacchetto o file preparati alterati.
- 44 verifiche di nuova installazione nelle quattro lingue: modello iniziale pulito, nessun destinatario email preimpostato, identità del ristorante, esportazione BWA senza Excel e conservazione del modello esistente.

Totale delle suite funzionali elencate: 222 controlli superati, oltre alle verifiche di firma, risorse e contenuto del pacchetto. Rispetto alla 0.6.80, nel pacchetto cambia soltanto l'eseguibile BWA; lettori e bot sono identici.

I test dei comandi di chiusura usano servizi simulati: non rappresentano un nuovo collaudo live di Lightspeed, Nesto, Bomito o Outlook. La verifica del pacchetto non può garantire che tutti i profili esterni e i PC dei ristoranti siano configurati correttamente.
