L'obiettivo è realizzare una comunicazione logica fra [[processo|Processi]]
residenti in [[host]] system diversi. Si chiama logico perché è un astrazione per i sistemi applicativi che fanno comunicare i processi come se fossero direttamente collegati.

Offre dei servizi allo [[strato]] di applicazione che possono trasmettere o ricevere dati mediante uno stile di trasporto che preferisce che possono essere:
- Sequenza di messaggi singoli
- Una sequenza continua di byte

Il programma applicativo passa i dati nella forma richiesta al livello di trasporto per la consegna.

Utilizza i servizi dello strato di rete. Il [[livello di rete]] si occupa della comunicazione tra host mentre il [[protocollo]] di rete consegna il datagramma all'host destinatario (e non al processo).

Possiamo dividere lo strato di trasporto in:
- Servizio privo di connessione: Non vengono date garanzia di né di consegna e né di ordine, ma il mittente consegna i messaggi uno ad uno e tratta ogni messaggio come entità singola senza mantenere alcuna relazione fra di essi (Protocollo UDP)
- Servizio orientato alla connessione: client e server stabiliscono una connessione logica cioè che i processi vedono come una connessione diretta punto-punto. Viene usato il protocollo [[TCP]] che gestisce la connessione facendo consegne affidabile e controllo di congestione

Le azioni del livello di trasporto sono
Mittente:
- Riceve un messaggio dal livello applicazione
- Determina i valori dell'header
- Crea il segmento
- Passa il segmento a IP

Destinatario:
- Riceve il segmento da IP
- Controlla i valori dell'header
- Estrae il messaggio del livello applicazione
- Smista il messaggio all'applicazione attraverso la socket

Lo strato di trasporto fa uso del [[Concetto di Multiplexing-Demultiplexing]].

