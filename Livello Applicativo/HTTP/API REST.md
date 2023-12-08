Acronimo di "Application Programming Interface Representational State Transfer", è un affermata interfaccia API per servizi web utile e versatile che consente alle applicazioni di servizi web di comunicare fra loro, ideato per funzionare con qualsiasi [[protocollo]] ma utilizzato prevalentemente in [[HTTP]] trasferendo dati JSON.

Il processo inizia quando un client nell'architettura REST usa comandi HTTP per inviare richieste al server. Una volta inviata una richiesta dal client, la API REST ottiene e fornisce una risposta contenente varie risorse ma non inviate come risorse vere e proprie ma con una loro rappresentazione in formato JSON leggibile sia da persone che da macchine e compatibile con la maggior parte dei linguaggi.

--- 

Esempio per capire simpatico:

Le API REST sono come un menu in un ristorante.

Immagina di andare in un ristorante e di vedere un menu con elencati i piatti disponibili. Ogni piatto ha un nome (l'[[URL]]), una descrizione (i dati), e delle istruzioni su come richiederlo o personalizzarlo (i [[Metodi HTTP]]).

- Quando vuoi sapere cosa c'è nel menu, dai un'occhiata (richiesta [[GET]]).
- Quando desideri ordinare un nuovo piatto, lo chiedi al cameriere (richiesta [[POST]]).
- Se vuoi modificare un piatto che hai già ordinato, dici al cameriere come vuoi che sia cambiato (richiesta [[PUT]] o PATCH).
- Se hai finito di mangiare un piatto, chiedi al cameriere di toglierlo dal tavolo (richiesta [[DELETE]]).

Le API REST funzionano in modo simile. Rappresentano risorse (come piatti) tramite URL, e puoi eseguire diverse azioni su di esse utilizzando metodi HTTP. È come comunicare con un ristorante web attraverso richieste HTTP per ottenere, creare, aggiornare o eliminare dati.