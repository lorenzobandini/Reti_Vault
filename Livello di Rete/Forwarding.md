Trasferimento del pacchetto sull'appropriato collegamento di uscita.

![[Pasted image 20231122121937.png]]

Per questo viene utilizzata una tabella d'inoltro che viene costruita grazie alla funzione di instradamento.

Ogni [[Datagramma IP]] è soggetto a "forwarding" da parte dell'host di origine e del [[router]] che sta attraversando causando:
- inoltro di un pacchetto verso l'uscita
- [[Forwarding Diretto IP]] o [[Forwarding Indiretto IP]]

Si osserva come, sia nell'inoltro diretto che in quello indiretto, le condizioni necessarie perché tutto funzioni sono che:
- Esista un cammino (funzionante e) diretto, a livello data-link, tra tutti gli host che appartengono ad una stessa sottorete.
- Ogni host coinvolto abbia un indirizzo IP “giusto”, cioè con uguale net ID (cioè appartenga alla stessa sottorete) e con host ID univoco nella sottorete.

Le due condizioni insieme diventano condizione necessaria e sufficiente perché la comunicazione “funzioni”.

Ad ogni interfaccia verso la rete IP viene assegnato un indirizzo IP distinto.
Il router è un apparato che svolge funzioni di inoltro e instradamento a livello IP. Esso legge gli indirizzi IP, consulta la propria tabella di forwarding e decide dove mandare il pacchetto IP.

![[Pasted image 20231124174011.png]]

Altre tecniche adottate nell'inoltro sono:
- Aggregazione degli indirizzi: raggruppare più blocchi di indirizzi IP contigui in un unico blocco più grande per ridurre la complessità della tabella di instradamento e migliorare l'efficienza.
- Longer Mask Matching:  processo di selezione della regola di instradamento con la maschera di sottorete più lunga che corrisponde all'indirizzo IP di destinazione del pacchetto. Quando ci sono più regole di instradamento che corrispondono a un indirizzo IP, il router sceglierà la regola con la maschera di sottorete più specifica, poiché questa rappresenta la corrispondenza più lunga e precisa.
- Router Gerarchico:  modello di rete in cui i router sono organizzati in una struttura gerarchica.
