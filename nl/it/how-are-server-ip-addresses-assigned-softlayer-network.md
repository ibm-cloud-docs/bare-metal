---

copyright:
  years: 1994, 2019
lastupdated: "2019-06-17"

keywords: server IP addresses, bare metal, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Assegnazione e bind di indirizzi IP
{: #bm-assigning-and-binding-ip-addresses
Utilizza le seguenti informazioni per assegnare un indirizzo IP al tuo server e per eseguire il bind di un indirizzo IP secondario al server laddove necessario.
{: shortdesc}

## Assegnazione di indirizzi IP dei server
{: #bm-assign-ip-address}

{{site.data.keyword.cloud}} configura i server con questi indirizzi:
un indirizzo IPv4 sulla rete privata,
un indirizzo IPv4 per un accesso di gestione di basso livello sulla
rete privata e,
se richiesto, un indirizzo IPv4 pubblico.

Se richiesto, è disponibile un indirizzo IPv6 sulla rete pubblica. Tutti questi
indirizzi IP vengono denominati collettivamente **Indirizzi IP primari**.

È possibile eseguire il bind di ulteriori indirizzi IP ai server dopo aver acquistato **Sottoreti
secondarie** tramite la [console {{site.data.keyword.cloud_notm}}](https://cloud.ibm.com){: external}. Gli indirizzi IP da te acquistati tramite il portale clienti
e da te gestiti sono detti **Indirizzi IP secondari**.

Per ulteriori informazioni sull'acquisizione di indirizzi IP, vedi [Sottoreti e IP](https://cloud.ibm.com/docs/infrastructure/subnets/){: external}.


## Bind di indirizzi IP secondari
{: #bm-bind-secondary-ip-address}

Dopo aver acquistato una sottorete secondaria, devi configurare il sistema operativo per utilizzare uno o più indirizzi IP. Ogni sistema operativo configura gli indirizzi IP in modo diverso, ma in genere tale operazione viene definita come configurazione di "alias dell'interfaccia".
