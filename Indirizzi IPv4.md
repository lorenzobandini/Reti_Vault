Gli indirizzi IP sono costituiti da 32 bit (4 byte), rappresentati in notazione decimale puntata.

![[Pasted image 20231124141759.png]]

Ogni host ha un indirizzo univoco diviso in due parti, Network ID + Host ID, che identificano una rete IP su internet e l'host su quella rete IP,

![[Pasted image 20231124141852.png]]

In passato, quando è stato introdotto il sistema di indirizzamento IP, gli indirizzi IP erano assegnati in classi, e ciò è noto come "Classful addressing". Questo sistema divideva gli indirizzi IP in cinque classi principali: Classe A, Classe B, Classe C, Classe D; Classe E (gli ultimi 2 straordinari per ambiti speciali). Ogni classe aveva un intervallo specifico di indirizzi IP e un diverso numero di bit dedicati alla parte di rete e alla parte di host. 

![[Pasted image 20231124141959.png]]

In particolare:
- Classe A (7 bit per 128 reti IP, 24 bit): Reti di 16 milioni di host, da 0.0.0.0 a 127.255.255.255
- Classe B (14 bit per ca. 16000 reti IP, 16 bit host id):  Reti di circa 64000 host, da  128.0.0.0 a 191.255.255.255
- Classe C (21 bit per reti IP e 8 bit per host id): Reti di circa 256 host, da 192.0.0.0 a 223.255.255.255
- Classe D, riservata a multicasting: da 224.0.0.0 a 239.255.255.255
- Classe E, riservata per usi futuri/ricerca: da 240.0.0.0 a 255.255.255.255

Il vantaggio di questo adressing è il fatto che sia facile risalire all'indirizzo di rete ma poco flessibile nell'utilizzo dello scarso range di indirizzi disponibili

Per questo come soluzione si utilizza il Classless Adressing e gli [[Indirizzi IPv6]] di 128 bit anziché 32.

Il Classless Adressing, noto anche come CIDR (Classless Inter-Domain Routing), è un sistema di assegnazione degli indirizzi IP che invece di assegnare automaticamente un blocco di indirizzi IP basato sulla classe della rete, CIDR consente di assegnare una "maschera di rete" che indica quanti bit dell'indirizzo IP rappresentano la rete stessa. La notazione CIDR usa il formato "indirizzo IP/maschera di rete", dove la maschera di rete indica quanti bit sono dedicati alla parte di rete e quanti alla parte di host.

![[Pasted image 20231124143006.png]]

Un indirizzo diventa del tipo  `a.b.c.d/n`, dove gli `n`  bit più a sinistra costituiscono la parte di indirizzo di rete.
La maschera di sottorete è numero composto da 32 bit in cui i primi `n` bit a sinistra sono imposti a 1 e i rimanenti a 0 e serve per distinguere quale parte di un indirizzo IP identifica la rete e quale l'host.
Se tra due indirizzi, i primi `n` bit sono uguali, vuol dire che appartengono alla stessa rete.

`