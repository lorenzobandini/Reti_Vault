Servono per scomporre sistemi complessi in una serie di passi e rendere l'implementazione [[efficace]] ed [[efficiente]].
Ad ogni passo viene eseguito un particolare compito su un messaggio, che viene integrato e trasferito ad un altro agente, seguendo specifiche regole di esecuzione.

I motivi per cui stratifichiamo sono:
- Mantenere la struttura esplicita che permetta di identificare facilmente le relazioni tra gli elementi di un sistema complesso
- Facilità di manutenzione e aggiornamento del sistema poiché ogni modulo/livello/strato svolge un insieme limitato di compiti e nel sistema appare solo come un black box che riceve input dal livello inferiore e restituisce output a quello superiore attraverso un [[Interfaccia]]
- Ogni cambiamento dell'implementazione è trasparente per il resto del sistema

Principi base di come stratificare sono:
- [[Separation of Concern]]
- [[Information Hiding]]

Ogni livello logico di astrazione è realizzato in un apposito strato e ne viene creato uno nuovo quando si rende necessario un diverso grado di astrazione. 

Prima si usavano dei [[Sistemi Chiusi]], poi l'[[International Organization for Standards (ISO)]]ha introdotto i [[Sistemi Aperti]] con l'[[Open System Interconnector (OSI)]] creando il [[Modello ISO-OSI]]

Dalla controparte abbiamo [[Stack Protocollare TCP-IP]] con cui possiamo fare un confronto [[ISO-OSI vs TCP-IP]]
