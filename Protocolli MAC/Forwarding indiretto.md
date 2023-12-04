Nel forwarding indiretto, il dispositivo mittente deve fare affidamento su un router per inoltrare il pacchetto al destinatario. Questo accade quando il mittente e il destinatario non sono direttamente collegati alla stessa rete locale, e il pacchetto deve attraversare una o più reti intermedie. In questo caso, il dispositivo mittente consulta una tabella di routing per determinare il percorso ottimale attraverso la rete. Il router, a sua volta, si occupa di inoltrare il pacchetto lungo il percorso corretto in direzione del destinatario.

Questo processo avviene in più fasi, considerando l'invio di un datagramma con mittente IP di A e destinatario IP di B:
1. A crea un datagramma IP con IP sorgente A e destinazione B. A crea un frame con indirizzo MAC destinazione l'indirizzo MAC del router che incapsula il datagramma IP
2. Il frame viene inviato da A al router nel quale viene decapsulato e il datagramma passa al livello IP
3. Il router estrae il datagramma IP dal frame Ethernet e vede la sua destinazione B per cui inoltra il pacchetto verso B utilizzando ARP per ottenere l'indirizzo MAC e incapsulando in un frame
4.  B riceve il frame ed estrae il datagramma