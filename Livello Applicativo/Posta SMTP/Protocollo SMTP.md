Utilizza il protocollo [[TCP]] alla (porta 25) per consegnare in modo affidabile messaggi dal [[client]] al [[server]].
Ha 3 fasi:
- [[Handshake SMTP]]
- Trasferimento del messaggio
- Chiusura della connessione

Inoltre ci sono delle interazioni comando/risposta:
- Comandi: testo ASCII
- Risposta: codice di stato e descrizione

Alcuni comandi sono:
- **HELO** \<client identifier\>
- MAIL FROM:\<reverse-path\><\CRLF\>
- RCPT TO:\<forward-path\>\<CRLF\>
- DATA
- QUIT
- \<CRLF\>.\<CRLF\> (per determinare la fine di un messaggio)

La struttura di un messaggio mail è composta da:
- Linee intestazione (come To: , From: , Subject: , diversi dai comandi [[SMTP]])
- Linea vuota
- Body: che contiene l'effettivo messaggio con solamente caratteri ASCII a 7 bit.

Il problema di permettere di inviare solo messaggi di testo in ASCII si pone quando gli utenti tentano di inviare/ricevere messaggi con accenti o alfabeti non latini oppure contenenti audio o video. Per questo viene usato [[MIME]].