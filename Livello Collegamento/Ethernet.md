[[LAN]] cablata con più posizione sul mercato. Prima LAN ad alta velocità con vasta diffusione semplice e meno costosa di token ring, FDDI e ATM e sempre al passo dei tempi con il tasso trasmissivo.

Fino a metà degli anni 90, per distribuire il cavo prima veniva usata una topologia a bus mentre ora tutte le reti odierne LAN Ethernet sono progettate con topologia a stella dove al centro è collocato uno [[Switch]]. 

L'adattatore trasmittente incapsula i datagrammi IP in un pacchetto Ethernet che ha forma:
![[Pasted image 20231205165745.png]]

In cui:
- _Preambolo_: campo di 8 byte che serve per attivare gli adattatori dei riceventi e sincronizzare i loro orologi con quello del trasmittente. Sette hanno i bit a `10101010` mentre l'ultimo `10101011`.
- _Indirizzo di destinazione_: 6 byte che serve ad un adattatore a confrontarlo con il proprio [[Indirizzo MAC]] per poi trasferire il contenuto a livello di rete, se non combacia viene ignorato.
- _Indirizzo sorgente_: 6 byte che indicano l'indirizzo dell'adattatore che trasmette il frame.
- _Campo tipo_: 2 byte che consentono a ethernet di supportare vari protocolli di rete.
- _Dati_: L'unità massima di trasferimento MTU che varia tra 46 byte ad un massimo di 1500 byte. Se il datagramma è più grande allora deve essere frammentato. Se il campo dati è più piccolo il campo dati deve essere riempito.
- _Controllo CRC_: consente all'adattatore ricevente di rilevare la presenza di un errore nei bit del pacchetto

Ethernet rimane è un protocollo [[Connection-Less]] poiché non stabilisce nessuna connessione con nodo destinazione e anche non affidabile dato che non invia _ACK_ o _NACK_ al nodo mittente e i dati nei frame eliminati sono recuperati solo se il trasferimento dati affidabile è implementato ai livelli superiori.