Il Routing Information Protocol (RIP) è un protocollo di routing che viene utilizzato per scambiare informazioni sulla rete tra i router all'interno di [[Sistemi Autonomi]] (Intra-AS). Il suo obiettivo principale è quello di determinare il percorso ottimale per inviare i pacchetti da una sorgente a una destinazione attraverso una rete IP. RIP utilizza un algoritmo di routing a vettori delle distanze, che calcola il percorso in base alla "distanza" metrica tra i router che è massimo 15 inclusa la rete dove si trova la destinazione.

![[Pasted image 20231202170929.png]]

Il protocollo si basa sull'algoritmo per cui un nodo invia la tabella di inoltro ai propri vicini in periodi di circa 30 secondi.
Un nodo $R$ riceve advertisement da vicino $V$ con $D_V[Y]$ e allora $D_R[Y]=1+D_V[Y]$ cioè viene aggiunto un hop $c(x,v)$ e considera come next-hop $V$.
Il nuovo percorso da $R$ a $Y$ viene inserito in tabella se:
- Se è un percorso non presente nella tabella e quindi viene aggiunto
- Se $D_V[Y]+1<D_{Rold}[Y]$ costo ricevuto inferiore a quello del vecchio percorso
- Se V è nextHop del vecchio e nuovo percorso, ma il costo è cambiato