Il programma Traceroute in UNIX o tracert in Windows può essere utilizzato per individuare il percorso di un datagramma dalla sorgente alla destinazione tramite l’identificazione dell’indirizzo IP di tutti i router che vengono visitati lungo il percorso.
Solitamente il programma viene impostato per un massimo di 30 salti (router), che sono usualmente sufficienti per raggiungere la destinazione.

Traceroute è implementato con l'uso del protocollo UDP, si invia un datagramma ad un porta su cui è improbabile che un processo sia in ascolto e datagrammi sono configurati in modo da scatenare l’invio di messaggi di errore per tempo scaduto e per porta destinazione non raggiungibile.

![[Pasted image 20231129120733.png]]

Invio di $n +1$ datagrammi UDP (n numero di router nel percorso) con valori di TTL crescenti.
Quando TTL=0 il router invia un messaggio di errore di tempo scaduto.
Il messaggio di errore inviato dall’host destinazione è port unreachable.

Il programma traceroute imposta inoltre un timer per trovare il RTT di ciascun router e della destinazione.
La maggior parte dei programmi traceroute invia tre messaggi a ogni dispositivo, con lo stesso valore di TTL, per poter effettuare una stima migliore del tempo di round-trip.

L'implementazione del comando tracert su windows usa i messaggi [[ICMP]] echo request/reply.

![[Pasted image 20231129120942.png]]

