Serve per inviare dal client al server informazioni inserite nel body del messaggio.
Usato per chiedere che il server accetti la risorsa nel corpo della richiesta come una nuova subordinata della risorsa identificata dalla Request-[[URI]] nella Request-Line.
In pratica la funzione effettiva eseguita dal POST è determinata dal [[Server]] e dipendente tipicamente dalla Request-URI.
Alcuni esempi sono le annotazioni ad [[URL]] esistenti, FORMs, mail list e scritture su database.
Con le [[API REST]] vengono rispettate le specifiche [[HTTP]].


Possiamo vedere ad esempio:
![[Schermata 2023-10-08 alle 18.13.24.png]]

Viene fatta una richiesta `POST www.unipi.it/courses HTTP/1.1` al server con l'indirizzo del nodo padre dal quale il server si occuperà di creare una risorsa come suo nodo figlio (subordinata)