Algoritmo iterativo e distribuito, cioè ciascun nodo riceve parte delle informazioni da uno o più nodi direttamente connessi, effettuando calcoli e comunicando i risultati ai vicini in modo asincrono cioè senza la necessità di richiedere che tutti i nodi operino al passo con gli altri.

Questo algoritmo si basa sull'equazione di [[Bellman-Ford]].

L'idea di base dell'algoritmo è che ogni nodo invia una copia del proprio vettore distanza a ciascuno dei suoi vicini.
Quando un nodo $x$ riceve un nuovo vettore distanza $DV$ da qualcuno dei suoi vicini $v$, lo salva e usa l'equazione di Bellman-Ford per aggiornare il proprio vettore di distanza.
Finché tutti i nodi continuano a scambiare $DV$ in maniera asincrona, ciascuna stima dei costi $D_{xy}$ converge all'effettivo costo del percorso a costo minimo $d_{x,y}$

Si tratta di un algoritmo iterativo e asincrono poiché ogni iterazione locale è causata da cambio del costo di uno dei collegamenti locali o la ricezione da qualche vicino di un vettore distanza aggiornato.
Inoltre è distribuito poiché ogni nodo aggiorna i suoi vicino solo quando il proprio $DV$ cambia e i vicini avvisano i rispettivi vicini solo se necessario.

![[Pasted image 20231202152030.png]]

Il problema è che le variazioni necessitano di tempo per stabilizzarsi e per brevi periodi di tempo potremmo avere percorsi non efficienti.
Un problema comune è il _count-to-infinity problem_ poiché quando viene aggiornato il livello di un arco si avranno un gran numero di iterazioni prima che il vero costo del path si propaghi mantenendo per del tempo un costo errato del path. Ciò è risolvibile con una tecnica chiamata _Poison Reverse_ nella quale, se un arco adiacente cambia valore, impostiamo il costo per raggiungere il nodo a cui ci collegava ad infinito così che il path verrà ricalcolato totalmente senza iterare più volte inutilmente.