Simile al GET, ma il server non trasferisce il message body nella risposta.
Utile per controllare lo stato dei documenti (validità, modifiche, cache refresh).


```HTTP
HEAD http://192.168.11.66 HTTP/1.1
host: 192.168.11.66
Connection: close

HTTP/1.1 200 OK Date: Sun, 14 May 2000 20:02:41 GMT 
Server: Apache/1.3.9 (Unix) (Red Hat/Linux)
Last-Modified: Tue, 21 Sep 1999 14:46:36 GMT
ETag: "f2fc-799-37e79a4c"
Accept-Ranges: bytes 
Content-Length: 1945 Connection: close Content-Type: text/html
```

Da notare la mancanza del message body