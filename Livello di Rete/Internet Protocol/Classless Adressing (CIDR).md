Il Classless Adressing, noto anche come CIDR (Classless Inter-Domain Routing), è un sistema di assegnazione degli indirizzi IP che invece di assegnare automaticamente un blocco di indirizzi IP basato sulla classe della rete, CIDR consente di assegnare una "maschera di rete" che indica quanti bit dell'[[indirizzo IP]] rappresentano la rete stessa. La notazione CIDR usa il formato "indirizzo IP/maschera di rete", dove la maschera di rete indica quanti bit sono dedicati alla parte di rete e quanti alla parte di [[host]].

![[Pasted image 20231124143006.png]]

Un indirizzo diventa del tipo  `a.b.c.d/n`, dove gli `n`  bit più a sinistra costituiscono la parte di indirizzo di rete.
La maschera di sottorete è numero composto da 32 bit in cui i primi `n` bit a sinistra sono imposti a 1 e i rimanenti a 0 e serve per distinguere quale parte di un indirizzo IP identifica la rete e quale l'host.
Se tra due indirizzi, i primi `n` bit sono uguali, vuol dire che appartengono alla stessa rete.
