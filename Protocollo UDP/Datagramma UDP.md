Un datagramma UDP, User Datagram Protocol, è un formato di pacchetto dati usato per le comunicazioni su una rete.

Il datagramma UDP ha una struttura semplice. È composto dall'header di 8 byte che contiene:
- Source port \[16 bit]: identifica il numero di porta sull'host del mittente del datagramma.
- Destination port \[16 bit]: identifica il numero di porta sull'host del destinatario del datagramma.
- Length \[16 bit]: contiene la lunghezza totale in bytes del datagramma UDP (header + dati).
- Checksum \[16 bit] (opzionale): contiene il codice di controllo del datagramma (header + dati + pseudo-header, quest'ultimo comprendente gli indirizzi IP di sorgente e destinazione). 

e da un Payload che contiene il messaggio.

![[Pasted image 20231110174201.png]]

In particolare, il checksum, opzionale in UDP, effettua un controllo errore end-to-end e se il pacchetto è corrotto viene scartato senza notificare il mittente.
Calcolato sull'intero datagramma UDP più lo pseudo-header cioè la parte dell'header IP.

![[Pasted image 20231110152525.png]]

Per il calcolo del checksum lo vediamo da due punti di vista:
- Mittente: il campo checksum è a 0, tratta il contenuto del datagramma UDP come una sequenza di parole da 16 bit in complemento a uno e somma i singoli bit con eventuali riporti. Infine inverte i bit e lo assegna al campo checksum.
- Ricevente: calcola la checksum del segmento ricevuto includendo anche il campo checksum e se il valore della checksum è 0 il messaggio non ha errori, altrimenti sì e viene scartato