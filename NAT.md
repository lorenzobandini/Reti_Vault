Acronimo di Network Address Translation permette di trasmettere su Internet il traffico proveniente da sistemi attestati su sottoreti private, in cui sono assegnati indirizzi IP
privati.
L'accesso di una rete privata su Internet è realizzato attraverso un router abilitato alla NAT, questo router ha almeno un indirizzo IP pubblico.
Tutto il traffico in uscita dal router di accesso ha un indirizzo IP sorgente pubblico, quello del router mentre tutto il traffico in ingresso alla sottorete ha come indirizzo IP di destinazione l’indirizzo pubblico del router di accesso.

Il router di accesso ha in memoria una tabella di traduzione NAT, le cui righe contengono le associazioni (IP privato, Porta)(IP pubblico e porta assegnata dal router).

![[Pasted image 20231129113225.png]]

