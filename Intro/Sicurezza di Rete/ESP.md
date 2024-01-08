Acronimo di Encapsulating Security Payload, è uno dei protocolli principali utilizzati all'interno di [[IPSec]] per garantire la sicurezza delle comunicazioni su reti IP.

Ha come obiettivi l'autenticazione della sorgente, l'integrità e la riservatezza.

Per creare il pacchetto IPSec applicato ad ESP bisogna:
1. Aggiungere tralir ESP
2. Payload e trailer ESP vengono crittografati
3. Viene aggiunta intestazione ESP
4. Intestazione ESP, payload e trailer ESP vengono usati per generare dati autenticazione (che vengono aggiunti dopo trailer ESP)
5. Viene aggiunta intestazione IP (impostando campo [[protocollo]] a 50)

L'ESP trailer è formato da:
- Padding: valori 0 di riempimento
- Pad Length: quanti byte aggiuntivi di padding sono stati inseriti
- Next Header: tipo di payload contenuto nel [[datagramma IP]]

L'intestazione ESP è formata da:
- SPI: identificatore della SA
- Sequence number per prevenire gli attacchi a ripetizione di pacchetto

![[Schermata 2024-01-07 alle 21.37.45.png]]
