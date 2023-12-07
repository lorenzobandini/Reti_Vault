Più brevemente ECN, è un approccio per gestire la congestione completamente diverso nel quale sono i router a comunicare ai mittenti le congestioni in rete.
Per implementare questo meccanismo ci servono degli header nei campi delle intestazione di livello trasporto.
In particolare, i router, lavorano su due bit che indicano, il primo se supporta la tecnologia ECN mentre il secondo è settato ad 1 se ha problemi di congestione così da evitare di notificare quel router inutilmente.
La sorgente reagiste all'evento dimezzando la finestra di emissione.

![[Pasted image 20231110184331.png]]