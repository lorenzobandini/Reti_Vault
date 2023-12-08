Raffinamento di [[CSMA]] ma con Collision Detection cercando di ridurre le perdite. La collision detection è facile in [[LAN]] cablate e difficile in [[LAN]] wireless.

L'algoritmo [[ethernet]] CSMA/CD funziona nei seguenti passi:
1. **Ricezione del datagramma dalla rete:** La scheda di rete riceve un datagramma dal [[livello di rete]].
2. **Creazione del frame:** La scheda di rete crea un frame contenente il datagramma ricevuto dal livello di rete.
3. **Inizio della trasmissione del frame:** Se la scheda di rete rileva che il canale è inattivo, inizia la trasmissione del frame altrimenti attende finché il canale diventa inattivo e poi inizia la trasmissione.
4. **Completamento della trasmissione del frame:** Se la scheda di rete riesce a trasmettere l'intero frame senza rilevare altre trasmissioni, considera la sua operazione con il frame completata.
5. **Rilevamento di una collisione durante la trasmissione:** Se la scheda di rete rileva un'altra trasmissione durante il [[processo]] di trasmissione del frame, interrompe immediatamente la trasmissione e invia un segnale di "jam" per notificare a tutte le stazioni coinvolte di una collisione.
6. **Procedura di backoff binario (esponenziale) dopo una collisione:** Dopo una collisione, la scheda di rete entra in un periodo di attesa chiamato backoff binario, altrimenti dopo la $m$-esima collisione, la scheda di rete sceglie casualmente un numero $K$ da un insieme di valori. Quindi attende $K$ volte 512 bit prima di ritentare la trasmissione.

![[Pasted image 20231202184828.png]]
