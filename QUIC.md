Protocollo di trasporto che sfrutta [[UDP]] ed è [[Connection-Oriented]].
Aggiunge:
- Controllo del flusso e della congestione
- Rilevazione delle perdite e ritrasmissione

Ha un approccio avanzato in cui diversi "flussi" a livello di applicazione possono essere multiplexati su una singola connessione QUIC. Ciò significa che più canali di comunicazione possono coesistere e condividere la stessa connessione senza interferire l'uno con l'altro.

Un aspetto chiave è l'astrazione dello stream, che è gestito a livello di trasporto. In termini più semplici, QUIC organizza e gestisce i dati in "flussi" distinti all'interno di una connessione. Ogni flusso rappresenta un canale di comunicazione indipendente, consentendo una separazione chiara delle diverse attività o tipi di dati.

In linea di massima quindi, QUIC si dimostra superiore a TCP in termini di prestazioni, rappresentando un passo avanti nella modernizzazione delle comunicazioni su Internet. 
Nonostante i chiari vantaggi di QUIC nelle comunicazioni su Internet, emergono alcune problematiche prestazionali in contesti specifici. La gestione di pacchetti riordinati è stata identificata come una sfida, evidenziando criticità nel protocollo. Anche il multiplexing di un elevato numero di piccoli oggetti rappresenta un'area di attenzione, con una potenziale diminuzione dell'efficienza di QUIC in scenari con numerosi elementi di dimensioni ridotte. Un aspetto rilevante è la riduzione delle prestazioni di QUIC su dispositivi mobili e reti cellulari, indicando che, nonostante i benefici in termini di riduzione del ritardo e prestazioni generali, il protocollo potrebbe non essere sempre la scelta ottimale in ambienti mobili e su reti cellulari.


