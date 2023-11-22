![[Pasted image 20231122122843.png]]


![[Pasted image 20231122122909.png]]

I campi sono:
- Versione (4 bit): specifica la versione di IP usata (attualmente IPv4 o IPv6)
- Hlen (lunghezza dell'header, 4 bit): lunghezza dell'intestazione espressa in parole da 32 bit. Tipicamente vale 0101 ovvero 20 Byte.
- Tipo di servizio (8 bit): serve per decorare il datagramma con vari tipi di servizi:
	- 6 bit per Differentiated Services: I pacchetti vengono marcati in base alla classe di servizio (telefonata, controllo, multimedia ...) e trattati con differenti politiche di accodamento ai router
	- 2 bit di [[Explicit Congestion Notification]]: supporto a livello di rete e trasporto per la notifica di eventi di congestione.
- Lunghezza del datagramma (16 bit)
...

[[Frammentazione]]