Acronimo per Transmission control protocol, è un servizio internet di trasporto dati:
- [[Connection-Oriented]]: setup richiesto tra client e server
- [[Trasporto affidabile TCP]] tra processo mittente e destinatario
- [[Controllo del flusso TCP]]: il mittente non “inonderà” di dati il destinatario. Evita di spedire più dati di quanti il ricevitore sia in grado di trattare
- [[Controllo di congestione TCP]]: “strangola” il mittente quando la rete è sovraccarica e recupera le situazioni in stato di sovraccarico
- Non offre garanzie di timing né di ampiezza minima di banda

Il processo TCP gode di alcune proprietà:

Orientamento allo stream: lunghezza di byte indefinita a priori. Il servizio di consegna dello stream nella macchina di destinazione passa esattamente la medesima sequenza di ottetti che il trasmettitore ha passato al servizio di consegna nella macchina origine. TCP vede i dati come un flusso di byte ordinati ma strutturati

![[Pasted image 20231025112709.png]]

Orientato alla connessione: i processi effettuano un [[Handshake TCP]] prima dello scambio dei dati cioè l'invio di informazioni preliminari per preparare lo scambio dei dati.
Orientato perché lo stato della connessione risiede sui punti terminali e non sugli elementi intermedi della rete.
La connessione è vista dagli applicativi come un circuito dedicato, quindi il TCP è capace di fornire servizi del tipo [[Connection-Oriented]] mentre il [[protocollo]] [[Indirizzo IP|IP]] su cui appoggia è in grado di fornire servizi [[Connection-Less]].

Sfrutta una Connessione Full-Duplex: il flusso dati tra due host può avvenire contemporaneamente nelle due direzioni. Le due direzioni sono slegate. Viene istaurata una connessione punto-punto.

Tramite il [[Concetto di Multiplexing-Demultiplexing]], TCP è in grado di assegnare una data connessione ad un particolare processo.

Il trasferimento dei dati è ordinato e affidabile cioè capace di correggere tutti i tipi di errore quali:
- Dati corrotti
- Segmenti persi
- Segmenti duplicati
- Segmenti fuori sequenza

Il trasferimento dei dati è bufferizzato. Il software del protocollo TCP è libero di suddividere il flusso di byte in segmenti in modo indipendente dal programma applicativo che li ha generati. Per fare questo c'è bisogno di un buffer dove immagazzinare la sequenza di byte. Appena i dati sono sufficienti per riempire un segmento ragionevolmente grande, questo viene tramesso attraverso la rete.
La bufferizzazione consente una riduzione del traffico sulla rete "ottimizzando" in qualche modo il numero di segmenti da trasmettere.

![[Pasted image 20231025114054.png]]

I processi a livello applicativo scrivono e leggono byte nel/dal buffer e questo può avvenire a velocità diverse.
Il flusso di byte viene partizionato in [[Segmento TCP|segmenti TCP]], ognuno con il suo header, che viene consegnato al livello IP.

La chiusura della connessione avviene quando client e server chiudono ciascuno il loro lato della connessione inviando un segmento TCP con bit _FIN_ = 1. Ciascuno risponde al *FIN* ricevuto con un *ACK* combinato con il proprio *FIN*. Possibile anche lo scambio simultaneo di *FIN*.

![[Pasted image 20231025124431.png]]

*TIME_WAIT* è lo stato finale in cui il capo di una connessione che esegue la chiusura attiva resta prima di passare alla chiusura definitiva della connessione ed è lungo due volte la MSL (Maximum Segment Lifetime) cioè la stima del massimo periodo di tempo che un pacchetto IP può vivere sulla rete. Questo tempo è limitato perché ogni pacchetto IP può essere ritrasmesso dai [[Router]] un massimo di volte (detto hop limit).
Lo stato *TIME_WAIT* viene utilizzato dal protocollo per due motivi principali:
- Implementare in maniera affidabile la terminazione della connessione in entrambe le direzioni. Se l'ultimo _ACK_ viene perso, chi esegue la chiusura passiva manderà un ulteriore _FIN_ e chi esegue la chiusura attiva dovrà mantenere lo stato della connessione per poter rinviare l'_ACK_ 
- Consentire l'eliminazione dei segmenti duplicati in rete

Il calcolo del timeout (RTO) è fondamentale per il funzionamento di TCP. Prima di tutto il RTO deve essere maggiore del Round Trip Time (RTT) cioè il tempo trascorso da quando si invia un segmento a quando se ne riceve il riscontro.
Viene calcolato analizzando gli RTT dei segmenti non ritrasmessi ($SampleRTT$ stimato per un segmento trasmesso e non per ogni invio).
$$Estimed RTT = (1-\alpha)*EstimedRTT + \alpha*SampleRTT$$
$SampleRTT$ può fluttuare.
Si considera $EstimatedRTT$ la combinazione dei precedenti valori di $EstimatedRTT$ con il nuovo valore $SamleRTT$.
Il valore di $\alpha$  viene posto a $1/8$ in modo da rendere via via meno importanti gli RTT dei pacchetti più vecchi. Quindi: $$EstimatedRTT = 0.875*EstimatedRTT+0.125*SampleRTT$$
Oltre al valore $RTT$ stimato è necessario anche una stima della **variabilità** di $RTT$ data dalla seguente formula: $$RTT_{DEV}=(1-\beta)RTT_{DEV}+\beta|RTT_{SAMPLE}-RTT_{ESTIMED}|$$
Stima di quanto $SampleRTT$ si discosta $EstimatedRTT$. Il valore di $\beta$ viene posto a $1/4$. Una volta ottenuti questi valori, il timeout viene normalmente calcolato come: $$RTO=RTT_{ESTIMATED} + 4RTT_{DEV}$$
I dati inviati dal processo a livello applicativo sono mantenuti nel buffer di invio.
La trasmissione dei dati si basa sulla finestra di trasmissione (sliding window):
- Finestra sovrapposta sulla sequenza da trasmettere
- Negoziata dinamicamente
- Viene fatta avanzare alla ricezione di un ACK

![[Schermata 2023-11-09 alle 19.38.28.png]]

Come sua controparte c'è il buffer di ricezione che riceve dati con la stessa modalità.