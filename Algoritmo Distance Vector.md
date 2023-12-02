Algoritmo iterativo, distribuito cioè ciascun nodo riceve parte delle informazioni da uno o più nodi direttamente connessi, effettuando calcoli e comunicando i risultati ai vicini in modo asincrono cioè senza la necessita di richiedere che tutti i nodi operino al passo con gli altri.

Questo algoritmo si basa sull'equazione di [[Bellman-Ford]].

L'idea di base dell'algoritmo è che ogni nodo invia una copia del proprio vettore distanza a ciascuno dei suoi vicini.
Quando un nodo $x$ riceve un nuovo vettore distanza $DV$ da qualcuno dei suoi vicini $v$, lo salva e usa l'equazione di Bellman-Ford per aggiornare il proprio vettore di distanza.
Finché tutti i nodi continuano a scambiare $DV$ in maniera asincrona, ciascuna stima dei costi $D_{xy}$ converge all'effettivo costo del percorso a costo minimo $d_{x,y}$

Si tratta di un algoritmo iterativo e asincrono

![[Pasted image 20231202152030.png]]