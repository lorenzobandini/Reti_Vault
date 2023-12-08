Il [[router]] è un dispositivo che accetta pacchetti in entrata da una delle porte di input (interfacce) e usa una tabella d'inoltro per trovare la [[porta]] di output dalla quale inviare il pacchetto.

I componenti sono:
- Porte in input
- Porte di output
- Processore di [[routing]]
- Switching fabric (struttura di [[commutazione]])

![[Pasted image 20231201122938.png]]

Le porte di input ricevono bit su un collegamento e vengono inoltrati grazie ad una copia della tabella di inoltro per determinare la porta in output. Se la velocità con cui arrivano i datagrammi supera la velocità di inoltro nella struttura di commutazione, vengono messi in coda in un buffer.

La struttura di commutazione trasferisce il pacchetto dal buffer di input al buffer di output appropriato e la velocità di commutazione è la velocità con cui i pacchetti possono essere trasferiti dagli ingressi alle uscite. La strutture possibili possono essere:
![[Pasted image 20231201123726.png]]

Le porte di output utilizzano il buffering per quando i datagrammi arrivano dalla struttura di commutazione ad una velocità maggiore della [[velocità di trasmissione]] sul collegamento di uscita e inoltre utilizzano lo scheduling per definire l'ordine di trasmissione dei datagrammi.

Si possono formare code di pacchetti sia presso le porte di ingresso che sulle porte di uscita e ciò dipende da quantità di traffico sulla rete e le velocità relative della struttura di commutazione e della linea