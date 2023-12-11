Con HTTP/2 avevamo una maggiore flessibilità lato [[server]] nell'invio di oggetti al [[client]] mantenendo invariati metodi, codici di stato e campi di intestazione invariati rispetto a HTTP/1.1.
L'ordine di trasmissione degli oggetti richiesti era in base alla priorità dell'oggetto specificata dal client. Si potevano inviare anche oggetti non richiesti dal client (Push) e dividere gli oggetti in frame per mitigare la HOL.

Inoltre viene aggiunto un metodo di Multiplexing in cui è possibile inviare più richieste HTTP mentre le risposte possono essere ricevute in modo asincrono tramite una singola connessione TCP. Per comunicare si usa uno [[stream]], un flusso bidirezionale di frame all'interno di un'unica connessione TCP che rappresenta una comunicazione richiesta-risposta. I frame sono l'unità di comunicazione in HTTP/2 e una sequenza di essi costituisce un messaggio HTTP.
Mediante l'astrazione degli stream è possibile effettuare il multiplexing delle richieste gestendo così più stream sulla stessa connessione TCP.
Diventa possibile anche associare ad ogni stream un peso che ne indica la priorità e una dipendenza verso altri stream.

Gli header vengono poi compressi e il meccanismo Server Push permette al server di inviare risorse aggiuntive per una singola richiesta da parte del client. Grazie a tutte queste strategie riesce a mitigare parzialmente l'HOL ma non totalmente perché TCP non vede gli stream e quindi all'arrivo di 3 _ACK_ o il timeout mette in stallo la connessione e quindi tutti gli stream.
