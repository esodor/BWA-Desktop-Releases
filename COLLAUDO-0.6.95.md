# Verifiche BWA Desktop 0.6.95

Verifiche eseguite il 25 settembre 2026 sul pacchetto pubblico.

- Firma dei feed GitHub e Hetzner verificata con la chiave pubblica incorporata. Il client pubblicato 0.6.93 accetta il feed firmato di passaggio alla 0.6.95.
- Pacchetto di 377 file derivato dal pacchetto pubblico 0.6.93 verificato tramite SHA-256, con sostituzione dell'eseguibile e quattro file del lettore Food Cost. Risorse pubbliche e modello iniziale pulito conservati.
- Esclusi archivi operativi, credenziali, chiavi private e risorse modello private. Sintassi di tutti i file Python verificata. Microsoft Defender: nessuna minaccia rilevata.
- 44 controlli di nuova installazione nelle quattro lingue, apertura con archivio iniziale vuoto ed esportazione senza Excel superati.
- Aggiornamento provato su un'installazione sintetica: conservati archivi, modelli, configurazioni, collegamento Hetzner, impostazioni AI protette e dati HR. Verificato il ripristino dopo aggiornamento. Pacchetto, manifest e area temporanea alterati vengono rifiutati.
- Controllati HTTPS, host e percorso ammessi per gli aggiornamenti; rifiutati host simili, porte diverse e URL non consentiti.
- Superati i controlli esistenti BWA, Mini Matteo, routine, trasporto AI, HR/Salari, bozze e inbox. Incluse verifiche di disconnessione e arresto dei controlli email. Superati i sei controlli Python per gli scarti Food Cost.

## Limiti del collaudo

I test usano archivi e messaggi sintetici: non sono un invio reale di email né una prova operativa su tutti i PC dei ristoranti. La comparazione del modello BWA mantiene le 31 differenze XLOOKUP già note sulle 4.338 formule, senza introdurre una certificazione contabile.

Backup Hetzner e AI richiedono configurazioni private per ciascun PC. Il pacchetto non contiene dati Belval, token RunPod o collegamenti personali. L'installazione automatica su tutti i PC non è stata eseguita. Il completamento del trasferimento degli altri servizi GitHub resta un'attività distinta.

SHA-256 aggiornamento:
`5e77068e84a451c60c2f92884fce8e5c75d910583415ba6c703482fb22fde0e1`

SHA-256 setup:
`5d049600011466628274d3051f42a5203d843ea97eaf8712f655383810d94510`
