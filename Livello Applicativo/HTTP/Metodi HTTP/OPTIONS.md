Richiede solo le opzioni di comunicazione associate ad un [[URL]] o al [[server]] stesso (le sue capacità, metodi esposti, ecc.).

```http
OPTIONS http://192.168.11.66/manual/index.html HTTP/1.1
host: 192.168.11.66 
Connection: close

HTTP/1.1 200 OK 
Date: Sun, 14 May 2000 19:52:12 GMT
Server: Apache/1.3.9 (Unix) (Red Hat/Linux)
Content-Length: 0
Allow: GET, HEAD, OPTIONS, TRACE
Connection: close
```

Nella richiesta abbiamo:
- La prima riga indica il tipo di richiesta, che è "OPTIONS", seguita dall'URL di destinazione e la versione del protocollo HTTP utilizzata.
- La seconda riga specifica l'host di destinazione.
- La terza riga indica che la connessione verrà chiusa dopo la risposta ("Connection: close").

Nella risposta del server abbiamo:
- La prima riga della risposta indica che la richiesta è stata elaborata con successo.
- La seconda riga contiene la data in cui è stata generata la risposta.
- La terza riga specifica il tipo di server web utilizzato.
- La quarta riga indica che il corpo della risposta è vuoto ("Content-Length: 0").
- La quinta riga elenca i metodi HTTP consentiti su questa risorsa.
- Infine, l'ultima riga indica che la connessione verrà chiusa dopo la risposta.