Responsabile della consegna dei [[Datagramma IP|datagrammi]] tra gli [[host]]. Offre servizi allo [[Livello di Trasporto]] e utilizza i servizi del [[livello collegamento]].

La comunicazione a livello di rete avviene con:
1. L'entità a livello di rete riceve i segmenti dal [[livello di trasporto]] nell'host mittente e incapsula i segmenti in datagrammi
2. I datagrammi sono inoltrati al prossimo nodo
3. Il [[router]] esamina i campi intestazione in tutti i datagrammi IP che lo attraversano e li inoltra da un collegamento in ingresso ad un collegamento in uscita
4. Sul lato destinatario, consegna i segmenti al livello di trasporto

![[Screenshot 2023-11-22 115646.png]]

Le differenze principali con il livello di trasporto sono:
- Livello di trasporto nei sistemi terminali, mentre di reti nei nodi intermedi
- Il livello di rete interconnette reti eterogenee
- Il livello di rete implementa poche funzioni

Le funzioni fondamentali del livello di rete sono:
- Suddivisione in pacchetti
- [[Routing]] (Instradamento)
- [[Forwarding]] (Inoltro)

Per implementare queste funzioni bisogna implementare dei [[Meccanismi IP]].

Le caratteristiche dello strato di rete sono:
- Interconnessione di reti eterogenee: offre un'astrazione che consente a host e reti eterogenee di funzionare dal punto di vista logico come una singola rete. La traduzione tra [[indirizzo IP|indirizzi IP]] di una rete privata a quella pubblica è effettuata attraverso [[NAT]].
- Modello a clessidra: innovazione possibile nei livelli sottostanti e nei livelli superiori

![[Pasted image 20231122115824.png]]

Questo modello continua a evolversi con le nuove tecnologie e le esigenze crescenti delle reti di comunicazione.

Il [[protocollo]] usato è l'[[Internet Protocol]] che non ha sistemi di gestione degli errori che vengono quindi implementati da [[ICMP]].

Inoltre anche a livello di rete si usa il multiplexing per combinare flussi di dati provenienti da diverse sorgenti in un unico canale, utilizzando l'indirizzamento IP e le porte di trasporto e il demultiplexing per separare e indirizzare correttamente i pacchetti in base a tali informazioni, consentendo la comunicazione [[efficiente]] tra dispositivi su una rete.

![[Pasted image 20231122122540.png]]

Un insieme di reti e router sotto il controllo di una singola entità amministrativa che segue una politica di routing coerente si chiama [[Sistemi Autonomi|sistema autonomo]].