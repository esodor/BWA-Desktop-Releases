# BWA Desktop 0.6.98

- I PC collegati a Hetzner usano il servizio AI centrale per chat, analisi e bozze: RunPod principale, Ollama sul server come riserva. Le conversazioni mantengono il contesto preparato dal desktop. I PC non collegati conservano il trasporto precedente.
- Telegram e desktop riconoscono meglio formule come «potresti controllare le mail», «puoi farmi la chiusura di ieri», «cosa manca per la giornata di ieri». Una richiesta di chiusura senza data chiede quale giornata, senza avviarla.
- La chat desktop accede ai controlli esistenti di giornata, mese, standard, attività e newsletter già analizzate. Chiusure ed email usano le finestre locali; conferme e autorizzazioni restano obbligatorie.
- Il percorso Telegram centrale non chiede il token: spiega il collegamento al ristorante e alla chat da verificare. L'associazione resta necessaria; l'aggiornamento non trasferisce automaticamente la chat da un PC a un altro.
- Corretto il primo collegamento HTTPS e resa coerente la diagnostica con il fornitore AI effettivo. Una richiesta annullata dal desktop non avvia inutilmente l'AI di riserva.

Aggiornare da Admin → Controlla aggiornamenti → Installa. BWA e Outlook rimangono sul PC; per le operazioni remote BWA deve restare aperto. Nessun invio email automatico, nessuna prenotazione reale senza collegamento al gestionale. Conservata la correzione Food/Beverage della 0.6.97.
