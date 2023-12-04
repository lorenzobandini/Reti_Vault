L'indirizzo LAN è un indirizzo del livello collegamento, tipicamente permanente, associato alla scheda di rete e non al nodo che viene chiamato anche indirizzo fisico o indirizzo MAC. Per le LAN Ethernet e IEEE è lungo 6 byte (48 bit) ed è espresso in notazione esadecimale.
Per garantire l'univocità IEEE definisce ed assegna i primi 24 bit mentre i rimanenti 24 bit vengono gestiti dalle aziende ed assegnati a livello locale.
Quando una società vuole costruire adattatori, compra un blocco di spazio di indirizzi.

Ciascun adattatore di una LAN ha un indirizzo LAN univoco. Un adattatore inserisce l'indirizzo LAN di destinazione per spedire un frame:
- il LAN broadcast il frame sarà ricevuto ed elaborato da tutti gli adattatori della LAN
- Ogni scheda controlla se l'indirizzo MAC corrisponde al proprio
- In caso positivo estrae il datagramma e lo passa al livello superiore
- In caso negativo scarta il datagramma

![[Pasted image 20231204155552.png]]

Quando un adattatore spedisce un frame, vi inserisce l'indirizzo MAC della sched