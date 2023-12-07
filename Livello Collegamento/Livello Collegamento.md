Il livello collegamento muove i datagrammi da un nodo al nodo adiacente su un singolo link di comunicazione.

![[Pasted image 20231201143340.png]]

I termini usati sono:
- Host e Router sono i nodi
- Canali di comunicazione che collegano nodi adiacenti lungo un cammino sono collegamenti (link) e possono essere cablati o wireless
- Unità dati di livello 2 cioè i frame che incapsulano un datagramma

Un datagramma può essere gestito da diversi protocolli su collegamenti differenti e anche i servizi erogati dai protocolli del livello di link possono essere differenti.

I collegamenti possono essere:
- Punto-Punto: collegamento dedicato a due soli dispositivi come [[Wide Area Network (WAN)|WAN]] o switched [[LAN|LAN]] ethernet
- Broadcast: collegamento condiviso tra più dispositivi. Quando un nodo trasmette un frame, il canale lo diffonde e tutti gli altri nodi ricevono una copia come Wireless [[LAN|LAN]] 

I servizi solitamente offerti sono:
- Framing
- Consegna affidabile
- Controllo di flusso
- Rilevazione degli errori
- Correzione degli errori

Il livello collegamento è suddivisibile in due sottolivelli:
- Data-Link Control che si occupa del framing e del flow and error control
- Medium Access Control che si occupa dell'accesso al mezzo e impone le regole per accede al mezzo

Queste funzioni sono implementate sia a livello di software eseguite dalla CPU e anche dalla scheda di rete. Le cose tipicamente eseguite in software dalla CPU sono:
- Assemblare le informazioni di indirizzamento attivando il controller
- Risponde agli interrupt del controller, gestisce gli errori e passa il datagramma a livello di rete

La comunicazione tra adaptor avviene con:
- Lato mittente: incapsulamento del datagramma in un frame, aggiungendo error checking bits, rdt, flow control e altro
- Lato destinatario: Controllo errori, rdt, flow control e successivamente estrazione del datagramma da passare al livello superiore

![[Pasted image 20231201144544.png]]

Per permettere di regolare l'accesso condiviso ad un nodo esistono dei protocolli con algoritmi distribuiti che determinano come i nodi condividono il canale e quando il nodo può trasmettere per evitare collisioni.

In un protocollo di accesso multiplo ideale in cui abbiamo un canale broadcast con rate $R$ bps vogliamo:
- Quando un solo nodo tramette, può inviare dati con un rate di $R$ bps
- Quando $M$ nodi vogliono tramettere, ciascuno trasmette ad un rate medio di $\frac{R}{M}$
- Decentralizzato
- Semplice

I protocolli usati sono i [[Protocolli MAC]] 

Un indirizzo del livello collegamento è chiamato indirizzo fisico o [[Indirizzo MAC]] o indirizzo MAC. 

Il livello di collegamento sfrutta come mezzo di trasporto [[Ethernet]], [[Switch]] e [[VLAN]].

I repeater operano solo a livello fisico e rigenerano il segnale che ricevono mentre gli hub sono semplicemente dei repeater multi-porta.
Repeater e hub non hanno alcuna capacità di filtraggio.