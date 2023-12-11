Il flusso di dati punto-punto viene suddiviso in pacchetti che condividono le risorse di rete.
La [[commutazione]] del pacchetto poi continua con una trasmissione store and forward nella quale il commutatore deve ricevere l'intero pacchetto prima di poter cominciare a tramettere il primo bit del pacchetto sul collegamento in uscita creando un primo ritardo.

![[Schermata 2023-12-10 alle 20.26.11.png]]

Quando poi i pacchetti sono stati processati e indirizzati, vengono inseriti in una coda buffer di output creando altri ritardi in coda.
Date poi le dimensioni finite del buffer è possibile la perdita di pacchetti.

In questo tipo di comunicazione non c'è un canale dedicato ma gli [[host]] comunicano scambiandosi pacchetti su collegamenti condivisi tra gli utenti ma con il rischio di congestione causati dall'accodamento dei pacchetti in attesa per l'utilizzo del collegamento.

Per un confronto con le [[Reti a commutazione di circuito]]: [[Circuit-Switching vs Packet-Switching]]