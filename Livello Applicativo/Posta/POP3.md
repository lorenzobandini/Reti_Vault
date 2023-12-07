Lo User Agent apre una connessione [[TCP]] verso il server di posta.
Il processo è diviso in tre fasi:
- Autorizzazione
- Transizione
- Aggiornamento

In **Autorizzazione** il cliente usa i comandi 
- `user`: specifica la username
- `pass`: specifica la password
e il server risponde:
- `OK`
- `ERR`

In **Transizione** o fase di scambio i comandi del client sono:
- `list`: visualizza la lista dei messaggi
- `retr`: preleva il messaggio per numero
- `dele`: elimina il messaggio dal server
- `quit`: chiude la sessione

In **Aggiornamento** dopo `quit` il server cancella i messaggi marcati per la rimozione
