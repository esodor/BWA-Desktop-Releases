# Verifiche BWA Desktop 0.6.91

- Riprodotte quattro divergenze sulla versione precedente: argomenti equivalenti completamente quotati rifiutati, profilo duplicato accettato, porta duplicata accettata, percorso con spazi non quotato accettato. Baseline: 15/19 controlli superati.
- Correzione: 19/19 controlli superati per ciascuna delle tre configurazioni di porta/profilo Nesto, Bomito e Lightspeed, per un totale di 57. Nesto ordinario e salari condividono la medesima configurazione e funzione.
- Confermata con il parser nativo Windows l'equivalenza degli argomenti quotati. Verificati processo diverso, profilo diverso, porta diversa, prefissi, duplicati, comando vuoto, metadati mancanti, assenza del listener e reset del solo processo posseduto. Operazioni di rete e sui processi sostituite con simulazioni: nessun browser reale avviato o terminato.
- Patch limitata al riconoscimento degli argomenti; confronto testuale conferma che le funzioni successive del file condiviso sono identiche alla base 0.6.90.
- Audit del pacchetto: 376 file e sintassi di 290 Python; solo programma e bots/AccessConfig/BrowserWindow.ps1 differiscono dalla 0.6.90. Risorse incorporate confrontate con la base pubblica verificata.

- Superati i controlli di firma del canale aggiornamenti, integrita del payload incorporato nell'installer e sintassi degli script PowerShell inclusi.
- Superati gli otto controlli di aggiornamento su installazione simulata: conservazione dei dati, copia di ripristino e rifiuto dei pacchetti alterati prima di modificare l'installazione.
- Superati 44 controlli di nuova installazione, incluse le quattro lingue e l'esportazione BWA senza Excel.
- Scansione Microsoft Defender della cartella di distribuzione completata senza rilevamenti associati.

Limiti: nessun login reale o flusso operativo su un PC remoto ripetuto. Le command line dei vecchi incidenti Nesto non sono presenti nei report; la correzione del difetto riprodotto non prova che fosse la causa di quegli incidenti.
