[[Application Program Interface (API)]] che funge da [[Interfaccia]] tra gli strati di applicazione e di trasporto.
Socket è la API di [[internet]] per eccellenza.
Due processi comunicano mandando dati alla socket, e leggendoli da questa mentre il resto della connessione è responsabilità dei restanti 5 livelli dello[[Stack Protocollare TCP-IP]].
Un Socket è una struttura dati astratta utilizzata dal programma applicativo.
La comunicazione tra un processo [[Client]] e [[Server]] è realizzata attraverso la comunicazione tra due socket.
Il client considera la socket come l'entità che riceve le richieste e fornisce le risposte, per il server la socket è l'entità da cui riceve le richieste e a cui inviare le risposte.

![[Pasted image 20230930173317.png]]