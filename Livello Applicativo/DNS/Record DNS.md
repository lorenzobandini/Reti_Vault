Sono l'entità più piccola che contiene l'informazione esatta relativa "all'appartenenza" di un determinato [[dominio]] a un indirizzo di destinazione.
Il nome completo è Resource Records (RR).
Il formato è: **(Nome, Valore, Tipo, TTL)**
dove TTL (Time-To-Live) indica dopo quanto la risorsa dovrà essere rimossa dalla cache mentre Nome e Valore dipendono dal Tipo.
Alcuni esempi:
- Type = A
	- Nome: Hostname
	- Valore: [[Indirizzo IP]]
- Type = NS
	- Nome: [[Nome di dominio]]
	- Valore: Hostname dell'authoritative name server per quel dominio
- Type = CNAME
	- Nome: Hostname (sinonimo)
	- Valore: Nome canonico dell'host
- Type = MX
	- Nome: Nome del dominio
	- Valore: Nome canonico del server di posta associato al nome

