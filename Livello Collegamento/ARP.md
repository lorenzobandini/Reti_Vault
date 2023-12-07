Acronimo di Address Resolution Protocol, risolve il problema per cui una macchina all'accensione conosce il proprio indirizzo MAC, il proprio indirizzo IP e il suo indirizzo alfanumerico ma non sa chi ha attorno.

![[Pasted image 20231204161102.png]]

Ogni nodo IP nella LAN ha una tabella ARP. La tabella ARP contiene la corrispondenza tra indirizzi IP e indirizzi MAC in forma: \< Indirizzo IP; Indirizzo MAC; TTL \>
Il TTL è il tempo di vita ed è il valore che indica quando bisognirò eliminare una data voce nella tabella di vita.

Poiché ARP risolve gli indirizzi IP solo per i nodi della stessa LAN, le tabelle ARP contengono la corrispondenza fra indirizzi IP e indirizzi MAC per i nodi della stessa sottorete.

![[Pasted image 20231204164159.png]]

ARP utilizza una propria struttura dati che sono i [[Pacchetto ARP|Pacchetti ARP]].

Il protocollo ARP interagiste direttamente con il livello collegamento. Il pacchetto ARP viene incapsulato in un frame e spedito in broadcast sulla rete. L'header del frame di livello 2 specifica che il frame contiene un pacchetto ARP. Ogni nodo nella rete locale riceve ed elabora il pacchetto di richiesta ARP e il nodo che riconosce il proprio indirizzo IP restituisce un pacchetto di risposta ARP che contiene il proprio indirizzo IP e indirizzo MAC. Il pacchetto di risposta viene inviato in modalità unicast al nodo originario.

La richiesta ARP è inviata in broadcast
![[Pasted image 20231204165434.png]]
La risposta ARP è inviata in unicast
![[Pasted image 20231204165829.png]]

Per l'inoltro pacchetti è possibile utilizzare:
- [[Forwarding diretto MAC]]
- [[Forwarding indiretto MAC]]
