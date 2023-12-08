Un pacchetto [[ARP]] è inviato sulla rete per eseguire la risoluzione degli indirizzi. Il pacchetto ARP contiene informazioni come l'[[indirizzo IP]] del mittente, l'[[indirizzo MAC]] del mittente, l'indirizzo IP del destinatario e l'indirizzo MAC del destinatario.

![[Pasted image 20231204164327.png]]

In particolare:
- _Hardware Type_: [[protocollo]] a livello di collegamento
- _Protocol Type_: protocollo di livello superiore
- _Source hardware address e source protocol address_: indirizzi del nodo mittente a livello link e superiore. Lunghezza variabile. Campi Hard. Length e prot. Length
- _Destination hard Address_ (vuoto nelle richieste)
- _Destination protocol address_