L'idea è cercare di incrementare la finestra molto velocemente all'inizio e diminuire la crescita man mano che ci si avvicina al la massima congestione tollerata.

$W_{max}$ è il rate di invio quando è stata rilevata congestione. Dopo aver dimezzato la finestra in seguito ad un evento di perdita, prima incremento più velocemente verso $W_{max}$, ma poi rallento avvicinandomi a $W_{max}$

![[Pasted image 20231110142413.png]]

La caratteristica principale di TCP CUBIC è la sua capacità di regolare dinamicamente la finestra di congestione. Invece di aumentare linearmente, come fanno altri algoritmi, la finestra di congestione di CUBIC aumenta in modo più graduale seguendo una funzione cubica, consentendo una crescita più fluida del throughput in reti ad alta capacità.

Fissando $K$ il punto nel tempo in cui $cwnd$ raggiungerà $W_{max}$, aumento di $W$ come una funzione del cubo della distanza tra l'istante di tempo attuale e $K$ avendo così incrementi maggiori quando siamo lontani da $K$ e incrementi più cauti quando siamo vicini a $K$

![[Pasted image 20231110184119.png]]