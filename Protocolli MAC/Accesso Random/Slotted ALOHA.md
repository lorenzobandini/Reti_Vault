Viene suddiviso il tempo in slot uguali e fissi. I nodi iniziano a tramettere all'inizio dello slot non sincronizzati tra loro e se 2 o più nodi tramettono, ogni nodo rileva la collisione.
Se un nodo non rileva collisioni, il nodo può inviare un nuovo frame nello slot successivo mentre se rileva una collisione il nodo ritrasmette con probabilità $p$ il frame nello slot successivo finché non ha successo.

I pro sono:
- Il singolo nodo attivo può trasmettere alla massima velocità consentita dal canale
- Fortemente decentralizzato dato che solo gli slot sono sincronizzati
- Semplice

I contro sono:
- Molte collisioni
- Spreco di slot

![[Pasted image 20231201151551.png]]