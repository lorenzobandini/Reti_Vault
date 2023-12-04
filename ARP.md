Acronimo di Address Resolution Protocol, risolve il problema per cui una macchina all'accensione conosce il proprio indirizzo LAN, il proprio indirizzo IP e il suo indirizzo alfanumerico ma non sa chi ha attorno.

![[Pasted image 20231204161102.png]]

Ogni nodo IP nella LAN ha una tabella ARP. La tabella ARP contiene la corrispondenza tra indirizzi IP e indirizzi LAN in forma: \< Indirizzo IP; Indirizzo LAN; TTL \>
Il TTL è il tempo di vita ed è il valore che indica quando bisognirò eliminare una data voce nella tabella di vita.

Poiché ARP risolve gli indirizzi IP solo per i nodi della stessa LAN, le tabelle ARP contengono la corrispondenza fra indirizzi IP e indirizzi LAN per i nodi della stessa sottorete.

![[Pasted image 20231204164159.png]]

ARP utilizza una propria struttura dati che sono i [[Pacchetto ARP|Pacchetti ARP]].

Il funzionamento di ARP funziona con richieste e risposta.
La richiesta ARP è inviata in broadcast
![[Pasted image 20231204165434.png]]
La risposta ARP è inviata
