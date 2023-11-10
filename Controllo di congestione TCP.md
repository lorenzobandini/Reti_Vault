Il fenomeno della congestione è originato dal tentativo della/e sorgente/i di richiedere più banda di quella disponibile sul percorso. Troppe sorgenti che tramettono troppi dati a una velocità elevata per cui la rete non può gestirli.

Il traffico eccessivo della rete può provocare **lunghi ritardi** dovuti all'accodamenti nei buffer dei router e la **perdita di pacchetti** per l'overflow nei buffer dei router.

Nel meccanismo base del controllo della congestione, i dispositivi stessi monitorano e gestiscono la congestione senza l'assistenza attiva della rete. Questo funziona perché il meccanismo impone a ciascun mittente di limitare la frequenza di invio di pacchetti sulla connessione, in funzione della congestione percepita adattandosi così alla velocità di rete.

Per chiarire meglio possiamo fare un paragone con il riempimento di un secchio:

![[Pasted image 20231110111601.png]]

Per il controllo della congestione, il mittente TCP deve regolare la propria frequenza di invio in funzione alla congestione rilevata. Il processo è costituito da 4 passi:
1. **Slow Start**: All'inizio della connessione, la finestra di congestione (_cwnd_) inizia con un valore minimo e viene gradualmente aumentata, raddoppiandosi ad ogni RTT (_AIMD_), consentendo un rapido aumento della velocità di trasmissione.
2. **Congestion Avoidance**: Quando la _cwnd_ raggiunge una soglia (dipende dall'implementazione specifica), TCP passa dalla modalità di Slow Start alla modalità di Congestion Avoidance. In questa fase, la finestra di congestione aumenta gradualmente di 1 segmento per ogni round-trip time.
3. **Fast Recovery**: Durante questa fase, TCP invia pacchetti aggiuntivi per riempire la pipeline, ma con una finestra di congestione ridotta. In seguito, ritorna alla modalità di Congestion Avoidance.
4. **Reazione ai time-out**: Quando avviene un time-out, indica che un pacchetto non è stato confermato entro un tempo specifico. In risposta, TCP esegue una ritrasmissione del pacchetto persosi e riduce drasticamente la finestra di congestione a un valore minimo, comportandosi come se fosse nella fase iniziale di Slow Start. Questo serve a evitare ulteriori congestioni a causa di problemi nella rete.

La finestra di congestione (_cwnd_) impone un vincola alla frequenza di immissione del traffico sulla rete in base alla congestione percepita. Solitamente la frequenza di invio dati non super $cwnd/RTT$

La finestra di congestion (_cwnd_) si misura tipicamente in $MSS$ dove 1 $MSS$ è la quantità massima di dati trasportabili da un segmento determinato da:
-
