Dal nome completo Uniform Resource Locator, è un sottoinsieme di [[URI]] che identifica le risorse attraverso il loro meccanismo di accesso.

La sua sintassi è:
<center> <span style='color:#0fb9b1'>&lt scheme &gt</span> :// <span style='color:#0fb9b1'>&lt user &gt</span> : <span style='color:#0fb9b1'>&lt password &gt</span> @ <span style='color:#0fb9b1'>&lt host &gt</span> : <span style='color:#0fb9b1'>&lt port &gt</span> / <span style='color:#0fb9b1'>&lt path &gt</span> </center> 

- \<user> e \<password> opzionalmente e generalmente deprecate
- scheme: [[Protocollo]] di accesso alla risorsa ([[HTTP]], HTTPS, FTP, FTPS...)
- host è il nome di dominio di un host o indirizzo IP in notazione decimale puntata
- port è il numero di porta del server. Molti protocolli hanno porte di default (come 80 per http)
- Path contiene dati specifici per l'host e identifica la risorsa nel contesto di quello schema e host

Le URL possono essere:
- URL assolute: identificano una risorsa indipendentemente dal contesto in cui è usata
- URL relative: informazioni per indicare una risorsa in relazione ad un'altra URL. Non viaggia sulla rete e sono interpretate dal browser in relazione al documento di partenza.