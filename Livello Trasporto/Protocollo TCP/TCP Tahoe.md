TCP Tahoe è una delle prime implementazioni del controllo di congestione in [[TCP]], un [[protocollo]] utilizzato per trasmettere dati su reti informatiche. TCP Tahoe introduceva un meccanismo di controllo della congestione per regolare la [[velocità di trasmissione]] dei dati e prevenire la congestione e la perdita di pacchetti nella rete.

Il funzionamento di TCP Tahoe si basa su alcuni concetti chiave:

1. **Controllo della congestione:** TCP Tahoe monitora la congestione della rete. Quando rileva una congestione, riduce la finestra di congestione per limitare il flusso di dati. Questo è noto come "slow start".
2. **Rilevamento di perdite:** Quando vengono rilevate perdite di pacchetti, TCP Tahoe reagisce riducendo la finestra di congestione a metà (conosciuto come "congestion avoidance") per ridurre il carico sulla rete.
3. **Ritrasmissione selettiva:** Quando si verifica una perdita di pacchetti, TCP Tahoe può ritrasmettere solo i pacchetti mancanti anziché l'intera finestra di trasmissione. Questo aiuta a migliorare l'efficienza della trasmissione.

Quello che cambia è che Timeout e 3ACK duplicati sono trattati allo stesso modo.

Diagramma a stati di TCP Tahoe:

![[Pasted image 20231110121841.png]]