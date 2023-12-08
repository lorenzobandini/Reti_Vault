In molte situazioni, un frame di broadcast, viene utilizzato per uno scopo e quindi può contenere informazioni utili solo a un particolare reparto. Per non sprecare la capacità di trasmissione delle [[LAN]] e degli [[switch]] e per mantenere una sicurezza si usano le VLAN, che stanno per "Virtual Local Area Network".

Una VLAN è una tecnologia di rete che consente di creare più reti logiche all'interno di una singola rete fisica. Questa suddivisione logica permette di separare gruppi di dispositivi in differenti segmenti di rete, anche se sono fisicamente connessi alla stessa infrastruttura di rete.

Riunisce le stazioni utente e i dispositivi di rete in un unico [[dominio]] di broadcast, indipendentemente al segmento fisico della LAN a cui sono collegati.
Gli [[host]] all'interno di una VLAN comunicano tra loro come se fossero tutti connessi e nessun altro allo switch.

![[Pasted image 20231205182324.png]]

Gli switch possono supportare più VLAN su una singola infrastruttura LAN.

Un modi per considerare le VLAN è VLAN basato sulle porte cioè raggruppare un insieme di porte fisiche in uno switch e considerarle come uno singolo. Ha il vantaggio che possiamo assegnare dinamicamente le porte. Quando voglio far comunicare due host di due VLAN diverse utilizziamo il [[router]] come intermezzo.
Una porta di uno switch può anche collegarsi ad un altro switch e combinare le VLAN degli switch se vogliamo attraverso una trunk port. 
Per distinguere il traffico aggiungiamo un etichetta per distinguere il traffico tra VLAN ed utilizziamo lo standard 802.1Q che aggiunge dei campi al frame [[ethernet]].
![[Pasted image 20231206121855.png]]
Dopo che viene processato, le etichette vengono rimosse dato che non interessano.

Altri modi per definire VLAN sono definire le VLAN in base agli indirizzi MAC degli host oppure definire le VLAN in base ai protocolli a [[livello di rete]].