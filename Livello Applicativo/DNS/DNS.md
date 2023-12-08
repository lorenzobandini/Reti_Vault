Acronimo di Domain Name System, ha come obiettivo di identificare ogni [[Processo]].
Ogni processo di livello applicativo ha la necessità di individuare il processo omologo con il quale vuole comunicare. Il processo omologo risiede su una particolare macchina remota, anch'essa da individuare ma di cui sappiamo che utilizza lo stesso protocollo.
Vengono utilizzati [[Nome di Dominio|Nomi]] e [[Indirizzo IP|Indirizzi]].

Inizialmente l'associazione tra nomi logici e indirizzi IP era statica cioè tutti i nomi logici e relativi indirizzi IP erano contenuti in un file (host file) e periodicamente tutti gli host prelevano una versione aggiornata del file (master host file) da un server ufficiale.
Però date le dimensioni attuali di [[Internet]], questo approccio è impraticabile poiché non è possibile che ogni host abbia una copia (aggiornata) di un elenco del genere come poteva essere all'inizio delle reti e non è possibile neppure centralizzare un elenco del genere.
Si utilizza pertanto il DNS.

Il DNS è posizionato nel livello applicativo, gira su sistemi terminali e adotta il paradigma [[Client-Server]].
Si affida al sottostante protocollo di trasporto punto-punto per trasferire messaggi tra sistemi terminali ma non interagisce direttamente con gli utenti.

![[Pasted image 20231018170727.png]]

Il DNS è un meccanismo che deve:
- Specificare la sintassi dei nomi e le regole per gestirli
- Consentire la conversione da nomi a indirizzi e viceversa

Esso è costituito essenzialmente da:
- Uno **schema di assegnazione** dei nomi gerarchico e basato su domini
- Un **database distribuito** contenente i nomi e le corrispondenze con gli [[Indirizzo IP|Indirizzi IP]] implementando una gerarchia di name server
- Un [[Protocollo]] per la distribuzione delle informazioni sui nomi tra name server. Host e name server comunicano per risolvere nomi utilizzando [[UDP]] sulla porta 53 (oppure [[TCP]])

Il DNS offre anche dei [[Servizi DNS]].

La conversione da nome di [[Dominio]] a [[Indirizzo IP]] viene gestita da dei [[Name Servers]].


Il DNS è un database distribuito di [[Record DNS]].
Il comando `dig` (domain information groper) è uno strumento per interrogare il DNS name servers 
```dns
[dig @server name type]

dig unipi.it MX @8.8.8.8
``` 
Dove:
- server: è il nome o l'indirizzo IP del name server a cui fare la query
- name: è il nome del record che stiamo cercando
- type: indica il tipo di query richiesta, se non esplicitata è A

Ogni organizzazione dotata di host internet pubblicamente accessibili deve fornire i [[Record DNS]] al pubblico dominio che mappano i nomi di tali host in indirizzi IP.
Tali record possono essere mantenuti in un proprio DNS o tramite un gestore di servizi.

Il DNS è altamente decentralizzato. Nessun singolo server DNS contiene tutti gli indirizzi IP e i rispettivi domini. Una query viaggia lungo la catena di server DNS prima di ottenere un risultato. Il DNS Hijacking è la pratica di restituire risposte non corrette alle query DNS reindirizzando il client verso altri siti malevoli.

