Acronimo di **S**imple **M**ail **T**ransfer **P**rotocol, è un [[Protocollo]] di tipo **"push"** che ha come obiettivo il trasferimento affidabile ed efficiente di [[Posta Elettronica]] con l'utilizzo di intermediari.
SMTP è indipendente dal sistema di trasmissione usato e richiede solo il trasferimento di stream di byte ordinato e affidabile.
Una caratteristica di SMTP è la capacità di trasportare mail attraverso più reti. Un messaggio di mail può passare attraverso server intermedi nel percorso da mittente a destinatario finale

Quando un client SMTP vuole trasferire un messaggio, stabilisce un canale di trasmissione bidirezionale con un server SMTP. La responsabilità di un [[Client]] è di trasferire la mail a un server SMTP, o comunicare un eventuale insuccesso (scambio formale di responsabilità).
Un client SMTP determina l’indirizzo di un host appropriato che ospita un server SMTP risolvendo il nome della destinazione in un indirizzo del mail server destinazione.
La risoluzione di nome in indirizzo IP del mail server destinatario avviene attraverso il DNS.

![[Pasted image 20231015135251.png]]

I possibili problemi per gli scambi di messaggio possono essere:
- Connessione con il mail server del mittente (server inesistente o irraggiungibile)
- Connessione con il mail server destinatario (server inesistente o irraggiungibile)
- Inserimento in mailbox destinatario (user unknown, mailbox full) e in questi casi il mittente riceve una notifica

Gli unici casi in cui il destinatario non riceve il messaggio e se qualcun altro agente esterno, come ad esempio un filtro anti-spam, rimuove il messaggio. 
Lo scambio di messaggi segue il [[Protocollo SMTP]].

Gli User Agent per accedere alla posta utilizzano [[POP3]].

Un'alternativa è IMAP che ha più feature ma è anche più complesso.


