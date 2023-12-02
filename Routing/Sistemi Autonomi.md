Chiamati anche AS, sono gruppi di router sotto lo stesso controllo amministrativo . Gli AS decidono autonomamente i protocolli e le politiche di routing che intendono adottare al loro interno.
I protocolli di routing all'interno di un AS sono detti Interior Gateway Protocol (IGP) e i protocolli di routing fra AS sono detti Exterior Gateway Protector (EGP).
Quindi all'interno di un sistema autonomo:
- I router sono sotto lo stesso controllo amministrativo
- Usano lo stesso protocollo di routing intra-AS

[[Internet]] è partizionata in sistemi autonomi, in particolare dei tipi:
- AS stub: collegato a un solo AS
- AS multihomed: collegato a più di un altro AS
- AS di transito

INTRA-AS routing protocol determina rotte per le destinazioni interne ad AS grazie a Routing Information Protocol ([[RIP]]) e Open Shortest Path First ([[OSPF]])

INTRA-AS e INTER-AS routing protocol determinano insieme rotte per le destinazioni esterne all'AS con l'aiuto del Border Gateway Protocol ([[BGP]]) che consente di conoscere le destinazioni raggiungibili attraverso sistemi autonomi vicini, propaga le informazioni di raggiungibilità ai router interni del proprio AS e determina percorsi buoni verso le sottoreti di destinazione.

I sistemi autonomi sono interconnessi se ciascun sistema autonomo sa come inoltrare pacchetti lungo il percorso ottimo verso qualsiasi destinazione interna al gruppo.