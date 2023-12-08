Applicazioni formate da [[Processo|Processi]] distribuiti comunicanti.
All'interno dello stesso [[host]], due processi possono comunicare, due processi possono anche comunicare attraverso la comunicazione inter-processo definita dal sistema operativo mentre nella comunicazione a livello applicativo tra due dispositivi terminali diversi in una reti, due o più processi girano su ciascuno degli host comunicanti e si scambiano messaggi.

Il [[Protocollo]] dello strato di applicazione definisce i tipi di messaggi scambiati a livello applicativo, la sintassi, la semantica e le regole per determinare quando e come un processo invia e risponde ai messaggi.

Per ogni applicazione bisogna decidere il paradigmi del livello applicazione adatto tra i seguenti:
-  [[Client-Server]]
- [[Peer-to-Peer (P2P)]]
- Misto

Ogni applicazione di rete ha più componenti. Due esempi possono essere:
- **Web**
	-  browser sul [[client]]
	- [[server]] web
	- standard per il formato dei documenti
	- protocollo [[HTTP]]
- **Posta elettronica**
	- standard per il formato dei messaggi
	- programmi di lettura/scrittura sul client
	- server di posta di [[Internet]]
	- protocolli [[SMTP]], [[POP3]], ecc.

Alcune terminologie delle applicazioni di rete sono  [[Application Program Interface (API)]] e poi [[Interfaccia socket]].

In qualche modo bisogna anche [[Indirizzare Processi]] e per farlo utilizziamo le famiglie di [[Protocollo|Protocolli]] come [[Modello ISO-OSI]] e [[Stack Protocollare TCP-IP]].


