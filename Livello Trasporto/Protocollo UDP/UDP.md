Acronimo per User Datagram Protocol, è un servizio [[internet]] di trasporto dati:
- Non orientato alle [[connessione]] ([[Connection-Less]])
- Trasporto NON affidabile
- NO controllo di [[Stream]]
- NO controllo congestione
- No garanzie timing né ampiezza minima di banda

Servizio di consegna a massimo sforzo, cioè che UDP farà del suo meglio per inviare i dati il più rapidamente possibile, nel quale però i datagrammi UDP possono essere perduti o consegnati fuori sequenza e l'affidabilità può essere aggiunta a livello applicazione.
[[Protocollo]] orientato al messaggio poiché ogni [[Datagramma UDP]] è indipendente dall'altro e i processi che lo utilizzano spesso devono inviare messaggi di dimensioni limitate che possono essere incapsulati in un datagramma UDP.

Rispetto al [[TCP]] l’UDP è meno complesso, offre meno servizi, ma è più indicato in contesti dove occorre un completo controllo della temporizzazione.

Le proprietà del servizio UDP sono:
- [[Connection-Less]] che non quindi non introduce ritardo e quindi rende il protocollo semplice non dovendo gestire lo stato di connessione. Ha un intestazione di soli 8 byte e non ha controllo di congestione e flusso potendo così di mandare dati a raffica.
- Il checksum è facoltativo
- Facile e leggero da gestire senza particolari meccanismi
- Utilizzato spesso in applicazioni multimediali dove c'è tolleranza alle piccole perdite.
- Altri impieghi sono i [[DNS]] o il SNMP (Simple Network Management Protocol)

Nel trasporto UDP:
- Il mittente UDP riceve un messaggio dal [[livello applicativo]], determina i valori dei campi dell'header UDP e crea lo user datagram che passa a IP
- Il destinatario UDP riceve lo user datagram da IP, controlla la checksum, estrae il messaggio di livello applicazione e smista il messaggio attraverso la socket

![[Pasted image 20231110152237.png]]

Gli attacchi hacker più famosi con UDP sono:
- [[Attacco UDP Flood]]: 
- [[Attacco UDP Amplification]]