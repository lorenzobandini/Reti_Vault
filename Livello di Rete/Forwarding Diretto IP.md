Nell'inoltro diretto, il pacchetto IP ha come destinazione un host nella propria rete IP e l'invio è diretto sul destinatario, l'indirizzo di destinazione a livello link è quello del destinatario e non viene interpellata nessun'altra entità.

Esempio di inoltro in 4 fasi:
1. L'entità IP di B deve spedire un pacchetto all'indirizzo IP-A
2. B conosce l'indirizzo IP-B della propria interfaccia e dal confronto con IP-A capisce che A si trova nella stessa rete
3. B consulta la tabella di corrispondenza tra indirizzi IP e indirizzi di rete (indirizzi MAC nel caso di rete locale) per reperire l'indirizzo MAC-A
4. L'entità IP di B passa il pacchetto al livello inferiore che crea un pacchetto con destinazione MAC-A

![[Pasted image 20231124172824.png]]