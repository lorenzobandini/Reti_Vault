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

