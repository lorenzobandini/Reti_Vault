Consiste nell'invio da parte del [[Client]] di molteplici richieste senza aspettare la ricezione di ciascuna risposta.
Il [[Server]] deve inviare le risposte nello stesso ordine in cui sono state ricevute le richieste e se una richiesta richiede tempo per essere processata, le risposte alle richieste successive sono bloccate: questa problematica si chiama Head of Line Blocking (HOLB).
Il client non può inviare in pipeline richieste che usano metodi [[HTTP]] non [[Idempotenza|Idempotenti]].

![[Pasted image 20231004120812.png]]