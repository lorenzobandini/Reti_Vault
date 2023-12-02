L'algoritmo di Dijkstra è un algoritmo utilizzato per trovare il percorso più breve da un nodo di partenza a tutti gli altri nodi in un grafo pesato, dove ogni arco ha associato un peso non negativo.

I passi sono:
1. **Inizializzazione:** Assegna a ogni nodo un valore di distanza iniziale. Il nodo di partenza avrà una distanza di zero, mentre tutti gli altri nodi avranno una distanza iniziale impostata a infinito e crea un insieme o una coda con priorità contenente tutti i nodi non ancora visitati, ordinati in base alle loro distanze attuali dal nodo di partenza.
2. **Scelta del nodo corrente:** Scegli il nodo con la distanza minima dal set di nodi non ancora visitati come nodo corrente.
3. **Aggiornamento delle distanze:** Per ogni nodo adiacente al nodo corrente, calcola la distanza totale dal nodo di partenza attraverso il nodo corrente. Se questa distanza è minore della distanza attuale del nodo adiacente, aggiorna la distanza del nodo adiacente.
4. **Marcatura del nodo corrente come visitato:** Segna il nodo corrente come visitato e rimuovilo dal set di nodi non ancora visitati.
5. **Ripeti:** Ripeti i passi 2-4 fino a quando tutti i nodi sono stati visitati o finché il nodo di destinazione non è stato visitato.

Alla fine dell'esecuzione, avrai le distanze minime da un nodo di partenza a tutti gli altri nodi nel grafo.