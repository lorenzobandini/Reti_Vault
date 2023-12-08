Acronimo di Dynamic Host Configuration Protocol, ha l'obiettivo assegnare un indirizzo IP ad un [[host]] che si aggiunge alla rete in modo dinamico.
Il DHCP è un protocollo Client-Server dove:
- L’host invia in broadcast un messaggio DHCP discover (opzionale)
- Il server DHCP risponde con un messaggio DHCP offer (opzionale)
- L’host richiede un indirizzo IP: messaggio DHCP request
- Il server DHCP invia un messaggio DHCP _ACK_ (se la richiesta va a buon fine)

Il DHCP può essere ospitato sul router, servendo tutte le sottoreti a cui è collegato il router e un DHCP client richiede un indirizzo in questa rete.

Lo scenario DHCP Client-Server è:

![[Screenshot 2023-11-24 151141 1.png]]

I passaggi DHCP discover e DHCP offer possono essere saltati se un client ricorda e desidera riutilizzare un indirizzo di rete precedentemente assegnato.

DHCP può restituire ulteriori informazioni come:
- Indirizzo del gateway/router
- Netmask
- Nome e indirizzo IP di almeno un server DNS

