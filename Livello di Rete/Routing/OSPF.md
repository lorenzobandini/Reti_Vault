OSPF, acronimo di Open Shortest Path First, è un [[protocollo]] di [[routing]] a stato di collegamento utilizzato per determinare i percorsi di routing all'interno di [[Sistemi Autonomi]] (Intra-AS). Utilizza [[Algoritmo Link-State]] e la sua metrica è decisa dall'amministratore e può essere [[latenza]], affidabilità, banda, numero di hop o altro.

![[Pasted image 20231202173838.png]]

AS può essere partizionato in aree per ridurre flooding di Link State Packet, una delle quali fa da dorsale (backbone).
Si hanno due livelli di gerarchia: la local area e la backbone così che gli annunci sullo stato dei collegamenti si sono inondati solo nell'area o nella dorsale e ogni nodo ha una topologia di area dettagliata; conosce solo la direzione da raggiungere altre destinazioni.

![[Pasted image 20231202174117.png]]

