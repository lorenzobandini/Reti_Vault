MTU (Maximum Transfer Unit) è la quantità massima di dati trasportata dal protocollo di collegamento. La MTU pone un limite alla lunghezza dei datagrammi IP e tratte diverse possono porre limiti differenti.

![[Pasted image 20231122123628.png]]

Perciò occorre il meccanismo di frammentazione. Se il router riceve un datagramma la cui dimensione supera l'MTU della rete verso cui deve inoltrare quel datagramma Ip in due o più datagrammi più piccoli detti frammenti.
Il riassemblaggio viene effettuato dall'entità rete nel sistema terminale (destinazione).

I frammenti possono arrivare fuori ordine e il livello di rete si occupa a ricomporti tramite:
- Identificatore (16 bit): è associato al datagramma dell'host sorgente. Associato a IP sorgente e IP destinazione identifica quel datagramma in un intervallo di tempo ragionevolmente lungo. I frammenti di quel datagramma mantengono il valore di questo campo. il destinatario riconosce i frammenti che vanno assemblati insieme.
- Offset (13 bit): indica la posizione relativa come multiplo di 8 byte. Serve ad ordinare i frammenti nell'assemblaggio. I frammenti devono essere multipli di 8 byte e il primo frammento ha offset 0.
- Flag (3 bit): serve per indicare l'ultimo frammento
	- il bit 0 è riservato e consideriamo sia sempre 0
	- il bit 1 è _do not fragment_ e vale 0 se il pacchetto può essere frammentato e1 se il pacchetto non deve essere frammentato