Ogni imposta buffer di invio e di ricezione. Il [[processo]] applicativo destinatario legge i dati dal buffer di ricezione ma non necessariamente nell'istante in cui arrivano.

Per controllo di flusso si intende la capacità del mittente di evitare la possibilità di saturare il buffer del ricevitore.

Il controllo di flusso mette in relazione la frequenza di invio del mittente con la frequenza di lettura dell'applicazione ricevente.

[[TCP]] implementa questa caratteristica tramite una variabile detta **finestra di ricezione** (_rwnd_) mantenuta nel mittente. Questa variabile fornisce un'idea di quanto spazio è ancora a disposizione nel buffer del ricevitore. 

Il destinatario TCP comunica la capacità residua nel buffer di recezione tramite il campo _rwnd_ field nell'header TCP. La variabile _rwnd_ è dinamica e si calcola con: $$rwnd=RcvBuffer-(LastByteReceived-LastByteRead)$$
Il mittente limita la quantità di dati unACKed al valore ricevuto di _rwnd_.
Si assicura inoltre che: $$LastByteSent-LastByteAsked\leq rwnd $$
Se $rwnd=0$, il mittente manda segmenti "sonda" di 1 byte per ricevere l'aggiornamento sulla dimensione di _rwnd_

![[Pasted image 20231110105146.png]]


