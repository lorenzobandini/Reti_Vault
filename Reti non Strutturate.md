Reti in cui i nodi sono organizzati come un grafo in modo randomico seguendo principi molto semplici.
Non ci sono vincoli sul posizionamento delle risorse rispetto alla topologia del grafo e l'aggiunta o la rimozione di nodi è un'operazione semplice e poco costosa..
L'obiettivo è gestire i nodi con comportamento fortemente transiente cioè con tassi di join e leave elevati.
Non avendo alcun server centralizzato è completamente distribuita e ogni peer invia una query a tutti i suoi vicini e se un peer riceve una query e ha il file richiesto invia messaggio _QueryHit_ sul reverse path o altrimenti inoltra la query a tutti i suoi vicini.

![[Schermata 2024-01-06 alle 12.30.19.png]]

I problemi sono il flooding (tipo di ricerca in cui c'è un inoltro a tutti i nodi), la poca scalabilità e il bootstrap molto lento in cui vengono caricati tutti i nodi in un elenco.
