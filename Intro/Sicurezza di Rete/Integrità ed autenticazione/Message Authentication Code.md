Anche chiamato MAC, è un tipo di codice di autenticazione dei messaggi, che viene utilizzato per garantire l'integrità e l'autenticità dei dati trasferiti tra parti di un sistema di comunicazione.
Il MAC è generato tramite l'utilizzo di una chiave segreta condivisa tra mittente e destinatario ed è implementato utilizzando algoritmi di hash crittografici insieme a una chiave segreta.

Il mittente:
- Prdcuce MAC dala funzione hash $H(M+K)$
- Invia M e Mac su canale non sicuro

Il destinatario:
- Ricalcola $H(M+K)$
- Confronta MAC calcolato e ricevuto


![[Schermata 2024-01-07 alle 18.15.00.png]]