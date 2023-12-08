Tipo di attacco denial-of-service in cui un fran numero di pacchetti [[UDP]] viene inviato a un [[server]] obiettivo e [[porta]] destinazione scelta in modo random. Attacco volumetrico con l'obiettivo di sovraccaricare la capacità del dispositivo di elaborare e rispondere poiché:
- Il server prima controlla se sono in esecuzione programmi che sono attualmente in attesa di richiesta sulla porta specificata
- Come risultato dell'utilizzo delle risorse da parte del server di destinazione per controllare e quindi rispondere ad ogni pacchetto UDP ricevuto, le risorse possono esaurirsi rapidamente, con conseguente denial-of-service al traffico normale
- Se nessun programma riceve pacchetti su quella porta, il server risponde con un pacchetto [[ICMP]] per informare il mittente che la destinazione non è raggiungibile

L'attaccante solitamente inserisce nel pacchetto del messaggio UDP un [[indirizzo IP]] spoofed

![[Pasted image 20231110175800.png]]