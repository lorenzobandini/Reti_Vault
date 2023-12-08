Un segmento può essere smarrito o corrotto. [[TCP]] crea un servizio di trasferimento dati affidabile sul servizio inaffidabile di IP mediante l'utilizzo di Checksum, controlli obbligatori che scartano segmenti corrotti e dei riscontri, processi di conferma della ricezione dei dati da parte del destinatario. In particolare il riscontro funziona che dopo aver ricevuto ciascun segmento, il destinatario invia un messaggio di riscontro _ACK_ al mittente per confermare la ricezione corretta del [[Segmento TCP]]. Questo messaggio di riscontro contiene il numero di sequenza del prossimo segmento che il destinatario si aspetta di ricevere. Questo processo assicura che i dati siano stati ricevuti senza errori.

![[Pasted image 20231027152809.png]]

Un metodo di trasporto che permette di aumentare la produttività è il metodo **Pipeline** in cui il mittente può inviare più segmenti senza attendere riscontro. 

![[Pasted image 20231025144425.png]]

Gli eventi **lato mittente** sono:
- TCP riceve i dati dall'applicazione
- Incapsula i dati in uno o più segmenti e assegna numero di sequenza
- Avvia il timer di ritrasmissione (Timeout di ritrasmissione - RTO , il timer viene avviato se non è già in funzione per un qualche altro segmento)

La ritrasmissione avviene in caso di:
- Timeout: ritrasmette il segmento che non è stato riscontrato e che ha causato il timeout e il timer viene riavviato
- Ricezione di tre *ACK* duplicati: se il mittente riceve tre *ACK* duplicati, il segmento successivo a quello riscontrato è andato perso. Quindi viene fatta una ritrasmissione veloce prima della scadenza del timer.

I dati a volte possono arrivare fuori sequenza ed essere temporaneamente memorizzati dall'entità TCP destinataria. Il TCP non dice come il destinatario deve gestire i pacchetti fuori sequenza dipendentemente dall'implementazione.
Nelle versioni più recenti si implementa la Selective _ACK_ (_SACK_), i pacchetti ricevuti fuori sequenza vengono memorizzati e il riscontro di pacchetti fuori sequenza e duplicati viene inviato in _[[OPTIONS]]_

![[Pasted image 20231025145713.png]]


In lato destinatario:
- Tutti i segmenti inviati per trasmettere dati includono _ACK_
- Se destinatario non ha dati da inviare e riceve segmento "in ordine" ritarda invio di _ACL_ di 500ms a meno che non riceva nuovo segmento
- Se destinatario riceve segmento atteso e precedente non è stato riscontrato allora invia immediatamente _ACK_
- Se destinatario riceve segmento fuori sequenza oppure mancante oppure duplicato allora invia un segmento _ACK_ indicando il prossimo numero atteso

![[Pasted image 20231025145732.png]]