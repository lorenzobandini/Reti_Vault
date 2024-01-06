Sono sistemi con _Distributed Hash Table (DHT)_ dove ad ogni peer è assegnato un _ID_ ed ogni peer conosce un certo numero di peer.

Quando una risorsa viene pubblicata, essa viene instradata verso il peer con l'ID più "vicino" a quello della risorsa, utilizzando una metrica di distanza. Allo stesso modo, le richieste per risorse specifiche sono instradate verso il peer il cui _ID_ è più "vicino" a quello della risorsa cercata.
In questo modo, la _DHT_ facilita la gestione distribuita delle risorse in una rete strutturata, assicurando un posizionamento efficiente e una ricerca ottimale delle risorse in base agli _ID_ assegnati ai peer e alle risorse stesse.

Una rete del genere ha è strutturata e quindi ha vincoli sul grafo e sul posizionamento delle risorse sui nodi del grafo, l'organizzazione segue principi rigidi e l'aggiunta o la rimozione di nodi è un'operazione costosa.
Perciò un obiettivo di ottimizzazione può essere migliorare la locazione delle risorse come se ne occupa [[BitTorrent]]-