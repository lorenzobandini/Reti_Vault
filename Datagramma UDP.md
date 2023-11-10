Un datagramma UDP, User Datagram Protocol, è un formato di pacchetto dati usato per le comunicazioni su una rete.

Il datagramma UDP ha una struttura semplice. È composto dall'header di 8 byte che contiene:
- Source port \[16 bit]: identifica il numero di porta sull'host del mittente del datagramma.
- Destination port \[16 bit]: identifica il numero di porta sull'host del destinatario del datagramma.
- Length \[16 bit]: contiene la lunghezza totale in bytes del datagramma UDP (header + dati).
- Checksum \[16 bit]: contiene il codice di controllo del datagramma (header + dati + pseudo-header, quest'ultimo comprendente gli indirizzi IP di sorgente e destinazione). 

e da un

![[Pasted image 20231110152343.png]]



![[Pasted image 20231110152525.png]]