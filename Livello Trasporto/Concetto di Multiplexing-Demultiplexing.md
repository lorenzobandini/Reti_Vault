Lo [[strato]] trasporto provvede allo "smistamento" dei pacchetti e le applicazioni seguendo il concetto di demultiplexing per dirigere ogni pacchetto dati che riceve in un processo.

![[Pasted image 20231023134930.png]]

Lo strato trasporto provvede anche all'"accorpamento" dei flussi dati dai processi verso la rete seguendo il concetto di multiplexing. 

Le operazioni di multiplexing e demultiplexing si basano sui socket address dei processi. Il socket address è identificato dalla combinazione [[Indirizzo IP]] e numero di [[Porta]].

Il demultiplexing funziona con l'[[host]] che riceve il [[datagramma IP]], ogni datagramma ha Indirizzo IP sorgente e Indirizzo IP destinatario e trasportano un segmento del [[livello di trasporto]] e un numero di porta sorgente e destinazione contenuti dell'header.

![[Pasted image 20231023135527.png]]

Ogni comunicazione di trasporto ([[TCP]] o [[UDP]] che sia) è identificata in maniera univoca grazie alle coppie [[Indirizzo IP]]/[[Porta]] degli host.

Il demultiplexing fatto senza connessione avviene attraverso il protocollo UDP. Lo strato di trasporto dell'host ricevente consegna il segmento UDP alla socket identificata da IP e porta destinazione. Il socket UDP è identificato dalla coppia (IP/Porta). I datagrammi con IP e/o porta mittente differenti ma stessi IP e porta destinatari vengono consegnati alla stessa socket.

![[Screenshot 2023-10-23 140922.png]]

Il demultiplexing orientato alla connessione avviene attraverso il protocollo TCP connessa è identificata da 4 parametri:
- Idirizzo IP di origine
- Numero di porta di origine
- Indirizzo IP di destinazione
- Numero di porta di destinazione

L'host ricevente usa i 4 parametri per inviare il segmento alla socket appropriata. Un host server può supportare più socket contemporanee.

![[Pasted image 20231023141812.png]]

Tra i vari livelli dello stack le interfacce dei livelli saranno quindi:

![[Pasted image 20231023142214.png]]