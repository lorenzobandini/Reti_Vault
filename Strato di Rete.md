Responsabile della consegna dei [[Datagramma IP|datagrammi]] tra gli host. Offre servizi allo strato di trasporto e utilizza i servizi dello strato collegamento.

La comunicazione a livello di rete avviene con:
1. L'entità a livello di rete riceve i segmenti dal livello di trasporto nell'host mittente e incapsula i segmenti in datagrammi
2. I datagrammi sono inoltrati al prossimo nodo
3. Il router esamina i campi intestazione in tutti i datagrammi IP che lo attraversano e li inoltra da un collegamento in ingresso ad un collegamento in uscita
4. Sul lato destinatario, consegna i segmenti al livello di trasporto

![[Screenshot 2023-11-22 115646.png]]

Le differenze principali del livello di trasporto sono:
- Livello di trasporto nei sistemi terminali, mentre di reti nei nodi intermedi
- Il livello di rete interconnette reti eterogenee
- Il livello di rete implementa poche funzioni

Le funzioni fondamentali del livello di rete sono:
- Suddivisione in pacchetti
- [[Instradamento]] (routing)
- Inoltro ([[Forwarding]])

Per implementare queste funzioni bisogna implementare dei [[Meccanismi IP]]

Le caratteristiche dello strato di rete sono:
- Interconnessione di reti eterogenee: offre un'astrazione che consente a host e reti eterogenee di funzionare dal punto di vista logico come una singola rete
- Modello a clessidra: innovazione possibile nei livelli sottostanti e nei livelli superiori

![[Pasted image 20231122115824.png]]

Nel tempo poi il modello si è trasformato...

[[Internet Protocol]]

Inoltre anche a livello di rete si fa multiplexing e demultiplexing

![[Pasted image 20231122122540.png]]