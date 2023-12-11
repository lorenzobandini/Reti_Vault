Prevede di dividere le funzionalità del [[Protocollo]] di telecomunicazione in strati o layers ognuno dei quali svolge una parte piccola e indipendente dalle altre allo scopo di permettere una realizzazione o revisione delle singole funzionalità senza dovere toccare le altre o anche di permettere una compatibilità a livelli diversi tra diverse implementazioni.
La comunicazione tra i vari livelli è assicurata da chiamate standard; ogni livello è tenuto a rispondere in maniera corretta alle chiamate che gli competono e che verranno generate dai due livello ad esso adiacenti.([[Interfaccia]])
La modalità con cui le funzioni competenti ad un livello vengono svolte non è visibile dall'esterno che ne è così svincolato.([[Incapsulamento dei Dati]])

Si divide in 7 livelli
1. Fisico: tramette un flusso di bit.
2. Datalink: Consegna trame sul link
3. Rete: Instradamento nel traffico
4. Trasporto: Trasferimento dati fra due [[host]]
5. Sessione: Controllo del dialogo
6. Presentazione: Unificazione dati
7. Applicazione: Elaborazione dati

![[Pasted image 20230927115422.png]]

In particolare:
- Livello fisico:
	- comprende tutte le funzioni (procedure meccaniche ed elettroniche) che permettono una connessione a livello fisico
	- si occupa della trasmissione dei bit attraverso il mezzo trasmissivo e delle caratteristiche di cavi e connettori
- Livello datalink (collegamento):
	- definisce le regole per inviare e ricevere informazioni tra due sistemi di comunicazione
	- permette di trasferire affidabile ai dati attraverso il livello fisico
	- si occupa di formare i dati da inviare attraverso il livello fisico incapsulando i dati in un pacchetto provvisto di header (intestazione) e tail (coda), chiamato frame
- Strato di rete:
	- deve far giungere i "pacchetti" a destinazione
	- si occupa dell'instradamento ("[[routing]]") dei pacchetti cioè di determinare la sequenza di collegamenti punto-punto necessari per trasmettere un pacchetto da un nodo generico della rete a un altro
- Strato di trasporto:
	- questo strato fornisce un servizio di trasferimento dati end-to-end
	- si occupa di instaurare, mantenere e terminare una connessione
	- può offrire funzionalità per frammentare e riassemblare i dati, rilevare e correggere gli errori e controllare il flusso dei dati
- Strato sessione:
	- assembla il dialogo tra nodi in unità logiche
- Strato di presentazione:
	- adatta la sintassi dei dati di ciascuna applicazione alla sintassi richiesta dalla sessione
- Strato di applicazione:
	- protocolli a supporto di applicazione distribuite

Le modalità di servizio possono essere:
- [[Connection-Oriented]]
- [[Connection-Less]]

Per la rete l'informazione ha origine al livello applicativo e scende i vari livelli fino alla trasmissione sul canale fisico e ogni livello aggiunge all'informazione del livello superiore una propria sezione informativa (un header che contiene informazioni riguardanti esclusivamente quel livello).
Per i dati ricevuti si segue il cammino inverso.
Per farlo è necessario un processo di [[Incapsulamento dei Dati]] tra i vari livelli in modo che rimangano intoccati da chi non deve.
Il processo è reversibile in modo tale da garantire la possibilità di estrarre i dati precedentemente incapsulati.
Durante il processo di incapsulamento dei dati per livello il pacchetto è diviso in:
- Header: qualificazione del pacchetto dati per questo livello
- DATA: payload proveniente dal livello superiore
- Trailer: generalmente usato in funzione di trattamento dell'errore

![[Pasted image 20230930152247.png]]
