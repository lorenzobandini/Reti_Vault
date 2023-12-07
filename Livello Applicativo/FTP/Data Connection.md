Connessione su cui i dato sono trasferiti con modi e tipi specificati. I dati trasferiti possono essere parte di un file, un file o un set di file.

Quando il server riceve un comando per trasferire un file (da o verso il client) sulla connessione di controllo, vengono svolte le seguenti azioni:
1. Il server apre una connessione dati [[TCP]] con il client (Active Mode)
2. Trasferisce il file sulla connessione dati
3. Dopo il trasferimento di un file, il server chiude la connessione

La connessione dati è una [[Connessione non persistente]], ce n'è una per ciascun trasferimento.
