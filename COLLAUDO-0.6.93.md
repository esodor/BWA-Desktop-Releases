# Verifiche BWA Desktop 0.6.93

- Riprodotta la perdita del messaggio precedente attraverso entrambi i filtri reali dell'applicazione; il nuovo testo statico supera i filtri senza includere dati di accesso.
- Confermati tre tentativi e tempi invariati. Otto confronti con la versione precedente: pagina pronta, accesso riuscito, scelta ambigua, disconnessione, browser visibile, accesso non configurato, automatismo disattivato e clic non riuscito.
- Sette righe sintetiche contenenti categorie di dati sensibili restano rimosse. Entrambi i sorgenti dei filtri sono identici alla versione precedente.
- Prove ripetute sullo script estratto dal pacchetto finale. Nessun browser reale, accesso a credenziali o collegamento Bomito durante i test.
- Pacchetto completo di 376 file: cambiano soltanto eseguibile con nuova versione e script Bomito; altri 374 file identici. Verificate sintassi di 290 Python e 15 PowerShell, risorse incorporate, payload installer ed esclusione di dati privati.

- Firma del nuovo canale verificata dai client 0.6.85 e 0.6.93. Otto controlli di aggiornamento superati, inclusi conservazione dei dati simulati, rollback e rifiuto di pacchetti alterati.
- Superati 44 controlli di nuova installazione nelle quattro lingue; scansione Microsoft Defender completata senza rilevamenti associati al pacchetto.

Limiti: le prove verificano il messaggio e la conservazione del comportamento, non la causa o la risoluzione di un accesso reale fallito.
