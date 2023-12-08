I [[server]] di posta adottano una tecnica, denominata *spooling*:
- l'utente invia un messaggio, il sistema ne pone una copia in memoria (*spool* - o area di accodamento della posta), insieme con id mittente, id destinatario, id macchina di destinazione e tempo di deposito.
- il sistema avvia il trasferimento alla macchina remota. Il sistema ([[client]]) stabilisce una connessione [[TCP]] con la macchina destinazione
- Se la [[connessione]] viene aperta, inizia il trasferimento del messaggio
- Se il trasferimento va a buon fine, il client cancella la copia locale della mail
- Se il trasferimento non va a buon fine, il processo di trasferimento scandisce periodicamente l'area di spooling, e tenta il trasferimento dei messaggi non consegnati. Oltre un certo intervallo di tempo, se il messaggio non è stato consegnato, viene inviata una notifica all'utente mittente

I server di postano offrono anche un servizio di gestione degli [[Alias]].
