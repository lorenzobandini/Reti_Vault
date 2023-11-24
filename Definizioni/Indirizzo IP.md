Identifica dove tale oggetto è situato. I dispositivi connessi in rete vengono individuati mediante i loro indirizzi IP, una sequenza di 4 byte (32 bit) usati per instradare i datagrammi a livello di rete.
Il formato indirizzo IP è progettato per garantire l'efficienza nell'istradamento.

Ogni host è connesso ad internet attraverso un'interfaccia di rete, che è il confine fra l'host ed il collegamento su cui vengono inviati i datagrammi.

Gli indirizzi si dividono in:
- [[Indirizzi IPv4]]
- [[Indirizzi IPv6]]

Gli indirizzi IP sono gestiti da ICANN e assegnati agli ISP in blocchi.
Gli [[Internet Service Provider (ISP)]] assegnano ai clienti sottoblocchi di indirizzi in base a:
- Il numero di indirizzi $N$ in ogni subnetwork deve essere una potenza di 2
- La lunghezza del prefisso di ogni sottorete ($n$) va calcolata con la formula $n=32 - log_2(N)$ dove $N$ è il numero di indirizzi della sottorete
- Si assegnano blocchi di indirizzi contigui
- Se i blocchi sono di dimensioni diverse si parte dai blocchi più grandi

Il CIDR (Classless Inter-Domain Routing) permette anche di aggregare i blocchi di indirizzi per rendere più efficiente l'instradamento.

Alcuni indirizzi speciali sono:
- This-host 0.0.0.0 - Usato quando un host ha necessità di inviare un datagramma ma non conosce il proprio indirizzo IP (indirizzo sorgente)
- Limited-broadcast 255.255.255.255 - Usato quando un router o un host devono inviare un datagramma a tutti i dispositivi che si trovano all’interno della rete. I router bloccano la propagazione alla sola rete locale.
- Loopback 127.0.0.1 - il datagramma con questo indirizzo di destinazione non lascia l’host locale (localhost). Per test e debug.
- Indirizzi privati – Quattro blocchi riservati per indirizzi privati (riservati per reti locali): 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16, 169.254.0.0/16
- Indirizzi multicast - Blocco 224.0.0.0/4

Un indirizzo IP può essere attribuito all'interfaccia di un host secondo due distinte modalità:
- Configurazione Manuale: l'amministratore  configura direttamente nell'host l'indirizzo IP ed inserisce ulteriori informazioni di servizio (indirizzo gateway/router, netmask e indirizzo IP di almeno un server DNS)
- [[DHCP]]: l'host ottiene il proprio indirizzo e le altre informazioni in modo autentico

Ora che abbiamo dato l'indirizzo IP al nostro host, ogni [[Datagramma IP]] è soggetto a "forwarding" da parte dell'host di origine e del router che sta attraversando causando:
- inoltro di un pacchetto verso l'uscita
- inoltro diretto o indiretto

Nell'inoltro diretto, il pacchetto IP ha come destinazione un host nella propria rete IP e l'invio è diretto sul destinatario, l'indirizzo di destinazione a livello link è quello del destinatario e non viene interpellata nessun'altra entità.

Nell'inoltro indiretto, il pacchetto IP ha come destinazione un host di un'altra rete IP, viene delegato l'invio al router e l'indirizzo di destinazione a livello link è quello del router.

Si osserva come, in entrambi i casi, condizioni necessarie perché tutto funzioni sono che:
- Esista un cammino (funzionante e) diretto, a livello data-link, tra tutti gli host che appartengono ad una stessa sottorete.
- Ogni host coinvolto abbia un indirizzo IP “giusto”, cioè con uguale net ID (cioè appartenga alla stessa sottorete) e con host ID univoco nella sottorete.

Le due condizioni insieme diventano condizione necessaria e sufficiente perché la comunicazione “funzioni”.

Ad ogni interfaccia verso la rete IP viene assegnato un indirizzo IP distinto.
Il router è un apparato che svolge funzioni di inoltro e instradamento a livello IP. Esso legge gli indirizzi IP, consulta la propria tabella di forwarding e decide dove mandare il pacchetto IP.


