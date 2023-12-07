Acronimo di Border Gateway Protocol, è l'unico INTER-AS usato in [[Internet]] ed è di tipo [[Algoritmo Distance Vector]] decentralizzato e asincrono.
Le coppie di router si scambiano info su connessioni [[TCP]] tramite sessioni BGP esterne (eBGP) e sessioni BGP interne (iBGP).

Si preoccupa dell'aggregazione degli indirizzi rappresentando destinazioni da prefissi CIDR (Classless Inter-Domain Routing). 

BGP mette a disposizione di ciascun router un modo per:
- Ottenere informazioni sulla raggiungibilità dei prefissi di sottorete da parte dei sistemi confinanti
- Determinare i percorsi ottimi verso le sottoreti

Pubblicizzare un prefisso significa impegnarsi ad instradare pacchetti destinati a reti in quel prefisso.

Per la distribuzione di informazioni su raggiungibilità:
- eBGP: gateway riceve informazioni da gateway di altri [[Sistemi Autonomi]] su sessione eBGP
- iBGP: gateway distribuisce informazioni ai router interni della propria rete su sessioni iBGP

Un Advertisement (ADV) si riferisce all'annuncio di una route da parte di un router a un altro all'interno di uno stesso sistema autonomo (iBGP) o tra sistemi autonomi diversi (eBGP). Quando un router ha informazioni su una route valida, invia un messaggio di Advertisement contenente il prefisso della route e i relativi attributi a tutti i suoi peer BGP.

Una "route" rappresenta il percorso che il traffico di rete segue da una sorgente a una destinazione ed è costituita da prefisso più attributi.

I due attributi più importanti sono:
- AS_PATH: sequenza degli AS attraversati nel path pubblicizzato dall'advertisement
- NEXT_HOP: indica l'indirizzo IP del primo router lungo un percorso annunciato a un dato prefisso di rete

Il policy-based routing in BGP consente agli amministratori di configurare politiche flessibili per la gestione del traffico.
Questo approccio permette ai gateway di ricevere route advertisements e applicare politiche di importazione per accettare o rifiutare percorsi specifici.
Il gateway, al ricevere un annuncio di route, applica una politica di importazione per decidere se accettare o rifiutare il percorso specificato nell'annuncio.
Si usa l'AS policy anche per determinare se advertise il percorso ad altri AS vicini.

La scelta delle rotte in BGP è guidata da regole specifiche durante il processo di selezione del percorso ottimale per un determinato prefisso.
Un router può riceve più di una rotta per lo stesso prefisso e quindi segue una sequenza di regole:
1. Vengono selezionati quelli coi valori più alti
2. In caso di parità di preferenza locale, si preferisce il percorso con l'AS_PATH più breve per ottimizzare il percorso attraverso la rete
3. Se le route hanno la stessa preferenza locale e lunghezza di AS_PATH, si preferisce il percorso che ha l'interfaccia NEXT-HOP più vicina, seguendo il principio di "hot potato routing."

Una sessione BGP è un'interazione tra due router BGP, chiamati "peers", in cui scambiano messaggi BGP tramite una connessione TCP stabile nel tempo. Il termine "peers" indica che questi due router stanno cooperando per lo scambio di informazioni di routing.

Il protocollo BGP è un protocollo "path vector", il che significa che, durante questa sessione, i router stanno annunciando percorsi (routes) specifici relativi a diversi prefissi di rete di destinazione. Un "prefisso di rete" indica un blocco specifico di indirizzi IP associato a una destinazione nella rete.