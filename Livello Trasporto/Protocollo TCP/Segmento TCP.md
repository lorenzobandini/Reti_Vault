Partizioni del flusso di byte inviati nel buffer.
TCP numera i byte, anziché i segmenti ed associa un **numero di sequenza** ad ogni segmento che è uguale al numero (nel flusso) del primo byte del segmento. In genere si parte a contare da un initial sequence number generato in modo casuale (e quindi $\neq$ 0).
Il **numero di riscontro** _(Ack, "acknowledgment" )_ è il numero dell'ultimo byte correttamente ricevuto +1 ($Ack=y$ vuol dire che ho aspetto byte $y$ ed ho ricevuto tutti i byte fino a $y-1$ incluso).

Header del segmento:

![[Pasted image 20231025115252.png]]
Il numero di sequenza, numero di riscontro e la finestra permettono il **flow control**, il meccanismo di ritrasmissione ed il riordino dei pacchetti in ricezione, necessari per la struttura stream-based del TCP.
In particolare:
- [[Porta]] (16 bit): numeri di porta della comunicazione
- **Numero di sequenza** (32 bit): è il numero di sequenza nello stream del primo byte di dati di questo segmento. Se il flag $SYN$ è settato, il numero di sequenza è $ISN$ (Initial Sequence Number) e il primo byte di dati è $ISN+1$
- **Numero di riscontro** (32 bit): se il bit $ACK$ è settato, questo campo contiene il valore del prossimo numero di sequenza che il mittente del segmento si aspetta di ricevere dall'altro host. Una volta che la connessione è stabilita è sempre inviato.
- **HLEN** (4Bit): lunghezza dell'header TCP espressa in parole da 4 byte (la lunghezza dell'header può variare tra 20 e 60 byte)
- **Bit codice** sono 6 flag e servono per:
	- **URG**: il campo Puntatore Urgente è significativo e ci sono dati da trasferire in via prioritaria
	- **ACK**: Il campo Numero di Riscontro contiene dati significativi
	- **PSH**: Funzione Push (trasferimento immediato dei dati in un segmento dal trasporto al livello applicativo)
	- **RST**: Reset della connessione
	- **SYN**: Sincronizza il Numero di Sequenza
	- **FIN**: Non ci sono altri dati dal mittente - Chiusura della connessione
- **Finestra di ricezione** (16 bit): indica il numero di byte di dati a partire da quello indicato nel campo Numero di Riscontro che il mittente di questo segmento è in grado di accettare. Serve per il controllo del flusso.
- **Checksum** (16 bit): checksum dell'intero pacchetto (dati, header TCP + parte dell'header IP) per rilevare errori (alteramenti del segmento). Si calcola come per UDP, ma per TCP è obbligatorio.
- **Opzioni** (facoltativo, lunghezza variabile fino a 40 byte): negoziazione di vari parametri. Le opzioni sono sempre multipli di 8 bit e il loro valore è considerato per il calcolo della checksum.
- **Puntatore Urgente** (16 bit): offset positivo a partire dal Numero di Sequenza del segmento corrente. Interpretato solo se il bit URG è uguale ad 1. Punta al primo byte di dati non urgenti a partire dal Numero di Sequenza e consente di far passare i dati urgenti in testa alla coda di ricezione. Nel segmento contenente dati urgente deve essere presente almeno un byte di dati.