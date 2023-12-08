Sta per **TE**rminal **NET**work ed è un [[Protocollo]] di terminale remoto il cui scopo è quello di permettere l'uso interattivo di macchine remote per:
- Lavoro remoto
- Accesso multiplo ad un computer

Invece di offrire [[Server]] specializzati per servizi interattivi, l'approccio consiste nel permettere all'utente di effettuare una sessione di login nella macchina remota e quindi inviare i comandi
Tramite il login remoto gli utenti hanno accesso ai comandi e programmi disponibili nella macchina remota ma non è un compito semplice, perciò Telnet maschera sia la rete che i sistemi operativi utilizzando un'[[interfaccia]] minima, spesso di soli caratteri, ma veloce.

Il funzionamento è:
1. Telnet permette ad un utente su una macchina di stabilire una connessione con un login server remoto
2. In seguito, passa le battute dei testi della macchina locale alla macchina remota che vengono eseguiti come se fossero stati battuti al terminale della macchina remota
3. L'output della macchina remota viene trasportato a terminale dell'utente

Tutto ciò facendolo sembrare un servizio trasparente come se l'utente fosse direttamente connesso alla macchina remota.

Il modello di Telnet include:
- Un programma [[Server]] che accetta le richieste
- Un programma [[Client]] che effettua le richieste interagendo con il terminale utente sull'[[host]] locale e scambiando messaggi con il Telnet server

Il [[protocollo]] Telnet consiste in:
- Il client stabilisce con il server una connessione [[TCP]]
- Il client accetta le battute di tasti del terminale e le invia al server. Accetta i caratteri che il server manda indietro e li visualizza sul terminale utente
- Il server accetta la connessione TCP e trasmette i dati al sistema operativo locale

Il client si connette alla porta 23 del server. La connessione TCP persiste per la durata della sessione di login.
Il sistema operativo assume che gli input ad un processo vengano forniti dalla tastiera (standard input) e che gli output siano inviati al monitor (standard output).

A differenza del [[Local Login]] che faremmo sulla nostra macchina, ma abbiamo bisogno di un [[Remote Login]].

Il problema di Telnet è quello di dover poter operare con il massimo di sistemi operativi e quindi gestire dettagli di sistemi operativi eterogenei ma ogni terminale può differire dagli altri per set e codifica di caratteri, larghezza della linea e lunghezza della pagina e i vari tasti escape perciò è stato definito un terminale virtuale, il [[Network Virtual Terminal (NVT)]], per ogni dispositivo che è intercambiabile con il terminale locale.

Il problema di Telnet è quello di far passare ogni dato in chiaro, anche le password e per questo viene sostituito nella maggior parte delle sue applicazioni dalla [[Secure Shell (SSH)]].