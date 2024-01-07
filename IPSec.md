IPSec è un insieme di protocolli per fornire sicurezza a livello rete.
Si occupa dell'autenticazione e confidenzialità dei pacchetti IP in:
-  Modalità trasporto se proteggi solo il payload del pacchetto IP passate da livello trasporto a livello di rete ![[Schermata 2024-01-07 alle 19.25.18.png]]
- Modalità tunnel se protegge l'intero pacchetto IP compresi gli header Ip originali e il payload del pacchetto![[Schermata 2024-01-07 alle 19.25.47.png]]

Da un punto di vista più ampio:

![[Schermata 2024-01-07 alle 19.27.05.png]]

Per definire i parametri necessari per proteggere il traffico tra due [[Router]] su una rete IP e le politiche di sicurezza si utilizzano le Security Associations ([[SAs]]).

I protocolli principali di IPSec sono:
- Encapsulating Security Payload ([[ESP]])
- Authenticathor Header ([[AH]])

Dopo questi passaggi il datagramma IPSec è della forma:

![[Schermata 2024-01-07 alle 21.41.22.png]]