Richiede il trasferimento di una risorsa identificata da una [[URL]] o operazioni associate all'[[URL]] stessa.


```HTTP
GET http://192.168.11.66 HTTP/1.1
host: 192.168.11.66
Connection: close

HTTP/1.1 200 OK
Date: Sun, 14 May 2000 19:57:13 GMT
Server: Apache/1.3.9 (Unix) (Red Hat/Linux)
Last-Modified: Tue, 21 Sep 1999 14:46:36 GMT
ETag: "f2fc-799-37e79a4c"
Accept-Ranges: bytes
Content-Length: 1945
Connection: close
Content-Type: text/html <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 3.2Final//EN">
<HTML> ... <\HTML>
```

Il **conditional GET** è un meccanismo che permette al [[Client]] HTTP di effettuare richieste a un [[Server]] WEB in modo più efficiente e ridurre il consumo di [[Bandwidth]] quando si tratta di recuperare risorse che potrebbero non essere state modificate dall'ultima volta che sono state richieste, rispondendo con "304 Not Modified" al posto della risorsa risparmiando il tempo di trasmissione del corpo.
Si basa principalmente su due [[Header HTTP]] HTTP:
- `If-Modified-Since`:  Il client invia data e ora in cui ha ricevuto la prima volta la risorsa e il server risponderà con la risorsa solo se è stata modificata dopo l'ultima volta che è stata ricevuta.
- `If-None-Match`: Il client invia un ETag che identifica unicamente la propria risorsa e se il server ha lo stesso identificatore non invierà la risorsa poichè non modificata.


```HTTP
GET http://192.168.11.66 HTTP/1.1
Host: 192.168.11.66
If-Modified-Since: Tue, 21 Sep 1999 14:46:36 GMT

HTTP/1.1 304 Not Modified
Date: Wed, 22 Sep 1999 15:06:36 GMT
Server: Apache/1.3.9 (Unix) (Red Hat/Linux)
```