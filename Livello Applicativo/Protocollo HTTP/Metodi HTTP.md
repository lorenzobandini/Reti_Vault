Operazione che il client richiede venga effettuata sulla risorsa identificata dalla Request - [[URI|URI]].

I vari metodi sono:
- "[[OPTIONS]]"
- "[[GET]]"
- "[[HEAD]]"
- "[[POST]]"
- "[[PUT]]"
- "[[DELETE]]"
- "[[TRACE]]"

Di cui PUT e DELETE normalmente non abilitati sui server web pubblici.
Invece, la differenza tra POST e PUT è che con POST solitamente si usa per creare risorse mentre con PUT abbiamo anche la possibilità di creare ma anche modificare con facilità le risorse. Inoltre la differenza principale sta nel fatto che con POST facciamo una richiesta ad un nodo padre e dipenderà dall'implementazione del [[Server]] come verrà trattato mentre con la PUT si crea/modifica una risorsa di cui passiamo l'[[URI]] specifico.

Classifichiamo anche i metodi come
- Metodi Sicuri: cioè che non hanno effetti collaterali come modificare una risorsa e sono GET, HEAD, OPTIONS, TRACE
- Metodi [[Idempotenza|Idempotenti]]: cioè se n richieste identiche hanno lo stesso effetto di una singola richiesta e sono GET, HEAD, PUT, DELETE, OPTIONS, TRACE