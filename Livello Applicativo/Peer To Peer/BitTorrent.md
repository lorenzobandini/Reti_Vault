Protocollo molto diffuso per la distribuzione di file in [[Internet]], in particolare un _torrent_ è un processo collaborativo di condivisione di un file.
L'idea di base è dividere un file in pezzi (_chunk_) di 256Kb e far ridistribuire ad ogni peer i dati ricevuti, fornendoli a nuovi destinatari in modo da:
- Ridurre il carico ad ogni sorgente
- Ridurre la dipendenza dal distributore originare
- Fornire ridondanza

L'insieme di peer che partecipano ad un torrent scambiandosi parti di file si chiama _swarm_ dove ogni peer allo stesso tempo preleva e trasmette più chunk.
Per coordinare la distribuzione del file si usa un nodo chiamato _tracker_ che tiene traccia dei peer che stanno partecipando al torrent. Per condividere un file, un peer crea un file `.torrent` che contiene metadati sul file condiviso e sul tracker.

Un nuovo peer cerca quello che vuole con il motore di ricerca e ottiene il file `.torrent` ovvero un metafile con info sui chunk e indirizzo IP di tracker e contatta il tracker ricevendo indirizzi di alcuni peer dello swarm.
Un peer quando entra a far parte di un torrent per la prima volta, non ha chunk dei file. Col passare del tempo accumula sempre più parti che, mentre scarica, invia agli altri peer. Una volta che un peer ha acquisito l'intero file, può egoisticamente lasciare il torrent o altruisticamente rimanere nel torrent e continuare a inviare chunk agli altri peer.

![[Schermata 2024-01-06 alle 17.25.32.png]]

Le strategie principali di BitTorrent sono:
- "Rarest Chunk First": prioritizza il download dei chunk di file meno diffusi tra i peer, promuovendo una distribuzione equilibrata e efficiente delle parti del file nella rete.
- "Tit for tat": inviare dati ai peer che inviano dati scegliendo quelli che stanno inviando dati a frequenza maggiore.