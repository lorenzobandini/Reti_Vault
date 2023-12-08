Un Datagramma IP è una struttura di dati che rappresenta un pacchetto di informazioni inviato attraverso una rete IP. I datagrammi IP contengono tutte le informazioni necessarie per instradare e consegnare i dati dalla sorgente alla destinazione attraverso una rete di computer.

Hanno la struttura:
![[Pasted image 20231122122843.png]]

In particolare:
![[Pasted image 20231122122909.png]]

I campi sono:
- **Versione (4 bit)**: specifica la versione di IP usata (attualmente IPv4 o IPv6)
- **Hlen (lunghezza dell'header, 4 bit)**: lunghezza dell'intestazione espressa in parole da 32 bit. Tipicamente vale 0101 ovvero 20 Byte.
- **Tipo di servizio (8 bit)**: serve per decorare il datagramma con vari tipi di servizi:
	- 6 bit per Differentiated Services: I pacchetti vengono marcati in base alla classe di servizio (telefonata, controllo, multimedia ...) e trattati con differenti politiche di accodamento ai router
	- 2 bit di [[Explicit Congestion Notification]]: supporto a livello di rete e trasporto per la notifica di eventi di congestione.
- **Lunghezza del datagramma (16 bit)**: è la lunghezza di tutto il datagramma in byte, header incluso. (Dim. MAX = 65535)
- **Identificatore, flag, offset (32 bit)**: sono campi per la [[frammentazione]]
- **Tempo di vita (8 bit)**: ad ogni passaggio da router viene decrementato, quando raggiunge lo zero viene scartato. Assicura che eventuali percorsi ad anello non provochino traffico perpetuo nella rete
- **Protocollo di trasporto(8 bit)**: in ricezione all'[[host]] destinatario indica quale protocollo dello strato superiore deve ricevere i dati.
- **Checksum dell'intestazione (16 bit)**: viene calcolato il checksum della sola intestazione ad ogni router. Se si ottiene un errore si scarta il datagramma.
- **Indirizzi sorgente (32 bit)**: indirizzo IP del mittente
- **Indirizzo destinazione (32 bit)**: indirizzo IP del destinatario
- **Opzioni (Lunghezza variabile, multiplo di 32 bit)**: uso sporadico, da 0 a 40 byte
- **Dati**: dati trasportati dal datagramma IP
