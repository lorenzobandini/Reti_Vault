Tempo richiesto affinché un messaggio arrivi a destinazione dal momento in cui il primo bit parte dalla sorgente.
Il ritardo ha 4 cause:
- **Ritardo di elaborazione** del nodo che comprende:
	- controllo errori sui bit
	- determinazione del canale di uscita
- **Ritardo di accodamento** nel buffer di output del [[router]] in attesa della trasmissione
- **Ritardo di trasmissione**: è il tempo impiegato per tramettere un pacchetto sul link e si calcola con $(L/R)$ dove $L$ è la lunghezza del pacchetto in bit e $R$ sta per rate di trasmissione (bps)
- **Ritardo di propagazione** è il tempo impiegato da 1 bit per essere propagato da un nodo all'altro e si calcola con $(d/s)$ dove $d$ è la lunghezza del collegamento fisico e $s$ è la velocità di propagazione del mezzo

![[Immagine 2023-09-26 175448.png]]
