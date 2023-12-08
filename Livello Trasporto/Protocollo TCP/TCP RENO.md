TCP Reno è un algoritmo di controllo della congestione all'interno del [[protocollo]] [[TCP]], ed è una delle varianti più comunemente utilizzate. Inizialmente viene definita una variabile "soglia" alla quale è assegnato un valore alto. La soglia determina quanto termina la partenza lenta ed inizia la fase di congestion avoidance:
- Se $cwnd \lt soglia$: _cwnd_ aumenta esponenzialmente
- Se $cwnd \gt soglia$: _cwnd_ aumenta linearmente

In caso di evento di perdita:
- Se ho 3 _ACK_ duplicati pongo la prima soglia a metà di _cwnd_ e poi $cwnd = soglia + 3 MSS$ (fast recovery)
- Se ho un _ACK_ perso per **timeout** pongo la soglia a metà di _cwnd_ e pongo $cwnd = 1 MSS$ (slow start)

Nella fase di recovery:
- Se avviene un timeout si va in slow start
- Finché continuano ad arrivare _ACK_ duplicati $cwnd=cwnd+1$
- Se arriva un nuovo _ACK_ non duplicato si va in congestion avoidance e $cwnd=soglia$

Il diagramma a stati di TCP RENO è:

![[Screenshot 2023-11-10 121321.png]]