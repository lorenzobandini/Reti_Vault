Nell'inoltro indiretto, il pacchetto IP ha come destinazione un [[host]] di un'altra rete IP, viene delegato l'invio al router e l'indirizzo di destinazione a livello link è quello del router.

Esempio di inoltro in 5 fasi:
1. L'entità IP di B deve spedire un pacchetto all'indirizzo IP-D=131.17.23.4
2. B conosce l'indirizzo IP-B della propria interfaccia e dal confronto con IP-D capisce che D non si trova nella stessa rete
3. B deve dunque inoltrare il pacchetto ad un router (di solito è configurato un solo default router)
4. B recupera l'indirizzo MAC nella tabella di corrispondenza e passa il pacchetto al livello inferiore
5. Il pacchetto viene costruito e spedito sull'interfaccia


![[Screenshot 2023-11-24 173051.png]]