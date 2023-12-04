L'indirizzo MAC è un indirizzo del livello collegamento, tipicamente permanente, associato alla scheda di rete e non al nodo che viene chiamato anche indirizzo fisico o indirizzo LAN. Per le LAN Ethernet e IEEE è lungo 6 byte (48 bit) ed è espresso in notazione esadecimale.
Per garantire l'univocità IEEE definisce ed assegna i primi 24 bit mentre i rimanenti 24 bit vengono gestiti dalle aziende ed assegnati a livello locale.
Quando una società vuole costruire adattatori, compra un blocco di spazio di indirizzi.

Ciascun adattatore di una MAC ha un indirizzo MAC univoco. Un adattatore inserisce l'indirizzo MAC di destinazione per spedire un frame:
- il LAN broadcast il frame sarà ricevuto ed elaborato da tutti gli adattatori della LAN
- Ogni scheda controlla se l'indirizzo MAC corrisponde al proprio
- In caso positivo estrae il datagramma e lo passa al livello superiore
- In caso negativo scarta il datagramma

![[Pasted image 20231204155552.png]]

Quando un adattatore spedisce un frame, vi inserisce l'indirizzo LAN della scheda di destinazione.
Nel caso di reti LAN broadcast, tutti gli adattatori attestati sulla rete controllano l'indirizzo destinazione e passano i dati allo stato superiore solo se riconoscono il proprio indirizzo LAN.
Se un adattatore trasmittente vuole che tutte le schede di rete passino i dati agli strati superiori, immette nel campo indirizzo destinazione `FF-FF-FF-FF-FF-FF` ovvero l'indirizzo broadcast.
La risoluzione degli indirizzi è svolta dal protocollo [[ARP]].