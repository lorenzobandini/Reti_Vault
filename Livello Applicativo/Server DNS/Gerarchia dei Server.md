Il [[Server]] radice (Root Name server) è responsabile dei record della zona radice e riconosce tutti i domini di massimo livello e conosce il server e risolve ciascun dominio.
Restituisce le informazioni sui name server di TLD (Top-Level-Domain).
Esistono centinaia di root name servers in tutto il mondo.

La gerarchia dei server è composta da:
- **Server top-level domain**: mantiene le informazioni dei nomi di dominio che appartengono a un certo TLD e restituisce informazioni sui name server di competenza dei sottodomini
- **Server di competenza**: autorità per una certa zona, memorizza [[Nome]] e [[Indirizzo IP]] di un insieme di host. Può effettuare traduzione nome/indirizzo per quegli host. Per una certa zona ci possono essere [[Server]] di competenza primari e secondari
	- Server primari mantengono il file di zona
	- Server secondari ricevono il file di zona e offrono il servizio di risoluzione 

Quando un programma deve trasformare un nome in un indirizzo IP chiama un programma in locale detto **resolver**, passando il nome come parametro di ingresso. Se il resolver non ha l'associazione richiesta, interroga un name server di cui conosce l'IP (local name server).
Il local name server cerca il nome nelle sue tabelle, se trova l'associazione restituisce l'indirizzo al resolver, altrimenti inoltra la query alla gerarchia DNS.
Il Local Name Server:
- Non appartiene strettamente alla gerarchia dei server
- Ogni ISP ha il suo default name server locale
- Le query [[DNS]] vengono prima rivolte al name server locale che opera da proxy e inoltra la query in una gerarchia di server DNS

Una query può essere:
- Ricorsiva: il local name server ha richiesto una conversione completa
- Iterativa: Le risposte sono restituite direttamente dal client e viene restituito il riferimento al server da contattare successivamente

Prendendo per esempio un client che vuole l'IP di "\www.amazon.com" la risoluzione dei nomi avviene con i seguenti passaggi:
1. Il client interroga il server radice per trovare il server DNS "com"
2. Il client interroga il server DNS "com" per ottenere il server DNS "amazon.com"
3. Il client interroga il server DNS "amazon.com" per ottenere l'indirizzo IP di "\www.amazon.com"

Una volta che un name server ha appreso un associazione, la mette nella cache per migliorare il ritardo e ridurre il numero di [[Messaggi DNS]]
