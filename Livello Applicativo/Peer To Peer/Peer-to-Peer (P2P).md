Modello di rete in cui i nodi sono tutti uguali e possono comunicare tra loro direttamente, senza la necessità di un [[server]] centrale.

In una rete P2P, ogni nodo può fungere da [[client]] e da server. I client possono accedere ai dati e ai servizi forniti dai server, e i server possono accedere ai dati e ai servizi forniti dai client.

I vantaggi delle reti P2P includono:
- **Scalabilità:** Le reti P2P possono essere scalate facilmente per supportare un numero elevato di utenti.
- **Efficienza:** Le reti P2P possono utilizzare la banda disponibile in modo [[efficiente]].
- **Risparmio sui costi:** Le reti P2P possono ridurre i costi per gli utenti e gli operatori di rete.

Gli svantaggi delle reti P2P includono:
- **Sicurezza:** Le reti P2P possono essere vulnerabili agli attacchi informatici.
- **Qualità del servizio:** La qualità del servizio può variare a seconda della congestione della rete.
- **Problemi di Copyright**: facilita la pirateria di file senza il controllo centralizzato delle autorità o dei detentori dei diritti.

Tutti i nodi (peer) hanno la stessa importanza e ogni nodo ha funzione sia di client che server (servent) e condivide le risorse. Ci possono essere dei server centralizzati o nodi con funzionalità diverse rispetto agli altri che si chiamano supernodi.

I sistemi sono altamente distribuiti e il numero dei nodi può essere dell'ordine delle centinaia di migliaia ma rimanendo dinamici e indipendenti entrando o uscendo dalla rete P2P in qualsiasi momento secondo operazioni di ingresso e uscita.

Un problema che si presenta dal fatto che le coppie di peer comunicano direttamente tra loro è che ogni peer non è necessariamente sempre attivo e può cambiare indirizzo IP ogni volta che si connette, quindi c'è bisogno di un metodo per trovare i peer e tenere traccia dei file disponibili nei vari peer.

Usando una **directory centralizzata** i problemi sono l'unico punto di fallimento, il collo di bottiglia per performance e la facilità con cui potrebbe essere oscurata.

Per cui vengono usate **reti decentralizzate** in un cui non c'è un servizio di directory centralizzato e i peer si organizzano in una overlay network. Ne esistono di due categorie:
- [[Reti non Strutturate]]
- [[Reti Strutturate]]

Per combinare al meglio i diversi approcci di directory centralizzata o reti decentralizzate si adotta una **copertura gerarchica** in cui non ci sono server con tutti i contenuti ma nemmeno abbiamo peer tutti uguali.
Ogni peer infatti o è un group leader se ha abbastanza banda o risorse oppure viene assegnato ad un group leader per poi instaurare le connessioni TCP tra peer e il suo group leader e tra varie coppie di group leader. Il group leader tiene traccia del contenuto dei suoi figli.
Ogni file è associato con un suo hash e un suo descrittore.
Il protocollo segue i passi:
1. Il client invia una query di keyword al suo group leader
2. il group leader risponde con dei match del tipo _\< hash del file, indirizzo IP \>_
3. Il client sceglie quindi i file da scaricare

Quando un group leader si disconnette, i peer di quel group leader devono essere assegnati ad un altro group leader.

![[Schermata 2024-01-06 alle 15.05.53.png]]