Si tratta di un algoritmo globale in cui la topologia di rete e tutti i costi dei collegamenti sono noti a tutti i nodi attraverso il "link-state broadcast".
Tutti i nodi dispongono delle stesse informazioni e il calcolo del cammino a costo minimo da un nodo a tutti gli altri nodi della rete è fatto grazie all'[[Algoritmo di Dijkstra]] che è iterativo cioè che dopo la $k$-esima iterazione i cammini a costo minimo verso $k$ nodi di destinazione sono noti.
Inoltre viene creata una tabella d'inoltro per quel nodo.
