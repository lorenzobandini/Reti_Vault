 L'IPv6 rappresenta una tappa fondamentale nell'evoluzione del protocollo Internet, rispondendo alle crescenti esigenze di connettività globale. La sua adozione è stata motivata principalmente dalla limitata disponibilità di indirizzi IPv4, che ha reso necessaria una soluzione più scalabile e flessibile per sostenere l'espansione continua della rete. 

I motivi di passaggio da IPv4 a IPv6 e le soluzioni sono:
- Esaurimento indirizzi a 32 bit e quindi indirizzi a 128 bit
- Velocizzare l'elaborazione e forwarding dei pacchetti inserendo la lunghezza fissa di 40byte nell'header e eliminando il checksum
- Risparmiare ai router il costo di frammentazione implementando ICMPv6 con messaggio "packet too big" così che sia la sorgente a preoccuparsi della frammentazione
- Facilitare il QoS introducendo il "flow label" per identificare datagrammi appartenenti allo stesso "flow"

Gli indirizzi IPv6 sono formati da 128 bit, una significativa espansione rispetto agli indirizzi IPv4 a 32 bit. Questa ampia capacità di indirizzamento fornisce praticamente un numero illimitato di indirizzi unici, risolvendo la crescente scarsità di IPv4 e aprendo la strada a una connettività su scala globale senza precedenti. 

La struttura degli indirizzi IPv6 è espressa in notazione esadecimale e suddivisa in otto blocchi, ognuno composto da quattro caratteri esadecimali. La possibilità di abbreviare gli indirizzi semplifica la rappresentazione, migliorando la leggibilità. 


![[Pasted image 20231201141834.png]]

Per supportare sia IPv4 e IPv6 si implementa il Dual Stack che funge da tramite.

![[Pasted image 20231201142257.png]]

Per connettere un network IPv4 a dei router IPv6 si effettua incapsulamento e tunnelling:
- L'incapsulamento è un processo mediante il quale un pacchetto di dati viene avvolto in un altro pacchetto prima di essere trasmesso attraverso una rete. Nel caso in cui dati IPv6 devono attraversare una rete che supporta solo IPv4, il pacchetto IPv6 viene incapsulato all'interno di un pacchetto IPv4 e il pacchetto IPv6 diventa il carico utile (payload) del pacchetto IPv4.
- Il tunneling è una tecnica che consente di instradare il traffico di una rete attraverso un'altra rete.