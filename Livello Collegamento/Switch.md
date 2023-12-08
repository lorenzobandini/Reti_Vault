Dispositivo di rete utilizzato per instradare il traffico dati all'interno di una [[LAN]] o tra reti.

Operano sia a livello fisico rigenerando il segnale e sia a livello di collegamento verificando indirizzi MAC contenuti in frame.
Hanno la capacità di immagazzinare e inoltrare frame [[Ethernet]]. Esamina gli indirizzi MAC dei frame in arrivo e li inoltra in modo selettivo su uno o più collegamenti seguendo una tabella.
![[Pasted image 20231205175201.png]]

Sono dispositivi trasparenti dato il fatto che gli [[host]] non sono a conoscenza della presenza degli switch ma non devono essere manco configurati dato che usufruiscono di un auto-apprendimento. Più switch ad auto-apprendimento possono essere collegati.
![[Pasted image 20231205175405.png]]

Gli host hanno connessioni dedicate verso lo switch che bufferizzano i pacchetti evitando così collisioni.

I passi che svolge uno switch sono:
1. Registra il collegamento in entrata e l'[[indirizzo MAC]] dell'host mittente.
2. Indice della tabella dello switch usando l'indirizzo MAC di destinazione
3. Se è presente una voce per la destinazione nella tabella dello switch vengono prese alcune decisioni:
    - Se la destinazione è sulla stessa segmento da cui è arrivato il frame il frame viene scartato, poiché significa che il destinatario è sulla stessa rete e il frame non deve essere inoltrato.
    - Altrimenti, inoltra il frame sulla porta indicata dalla voce della tabella lo switch inoltra il frame sulla porta corretta, sulla base delle informazioni contenute nella tabella.
4. Se non esiste una voce nella tabella dello switch per la destinazione, lo switch adotta una strategia di "flood" cioè inoltra il frame su tutte le porte tranne quella da cui è arrivato il frame.
 


