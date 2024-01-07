Acronimo di Security Associations, garantiscono la sicurezza delle comunicazioni su reti IP fornendo un modo per associare univocamente le politiche di sicurezza e i parametri di sicurezza a una coppia specifica di host o reti che comunicano tra loro.

Una SA viene stabilita prima dell'invio dei dati tra un'entità di invio e una di ricezione in maniera unidirezionale.
Ogni volta che il router mittente deve costruire un datagramma IPsec da inoltrare su questa SA, accede alle informazioni di stato della SA per determinare come autenticare e decifrare il datagramma.
Il router destinatario conserverà le stesse informazioni di stato per questa SA e le utilizzerà per autenticare e decrittografare qualsiasi datagramma IPsec in arrivo dal router mittente.

![[Schermata 2024-01-07 alle 21.23.19.png]]

Gli attributi di una SA sono:
- Identificatore di 32 bit per l'indice parametro di sicurezza (SPI)
- Interfaccia SA di origine
- Interfaccia SA di destinazione
- Tipo di crittografia usata
- Chiave crittografica
- Tipo di verifica di integrità
- Chiave di autenticazione