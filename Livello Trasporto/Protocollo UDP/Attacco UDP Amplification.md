[[UDP]] è un [[protocollo]] senza [[connessione]] che non controlla gli [[indirizzo IP|Indirizzi IP]] di origine per cui:
- Un utente malintenzionato può facilmente forgiare un pacchetto per usare un indirizzo IP di origine arbitrario (in questo caso è l’IP della vittima).
- L’attaccante invia numerosi pacchetti UDP con l'indirizzo IP di origine falsificato ad un [[server]] di destinazione (o amplificatore).
- Il server risponde alla vittima (anziché all'attaccante), creando un attacco DoS (Denial of Service) riflesso.
- Si basa sul fatto che alcuni protocolli applicativi che usano UDP possono generare risposte molto più grandi della richiesta iniziale.

![[Pasted image 20231110180010.png]]