1. Un'applicazione su un host sorgente genera dati da trasmettere.
2. I dati vengono inviati al protocollo di trasporto, in questo caso TCP.
3. TCP segmenta i dati in pacchetti più piccoli, chiamati segmenti TCP.
4. TCP aggiunge un'intestazione a ciascun segmento TCP.
5. I segmenti TCP vengono inviati al protocollo di rete, in questo caso IP.
6. IP incapsula i segmenti TCP in pacchetti IP.
7. I pacchetti IP vengono inviati attraverso la rete.
8. I pacchetti IP vengono consegnati a un router.
9. Il router scompone i pacchetti IP nei rispettivi segmenti TCP.
10. I segmenti TCP vengono inviati all'host destinazione.
11. TCP sull'host destinazione riceve i segmenti TCP.
12. TCP ricompone i segmenti TCP nei dati originali.
13. I dati vengono inviati al protocollo di applicazione sull'host destinazione.
14. Il protocollo di applicazione sull'host destinazione consegna i dati all'applicazione.
15. L'applicazione utilizza i dati come richiesto.