Chiamato anche Handshake a tre vie, consiste in tre scambi di messaggi prima di per poi iniziare una comunicazione tra [[client]] e [[server]]. Diviso in 3 fasi:
1. Il client invia una richiesta di [[connessione]] ad un server TCP attraverso un [[Segmento TCP]] con SYN attivo ma che non contiene dati. Viene trasmesso anche un numero di sequenza iniziale (ISN)
2. Il server estrae il segmento, alloca i buffer e le variabili TCP per la connessione ed invia in segmento di connessione garantita al client (chiamato SYNACK). Sono attivi SYN e ACK con l'ultimo byte ricevuto.
3. Il client alloca buffer e variabili di connessione e manda un riscontro positivo del messaggio del server in cui SYN è inattivo che significa che può iniziare lo scambio di dati.

![[Pasted image 20231025121923.png]]

Dopo l'handshaking a [[livello di trasporto]] non c'è più distinzione tra client e server.
I primi segmenti non hanno carico utili. All'arrivo del primo segmento il server inizializza due buffer e le variabili, necessari per il controllo del flusso e della congestione. All'arrivo del riscontro del primo segmento il client alloca due buffer e le variabili, necessari anche questi per il controllo del flusso e della congestione. Alla ricezione del terzo segmento la connessione è instaurata. 