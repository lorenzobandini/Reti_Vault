Acronimo di Internet Control Message Protocol, viene usato da host e router per scambiarsi messaggi di errore o altre situazioni che richiedono intervento.
I messaggi ICMP sono incapsulati all'interno di [[Datagramma IP]] ma viene comunque considerato parte integrante dello strato di rete.

Quando un router o un host di destinazione devono informare il mittente di errori o di eventi avvenuti nell’inoltro di un pacchetto IP utilizzano questo protocollo.

I pacchetti ICMP vengono instradati dai router prima dei pacchetti IP ordinari. Alcune caratteristiche sono:
- Per pacchetti IP frammentati, i messaggi ICMP sono relativi al solo frammento con offset 0 (il primo frammento).
- I messaggi ICMP NON sono mai inviati in risposta a pacchetti IP con indirizzo mittente che non rappresenta in modo univoco un host (es. 0.0.0.0, 127.0.0.1) oppure con destinazione IP broadcast o multicast
- I messaggi ICMP non sono mai inviati in risposta a messaggi di errore ICMP, ma possono essere inviati in risposta a messaggi ICMP di interrogazione

I messaggi si distinguono in:
- Messaggi di segnalazione errore
- Messaggi di richiesta/risposta

Nell’header ICMP i campi Tipo (8 bit) e Codice (8 bit) indicano tipo e significato dei messaggi

![[Pasted image 20231129114550.png]]