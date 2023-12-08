Inventato da un gruppo di ricercatori dell'Università di California, guidati da Vinton Cerf e Bob Kahn. Il lavoro su TCP/IP iniziò nel 1973 e fu pubblicato per la prima volta nel 1974 diventando la famiglia di protocolli che è ancora attualmente utilizzata in [[Internet]].
Si tratta di una gerarchia di protocolli, ciascuno dei quali fornisce funzionalità specifiche.
Il termine gerarchia significa che ciascun [[protocollo]] di livello superiore è supportato dai servizi forniti dai protocolli di livello inferiore.
Definita in origine in termini di quattro livelli software soprastanti a un livello hardware, la pila TCP/IP è oggi intesa come composta di cinque livelli:
- **Applicazione**: supporta le applicazioni di rete, collegamento logico end-to-end: scambio di messaggi tra due [[Processo|Processi]].
- **Trasporto**: trasferimento dati end-to-end (da un [[host]] sorgente all’host destinatario)
- **Rete**: instradamento dei datagrammi dalla sorgente alla destinazione
- **Link**: trasferimento dati in frame attraverso il collegamento tra elementi di dati vicino
- **Fisico**: trasferimenti dei bit di un frame sul mezzo trasmissivo

![[Pasted image 20230930152619.png]]
In dettaglio: [[Percorso dati TCP-IP]]

Sono previsti due [[Protocollo|Protocolli]] principali:
- [[TCP]]: servizio [[Connection-Oriented]], basato su [[Stream]]
- [[UDP]]: servizio [[Connection-Less]], orientato su messaggio

Da ciò che è scritto sopra sembrerebbe che [[UDP]] sia sempre peggio ma UDP viene utilizzato in quei casi in cui la affidabilità dei dati non è fondamentale, ma è invece importante la [[Velocità di trasmissione]]. UDP è un protocollo di datagramma senza connessione, il che significa che non richiede una connessione stabilita tra mittente e destinatario prima di trasmettere i dati. Questo rende UDP più efficiente di TCP, che è un protocollo di datagramma con connessione.

Infatti per ogni applicazione posso volere requisiti diversi:
- [[Throughput|throughtput]]
- perdita di dati
- sensibilità ai ritardi

Qui una tabella che le esamina caso per caso:

| Applicazione              | tolleranza alla perdita di dati | throughput                                | sensibilità al tempo |
| ------------------------- | ------------------------------- | ----------------------------------------- | -------------------- |
| file transfer             | no                              | elastico                                  | no                   |
| e-mail                    | no                              | elatico                                   | no                   |
| documenti web             | no                              | elastico                                  | no                   |
| audio/video real time     | si                              | audio:5kbps-1Mbps video:10kbps-5Mbps | Si, decine di msec   |
| audio/video memorizzato   | si                              | audio:5kbps-1Mbps video:10kbps-5Mbps  | si pochi secondi     |
| giochi interattivi        | si                              | pochi kbps                                | si, decine di msec   |
| messaggistica instantanea | no                              | elastico                                  | si e no              |                     |                                 |                                           |                      |

e i protocolli che usano:

| Applicazione           | Protocollo di livello di applicazione | Protocollo di trasport |
| ---------------------- | ------------------------------------- | ---------------------- |
| e-mail                 | SMTP [RFC 2821]                       | TCP                    |
| remote terminal access | Telnet [RFC 854]                      | TCP                    |
| Web                    | [[HTTP]] [RFC 2616]                       | TCP                    |
| file transfer          | FTP [959]                             | TCP                    |
| streaming multimedia   | HTTP o RTP [RFC 1889]                 | TCP o UDP              |
| internet telephony     | SIP, RTP, proprietary                 | TCP o UDP                       |
