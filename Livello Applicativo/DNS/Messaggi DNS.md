Pacchetti di dati che vengono scambiati utilizzando [[UDP]] sulla [[porta]] 53 tra i [[client]] [[DNS]] e i [[server]] DNS per la risoluzione dei nomi di [[dominio]] (è permesso anche l'uso di [[TCP]] per messaggi di grandi dimensioni e trasferimenti tra server DNS).
Possono essere messaggi di query o di reply e mantengono lo stesso formato.
Ha un header in cui sono contenuti:
- identification: 16 bit di identificazione per una query e per la reply ad una query con lo stesso identificatore
- flags: per identificare query (0) e reply (1) 

Nel resto del messaggio ci sono campi per:
- Domande: campi per il nome richiesto e il tipo di query
- Risposte: [[Record DNS]] nella risposta alla domanda
- Competenza: record relativi ai server di competenza
- Informazioni aggiuntive

![[Pasted image 20231018185840.png]]

Le risposte contengono:
- Zero o più [[Record DNS]] nella sezione "Risposte"
- Zero o più [[Record DNS]] nella sezione "Informazioni aggiuntive"