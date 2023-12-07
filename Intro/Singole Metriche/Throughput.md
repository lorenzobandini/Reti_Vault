Quantità di dati che possono essere trasmessi con successo dalla sorgente alla destinazione in un certo intervallo di tempo.
Throughput e [[Bitrate]] non sono la stessa; il throughput indica la velocità con cui traferiamo effettivamente i dati, al netto delle perdite sulla rete, duplicazioni, protocolli, ecc...

Throughput < [[Velocità di trasmissione]]

Dipende dalla velocità di trasmissione del collegamento, dalla quantità di dati, gli effetti dei protocolli, etc...

In un percorso da una sorgente a una destinazione un pacchetto può passare attraverso numerosi link, ognuno con throughput diverso. Il throughput dell'intero percorso si calcola con:

$$ EndToEndThroughout = min(R_s,R_c)$$
dove $R_s$ e $R_c$ sono due link diversi in cui passa il pacchetto