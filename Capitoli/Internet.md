Internet è un interconnessione di sistemi autonomi di reti più piccole.
Se un sistema si vuole aggiungere ad Internet basta che si adegui all'Internet Protocol.
I protocolli sono dappertutto, dall'invio e ricezione dei messaggi fino ai servizi [[HTTP]], streaming video, Ethernet...

Internet è composto da:
- Dispositivi connessi (hosts o sistemi terminali):
	- Macchine di proprietà degli utenti finali: dedicate a eseguire applicazioni (computer, portatile, cellulare...)
	- Server: computer con elevate prestazioni destinati a eseguire programmi che forniscono servizio a diverse applicazioni utente
- Reti di accesso e link di comunicazione: fibra ottica, rame, onde radio...
- Dispositivi di Interconnessione:
	- [[Router]]
	- [[Switch]]
- Reti: insiemi di hosts, dispositivi di interconnessione e link gestiti da una organizzazione in grado di scambiarsi informazioni

Internet è un'infrastruttura che offre servizi alle applicazioni (web, streaming video, email...) e offre un'interfaccia di programmazione alle applicazioni distribuite che permette alle app mittenti e destinatarie di collegarsi ed usare il servizio di trasporto di internet.

Le reti possono essere:
- [[Local Area Netword (LAN)]]
- [[Wide Area Network (WAN)]]
- [[Metropolitan Area Network (MAN)]]

Internet è un insieme mondiali di reti interconnesse, non possedute da nessun individuo o gruppo, che collaborano tra loro per scambiarsi informazioni utilizzando standard comuni (IP) utilizzando tecnologie e standard coerenti e comunemente riconosciuti. 
Le organizzazioni per aiutare e mantenere la struttura di internet sono:
-  Internet Engineering Task Force (IETF)
- Internet Corporation for Assigned Names and Numbers (ICANN)
- Internet Architecture Board (IAB), oltre a molte altre.

Dati molti punti [[Internet Service Provider (ISP)]]non è efficace connetterli tutti tra di loro al costo $O(N^2)$ perché la connessione non scala, perciò vengono tutti collegati ad un gruppo di [[Internet Service Provider (ISP)]] di transito globale con un accordo economico.
Questa attività, essendo redditizia avrà dei concorrenti, ognuno con il proprio gruppo di [[Router]].
Per far comunicare due [[Internet Service Provider (ISP)]] vengono usati dei peering link che accettano e inoltrano il traffico tra i due.
I peering link possono essere a loro volta degli [[Internet eXchange Point (IXP)]].
Tra gli [[Internet Service Provider (ISP)]] e i hosts spesso vengono usati dei Regional Isp per mediare la comunicazione.
Quindi il sistema di Internet diventa una rete dove al centro abbiamo delle reti molto connesse che poi si diramano fino a raggiungere ogni host.

