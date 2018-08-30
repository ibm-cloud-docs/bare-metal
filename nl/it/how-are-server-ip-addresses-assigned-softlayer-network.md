---

copyright:
  years: 1994, 2018
lastupdated: "2018-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Assegnazione di indirizzi IP dei server

{{site.data.keyword.cloud}} configura i server con un indirizzo IPv4 sulla
rete privata, un indirizzo IPv4 per un accesso di gestione di basso livello sulla rete privata
e, se richiesto, un indirizzo IPv4 pubblico.
Se richiesto, è disponibile un indirizzo IPv6 sulla rete pubblica. A tutti questi indirizzi IP si fa riferimento collettivamente come **Indirizzi IP primari**.

È possibile eseguire il bind di ulteriori indirizzi IP ai server dopo che hai acquistato **Sottoreti secondarie** tramite il [Portale clienti ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com). Gli indirizzi IP da te acquistati tramite il portale clienti e da te gestiti sono detti **Indirizzi IP secondari**.

Per ulteriori informazioni sull'acquisizione di indirizzi IP, consulta [Sottoreti e IP](https://console.bluemix.net/docs/infrastructure/subnets/).


# Bind di indirizzi IP secondari

Dopo che hai acquistato una sottorete secondaria, devi configurare il sistema operativo per utilizzare uno o più indirizzi IP, Ogni sistema operativo configura gli indirizzi IP in modo differente, ma si fa di norma riferimento a tale operazione come alla configurazione di "alias dell'interfaccia". 
