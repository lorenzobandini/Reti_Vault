Identifica dove tale oggetto è situato. I dispositivi connessi in rete vengono individuati mediante i loro indirizzi IP, una sequenza di 4 byte (32 bit) usati per instradare i datagrammi a [[livello di rete]].
Il formato indirizzo IP è progettato per garantire l'efficienza nell'istradamento.

Ogni [[host]] è connesso ad [[internet]] attraverso un'[[interfaccia]] di rete, che è il confine fra l'host ed il collegamento su cui vengono inviati i datagrammi.

Gli indirizzi si dividono in:
- [[Indirizzi IPv4]]
- [[Indirizzi IPv6]]

Gli indirizzi IP sono gestiti da ICANN e assegnati agli ISP in blocchi.
Gli [[ISP]] assegnano ai clienti sottoblocchi di indirizzi in base a:
- Il numero di indirizzi $N$ in ogni subnetwork deve essere una potenza di 2
- La lunghezza del prefisso di ogni sottorete ($n$) va calcolata con la formula $n=32 - log_2(N)$ dove $N$ è il numero di indirizzi della sottorete
- Si assegnano blocchi di indirizzi contigui
- Se i blocchi sono di dimensioni diverse si parte dai blocchi più grandi

Il CIDR (Classless Inter-Domain Routing) permette anche di aggregare i blocchi di indirizzi per rendere più [[efficiente]] l'instradamento.

Alcuni indirizzi speciali sono:
- This-host 0.0.0.0 - Usato quando un host ha necessità di inviare un datagramma ma non conosce il proprio indirizzo IP (indirizzo sorgente)
- Limited-broadcast 255.255.255.255 - Usato quando un router o un host devono inviare un datagramma a tutti i dispositivi che si trovano all’interno della rete. I router bloccano la propagazione alla sola rete locale.
- Loopback 127.0.0.1 - il datagramma con questo indirizzo di destinazione non lascia l’host locale (localhost). Per test e debug.
- Indirizzi privati – Quattro blocchi riservati per indirizzi privati (riservati per reti locali): 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16, 169.254.0.0/16
- Indirizzi multicast - Blocco 224.0.0.0/4

Un indirizzo IP può essere attribuito all'interfaccia di un host secondo due distinte modalità:
- Configurazione Manuale: l'amministratore  configura direttamente nell'host l'indirizzo IP ed inserisce ulteriori informazioni di servizio (indirizzo gateway/router, netmask e indirizzo IP di almeno un server DNS)
- [[DHCP]]: l'host ottiene il proprio indirizzo e le altre informazioni in modo autentico
