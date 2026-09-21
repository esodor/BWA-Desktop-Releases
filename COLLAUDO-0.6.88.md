# Verifiche 0.6.88

- Modulo generico senza seed finanziari: nessun inventario iniziale o risultato del ristorante nel pacchetto. Prezzi precompilati delle ricette rimossi: i costi derivano dai dati della postazione.
- Test con il Python incluso: installazione nuova richiede inventario; sincronizzazione senza apertura respinta; ristorante e mese errati respinti; inventario valido acquisito; sostituzione non valida non altera la precedente; mese successivo richiede un'altra apertura.
- Ricalcolo con report già acquisiti e copie isolate dei carichi: completato, periodo verificato. Periodo report incoerente respinto conservando il risultato precedente. Le fonti reali sono state aperte in sola lettura; nessun dato operativo modificato.
- Importazione e sincronizzazione sono protette da un lock esclusivo; le generazioni precedenti restano conservate. Il modulo non importa vecchi seed lasciati da una precedente installazione locale.
- Interfaccia renderizzata nelle quattro lingue; verificata richiesta inventario mancante e spazio dei pulsanti.
- Pacchetto 376 file, controllo hash/percorsi/segreti e sintassi di 290 file Python superati. Risorse incorporate confrontate con la base pubblica verificata.
- Feed firmato verificato dai client 0.6.85 e 0.6.88; setup incorpora lo stesso ZIP. Test aggiornamento e installazione pulita nelle quattro lingue superati.
- Microsoft Defender sul pacchetto finale: nessuna minaccia rilevata. Nessuna modifica delle protezioni.

Limiti: il recupero live Lightspeed non è stato ripetuto in questo collaudo; sono stati riutilizzati report già acquisiti. La stima mantiene le lacune delle ricette e conversioni come dati da verificare. Le configurazioni dei singoli ristoranti restano necessarie.
