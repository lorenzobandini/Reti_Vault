Tecnica utilizzata per migliorare le prestazioni e ridurre il carico sui [[server]] web e consiste nell'archiviare temporaneamente in cache le risorse web. Queste risorse vengono quindi fornite direttamente dalla cache invece di essere richieste e ottenute nuovamente dal server web di origine ogni volta che vengono richieste.
L'utente configura il browser in modo che punti a una cache web alla quale inviare tutte le [[HTTP Request Message]]; se la cache ha l'oggetto viene restituito al [[client]] altrimenti la cache richiedo l'oggetto al server di origine, lo memorizza per le successive volte e lo restituisce al client.
La cache web funge sia da client verso il server di origine che da server per il client richiedente ed ha i vantaggi di:
- Ridurre i tempi di risposta essendo la cache più vicina al client
- Ridurre il traffico sui collegamenti
- Consentire ai piccoli fornitori di contenuti di tutto il mondo di fornire contenuti in modo più efficace
