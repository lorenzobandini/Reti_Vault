Acronimo di _Additive Increase Multiplicative Decrease_ è l'aumento della finestra di congestione del mittente proporzionalmente ad ogni _ACK_ ricevuto. Ad ogni _ACK_ la finestra di congestione viene incrementata in modo che si abbia una crescita pari ad 1 _MSS_ per ogni _RTT_
Ad ogni evento di perdita, la finestra di congestione del mittente dimezza.

L'algoritmo di controllo della congestione _AIMD_ crea quindi un grafico del genere:

![[Pasted image 20231110113732.png]]

Per un miglior controllo di congestione sulla rete possiamo utilizzare il più recente algoritmo [[TCP RENO]] o il suo predecessore [[TCP Tahoe]]