
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

Con le varie versioni di HTTP ci sono sempre stati dei tentativi per migliorare il tempo di caricamento di una pagina agendo a livello di protocollo.

Con HTTP/1.1 venivano fatte più [[GET]] in pipeline su una singola connessione [[TCP]] così che il server rispondesse in ordine (FCFS: first-come-first-served scheduling) ma il problema è che un oggetto più piccolo dovesse attendere la trasmissione dietro a oggetti di grandi dimensioni (HOL: head of line blocking) ed il ripristino delle perdite per i [[Segmento TCP|Segmenti TCP]] persi introduceva un altro ritardo.
Un altra soluzione con HTTP1.1 i browser iniziarono ad instaurare più connessioni TCP in parallelo con un massimo di 6 connessioni contemporanee causando però un comportamento non più equo e poco efficace per il controllo della gestione.

Con HTTP/2 avevamo una maggiore flessibilità lato [[server]] nell'invio di oggetti al [[client]] mantenendo invariati metodi, codici di stato e campi di intestazione invariati rispetto a HTTP/1.1.
L'ordine di trasmissione degli oggetti richiesti era in base alla priorità dell'oggetto specificata dal client. Si potevano inviare anche oggetti non richiesti dal client (Push) e dividere gli oggetti in frame per mitigare la HOL.
Inoltre viene aggiunto un metodo di Multiplexing in cui è possibile inviare più richieste HTTP mentre le risposte possono essere ricevute in modo asincrono tramite una singola connessione TCP. Per comunicare si usa uno [[stream]], un flusso bidirezionale di frame all'interno di un'unica connessione TCP che rappresenta una comunicazione richiesta-risposta. I frame sono l'unità di comunicazione in HTTP/2 e una sequenza di essi costituisce un messaggio HTTP.
Mediante l'astrazione degli stream è possibile effettuare il multiplexing delle richieste gestendo così più stream sulla stessa connessione TCP.
Diventa possibile anche associare ad ogni stream un peso che ne indica la priorità e una dipendenza verso altri stream.
Gli header vengono poi compressi e il meccanismo Server Push permette al server di inviare risorse aggiuntive per una singola richiesta da parte del client. Grazie a tutte queste strategie riesce a mitigare parzialmente l'HOL ma non totalmente perché TCP non vede gli stream e quindi all'arrivo di 3 _ACK_ o il timeout mette in stallo la connessione e quindi tutti gli stream.

HTTP/3 è l'evoluzione di HTTP/2 che usa i servizi di [[QUIC]] ma mantiene la semantica di HTTP/2. In più aggiunge sicurezza, controllo degli errori e controllo della congestione sopra [[UDP]].

![[Pasted image 20231117184120.png]]