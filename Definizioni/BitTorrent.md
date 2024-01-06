Protocollo molto diffuso per la distribuzione di file in [[Internet]], in particolare un _torrent_ è un processo collaborativo di condivisione di un file.
L'idea di base è dividere un file in pazzi (_chunk_) e far ridistribuire ad ogni peer i dati ricevuti, fornendoli a nuovi destinatari in modo da:
- Ridurre il carico ad ogni sorgente
- Ridurre la dipendenza dal distributore originare
- Fornire ridondanza

L'insieme di peer che partecipano ad un torrent scambiandosi parti di file si chiama _swarm_ dove ogni peer allo stesso tempo preleva e trasmette più chunk.
Per coordinare la distribuzione del file si usa un nodo chiamato _tracker_ che tiene traccia dei peer che stanno partecipando al torrent. Per condividere un file, un peer crea un file `.torrent` che contiene metadati sul file condiviso e sul tracker come .

![[Schermata 2024-01-06 alle 17.25.32.png]]