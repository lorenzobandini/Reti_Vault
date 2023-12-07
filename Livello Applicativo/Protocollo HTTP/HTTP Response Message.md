La prima riga di un messaggio di risposta è la Status-Line che contiene:
- Status-Code: intero a tre cifre che rappresenta un codice di risultato dell'operazione richiesta
- Reason-Phrase: descrizione testuale dello Status-Code (pensata per l'utente umano)

Nell'[[Header HTTP]] vengono inserite informazioni che non possono essere inserite nella Status-Line come la Location.

![[Pasted image 20231004121537.png]]

In particolare, dallo standard, lo Status-Code indica :
- 1xx: Informativa - Richiesta ricevuta, processo in corso.
- 2xx: Successo - L'azione è stata ricevuta, compresa e accettata con successo.
- 3xx: Reindirizzamento - È necessario compiere ulteriori azioni per completare la richiesta.
- 4xx: Errore del client - La richiesta contiene una sintassi errata o non può essere soddisfatta.
- 5xx: Errore del server - Il server non è riuscito a soddisfare una richiesta apparentemente valida.