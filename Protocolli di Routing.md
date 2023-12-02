Hanno l'obiettivo di determinare percorsi buoni dagli host mittenti agli host destinatari attraverso nodi intermedi ([[Router]])
Un percorso è una sequenza di router che i pacchetti attraversano dall'host sorgente alla destinazione finale ed è buono se è quello di costo minore, più veloce e meno congestionato.
Astraendo la rete di reti come un grafo dove i nodi sono i router e gli archi sono i collegamenti tra loro che hanno ognuno il loro costo possiamo applicare algoritmi come stessimo lavorando su grafi.

Gli algoritmi di routing vengono classificati in base a quanto cambiano velocemente i percorsi (statici - dinamici) e quanto sono globali o decentralizzate le informazioni.

Nel routing statico le righe (entry) della tabella vengono configurate manualmente dall’operatore. Tale metodo viene usato per reti di piccole dimensioni e la cui topologia non varia molto, dove è possibile prevedere tutti i possibili percorsi di un pacchetto IP nella rete.

Nel routing dinamico esistono protocolli specifici che provvedono automaticamente ad inserire nella tabella del router le entry relative ai possibili percorsi. Viene usato nelle reti di medie-grandi dimensioni e con topologia variabile (grandi reti locali private e Internet).

Gli algoritmi sono globali se si basano sulla conoscenza della topologia di tutta la rete. Il calcolo può essere fatto in un unico sito o in più nodi, utilizzando informazioni sulla connettività di tutti i nodi e sui costi di tutti i link.

Gli algoritmi sono decentralizzati quando nessun nodo conosce la topologia di tutta la rete, all’inizio ha informazioni solo sui nodi e link vicini. Il calcolo del percorso è iterativo e distribuito (ad esempio [[Algoritmo Distance Vector]]) dove ogni nodo elabora un vettore di stima dei costi verso tutti gli altri nodi nella rete e il cammino a costo minimo viene calcolato in modo distribuito e iterativo scambiandosi informazioni con i nodi vicini.

Un altro algoritmo in contrapposizione, che si basa su [[Algoritmo di Dijkstra]], è l'[[Algoritmo Link-State]]

Facciamo un confronto tra LS e DV
Complessità dei messaggi:
- LS: con $n$ nodi, $E$ collegamenti, implica l'invio di $O(nE)$ messaggi
- DV: richiede scambi tra nodi adiacenti

Velocità di convergenza:
- LS: l'algoritmo $O(n^2)$ richiede $O(nE)$ messaggi
- DV: può convergere lentamente. Può presentare cicli d'instradamento. Può presentare il problema del conteggio infinito.

Robustezza in caso di malfunzionamenti:
- LS: un router può comunicare via broadcast un costo sbagliato per uno dei suoi collegamenti connessi ma non per gli altri. I nodi si occupano di calcolare soltanto le proprie tabelle.
- DV: un nodo può comunicare cammini a costo minimo errati a tutte le destinazioni. La tabella di ciascun nodo può essere usata dagli altri e un calcolo errato si può diffondere in tutta la rete.

La visione di una rete costituita da un insieme di router omogenei interconnessi è semplicistica. Nella realtà i router sono organizzati in [[Sistemi Autonomi]]