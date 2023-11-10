L'idea è cercare di incrementare la finestra molto velocemente all'inizio e diminuire la crescita man mano che ci si avvicina al la massima congestione tollerata.

$W_{max}$ è il rate di invio quando è stata rilevata congestione. Dopo aver dimezzato la finestra in seguito ad un evento di perdita, prima incremento più velocemente verso $W_{max}$, ma poi rallento avvicinandomi a $W_{max}$

![[Pasted image 20231110142413.png]]

L'aumento di $W$ avviene come una funzione del cubo della distanza tra l'istanza del tempo attuale k