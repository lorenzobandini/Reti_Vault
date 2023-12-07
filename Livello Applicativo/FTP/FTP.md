Acronimo di File Transfer Protocol, serve per il trasferimento file a/da un host remoto e segue il modello [[Client-Server]] dove:
- [[Client]]: il lato che richiede il trasferimento
- [[Server]]: host remoto

![[Pasted image 20231018152047.png]]

FTP è lo standard per il trasferimento di file in reti [[Stack Protocollare TCP-IP|TCP-IP]], diverso dall'accesso condiviso on-line.
Il trasferimento file si ha facendo una copia locale nella quale si effettuano le modifiche e poi si può fare un eventuale trasferimento del file modificato in remoto.
Ma FTP fornisce funzionalità aggiuntive rispetto al semplice trasferimento file:
- un accesso interattivo, in quanto un utente può navigare e cambiare/modificare l'albero di directory nel file system remoto
- specifica del formato dei dati da trasferire
- autenticazione in quanto il client può specificare login e password

Il modello FTP è un [[Protocollo]] Stateful in quando il server deve tenere traccia dello stato dell'utente (connessione di controllo associata ad un account, directory attuale, ecc...)
Ha un totale di due tipi di connessione, le quali entrambe utilizzano il protocollo di trasporto TCP:
- [[Control Connection]]
- [[Data Connection]]

![[Pasted image 20231018161313.png]]

Quando il client attiva la connessione di controllo con il server, usa un numero di porta assegnato localmente in modo casuale e contatta il server ad una porta nota (21).
FTP usa la connessione di controllo per permettere a client e server di coordinare l'uso delle porte assegnate dinamicamente per il trasferimento dati
La comunicazione sulla connessione di controllo avviene per mezzo di caratteri con una codifica standard NVT ASCII, sia per i comandi che per le risposte.

Per creare la connessione TCP per il trasferimento dati sono possibili due modalità:
- Active Mode: il server apre una connessione dati TCP con il client e deve conoscere il numero di porta lato client (il client gliela comunica sulla connessione di controllo)
- Passive Mode: il client chiede al server di mettersi in ascolto su una porta per una connessione dati, ottiene un numero di porta dal server e lo usa per aprire la connessione con il server. Il comando PASV richiede al server di ascoltare su una porta dati e di aspettare la connessione.

I dispositivi dove risiedono client e server FTP sono diversi, sistema operativo, strutture per gestire i file, diversi formati dei file, e quindi per effettuare il trasferimento file, il client deve definire il tipo di file, la struttura dati e la modalità di trasmissione al fine di risolvere eventuali problemi di eterogeneità tra client e server. Il trasferimento file viene preparato attraverso uno scambio di informazioni lungo la connessione di controllo.

Le modalità di trasmissione possono essere:
- Stream mode: FTP invia i dati a TCP con un flusso continuo di bit
- Block mode: FTP invia i dati a TCP suddivisi in blocchi, ognuno dei quali è preceduto da un header
- Compressed mode: si trasmette il file compresso 

Esistono anche gli Anonymous FTP, cioè server che supportano connessioni FTP senza autenticazione. Tipicamente consentono di accedere solo ad una parte del file system e permettono solo un subset di operazioni.

I comandi di controllo sono:

| <span style='color:#0fb9b1'>Comandi</span>       | <span style='color:#f7b731'>Azione</span>                                                  |
| ------------- | ------------------------------------------------------- |
| USER          | username                                                |
| PASS          | password                                                |
| LIST          | elenca i file della directory corrente                  |
| NLST          | richiede elenco file e directory                        |
| RETR filename | recupera un file dalla directory corrente               |
| STOR filename | memorizza un file nell'host remoto                      |
| ABOR          | interrompe l'ultimo comando ed i trasferimenti in corso |
| PORT          | indirizzo e numero di porta del client                  |
| SYST          | il server restituisce il tipo di sistema                |
| QUIT          | chiude la connessione                                   |


I codici di ritorno sono:

| <span style='color:#8854d0'>Codice</span> | <span style='color:#fa8231'>Significato</span>            |
| ----------------------------------------- | --------------------------------------------------------- |
| 125                                       | Data connection already open; transfer starting           |
| 200                                       | Comando OK                                                |
| 225                                       | Data connection open                                      |
| 226                                       | Closing data connection. Requested file action succesfull |
| 227                                       | Entering passive mode                                     |
| 331                                       | Username OK, password required                            |
| 425                                       | Can't open data connection                                |
| 426                                       | Connection closed; transfer aborted                       |
| 452                                       | Error writing file                                        |


