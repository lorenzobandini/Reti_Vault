Insieme di coppie (nome: valore) che specificano alcuni parametri del messaggio trasmesso o ricevuto.
Ne esistono di vari tipi:
- General Header: relativi alla connessione
- Entity Header:  informazioni relative all'entità tramessa:
	- Content-Base: [[URI]] assoluta da usare per risolvere le [[URL]] relative contenute nell'entity body
	- Content-Encoding: codifica dell'entity body
	- Content-Language: lingua dell'entity body
	- Content-Type: tipo dell'entity body (text, html ...)
	- Expires: validità temporale del contenuto
	- Last-Modified: data dall'ultima modifica sul server
- Request Header: relativi alla richiesta
- Response Header: Informazioni relativi alla risposta che non possono essere inserite nella Status-Line in cui può essere inserita anche la "Location", parametro usato per ridirezionare il ricevente a una [[URI]] differente dalla Request-URI per completare la richiesta o per identificare una nuova risorsa.

