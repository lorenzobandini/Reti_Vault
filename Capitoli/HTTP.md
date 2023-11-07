
Usato dal 1990 come [[Protocollo]] di trasferimento per il [[World Wide Web]], sta per HyperText Transfer Protocol ed è un generico protocollo senza stato che può essere usato per numerose tasks, oltre che all'ipertesto, come name server e gestione degli oggetti distribuiti.
Una caratteristica di HTTP è la digitazione e negoziazione della rappresentazione dei dati, consentendo sistemi da costruire indipendentemente dai dati in fase di trasferimento.

Protocollo di tipo **richiesta/risposta** che funziona seguendo l'architettura [[Client-Server]] dove:
- Client HTTP: programma che stabilisce una connessione con un server HTTP e invia una **richiesta** per effettuare operazioni su risorse web
	- Server HTTP: programma che accetta connessioni per servire richieste inviando messaggi di **risposta**

Inoltre è un protocollo stateless cioè senza memoria di stato dato dal fatto che le coppie richiesta/risposta sono indipendenti e ogni richiesta viene eseguita indipendentemente da quelle che l'hanno preceduta.
La [[Connessione]] richiesta dal client con il server segue il protocollo [[TCP]]([[Connection-Oriented]]) e i processi si scambiano [[Messaggi HTTP]] attraverso i rispettivi socket.

Per migliorare le prestazioni usiamo il [[Pipelining]] e la Web Cache o spesso chiamata [[Server Proxy]].
Le risorse possono essere disponibili in più rappresentazioni così usiamo il [[Content Negotiation]].

HTTP è server-less cioè non mantengono informazioni sui clienti, quindi si usano i [[Cookie]].




