Il flusso di dati punto-punto viene suddiviso in pacchetti che condividono le risorse di rete.
La [[commutazione]] del pacchetto poi continua con una trasmissione store and forward nella quale lo [[Switch]] deve ricevere l'intero pacchetto prima di poter cominciare a tramettere il primo bit del pacchetto sul collegamento in uscita creando un primo ritardo.
Quando poi i pacchetti sono stati processati e indirizzati, vengono inseriti in una coda buffer di output creando altri ritardi in coda.
Date poi le dimensioni finite del buffer è possibile la perdita di pacchetti.

In questo tipo di comunicazione non c'è un canale dedicato ma gli host comunicano scambiandosi pacchetti su collegamenti condivisi tra gli utenti ma con il rischio di congestione causati dall'accodamento dei pacchetti in attesa per l'utilizzo del collegamento.

Per un confronto con le [[Reti a commutazione di circuito]]: [[Circuit-Switching vs Packet-Switching]]