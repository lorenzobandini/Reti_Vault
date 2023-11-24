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

Per questo come soluzione si utilizza il [[Classless Adressing]] e gli [[Indirizzi IPv6]] di 128 bit anziché 32.

`