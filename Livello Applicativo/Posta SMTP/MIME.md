Acronimo di Multipurpose Internet Mail Extension, ha come idea di base continuare ad usare il formato di messaggio già specificato nel [[Protocollo SMTP]] ma aggiungendo una struttura al message body e definendo regole di codifica per il trasferimento di testo non-ASCII continuando però ad usare gli stessi protocolli e [[mail server]] esistenti, modificando solo gli User Agents.

![[Pasted image 20231015143237.png]]

Questo nuovo standard che estende il formato di e-mail, permette di supportare:
- testo in set di caratteri diversi da US-ASCII
- allegati in formato non testuale
- corpo del messaggio con più parti
- header in set di carattere non-ASCII

Definisce un insieme di metodi per rappresentare dati binari in formato ASCII e aggiunge linee di intestazione per dichiarare il tipo di contenuti MIME

![[Pasted image 20231015143212.png]]

MIME fornisce vari schemi di transfer encoding, tra cui:
- ASCII encoding of binary data: base 64 encoding: gruppi di 24 bit divisi in 4 unità da 6 bit e ciascuna unità viene inviata come un carattere ASCII
- Quoted-Printable encoding: per messaggi testuali con pochi caratteri non-ASCII, più [[efficiente]].

I tipi MIME specificano la natura dei dati nel corpo di un'entità MIME e sono (a fianco alcuni loro sottotipi):
- Text: plain, html
- Video: mpeg
- Image: jpeg, gif
- Audio: basic, 32kadpcm
- Application: msword, octet-stream