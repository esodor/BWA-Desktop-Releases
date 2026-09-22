# Verifiche BWA Desktop 0.6.92

- Riprodotto il rifiuto prematuro della 0.6.91 con conti disponibili dopo alcune letture; il nuovo controllo attende e prosegue.
- Quattro scenari della funzione di attesa: pagina pronta, caricamento ritardato, pagina sempre vuota con termine a 20 secondi, disconnessione. Nessuna operazione su browser reali.
- Otto scenari sul blocco effettivo di lettura, ripetuti sullo script estratto dal pacchetto: confronto con la base, recupero del ritardo, lettura immediata, rifiuto di pagina vuota, mese errato, vista non valida, conto presente ma illeggibile, disconnessione.
- Verificato che le altre istruzioni del bot restano identiche: nessuna modifica ai controlli di ristorante o agli importi.
- Pacchetto completo: 376 file, sintassi di 290 Python e 15 PowerShell verificata. Rispetto alla 0.6.91 cambiano solo l'eseguibile con la nuova versione e lo script Bomito; gli altri 374 file sono identici.
- Audit di esclusione di credenziali, database, documenti e log privati superato. Risorse incorporate e payload dell'installer verificati.

- Firma del nuovo canale verificata dai client 0.6.85 e 0.6.92. Otto controlli di aggiornamento superati, inclusi conservazione dei dati simulati, rollback e rifiuto dei pacchetti alterati.
- Superati 44 controlli di nuova installazione nelle quattro lingue, inclusa esportazione BWA senza Excel.
- Scansione Microsoft Defender completata senza rilevamenti associati al pacchetto.

Limiti: test con pagina simulata, senza accesso reale a Bomito. Le schermate storiche mostrano conti assenti ma non provano se sarebbero comparsi entro 20 secondi. La pubblicazione non costituisce verifica della risoluzione su quei PC.
