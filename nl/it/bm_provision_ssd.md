---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-02"

keywords: provision Intel Optane compatible bare metal server, Intel Optane, optane 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning di un server bare metal compatibile con Intel Optane
{: #bm-provision-optane-server}

Per eseguire il provisioning di un server bare metal con un'unità Intel Optane:
1. Utilizza la procedura: [Creazione di un server bare metal personalizzato](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server).
* Seleziona le seguenti opzioni sul modulo d'ordine:

|Sezione|Opzione da selezionare
|------|------|
|Regione-Data center|Per utilizzare l'unità Intel Optane, seleziona uno dei seguenti data center:<br>Europa - AMS03, FRA02, LON02, OSL01<br>Nord America meridionale DAL09, DAL10, DAL12<br>Asia-Pacifico - MEL01<br>Nord America orientale - MON01, TOR01, WDC04<br>Nord America occidentale - SJC03<br>|
|Server|1. Seleziona **All servers**<br>2. Seleziona *Dual Processors*<br>3. Seleziona uno dei seguenti server<br>-Intel Xeon 4110, fino a 12 unità<br>-Intel Xeon 5120, fino a 12 unità<br>-Intel Xeon 6140, fino a 12 unità<br>-Intel Xeon E5-2620 v4 con supporto GPU<br>-Intel Xeon E5-2650 v4 con supporto GPU<br>-Intel Xeon E5-2690 v4 con supporto GPU<br><br>  **Nota**: se selezioni E5-2620 v4, E5-2650 v4 o E5-2650 v4, l'unità Intel Optane sostituisce la tua GPU, per cui non puoi avere sia la GPU che un'unità Intel Optane.|
|Sistema operativo|Per unità Optane fornite da Intel, i seguenti sistemi operativi sono certificati da Intel:<br>Windows Server 2016 (tutte le edizioni)<br>Windows Server 2012 R2 (tutte le edizioni)<br><br>Per le unità incluse, open source e non Intel, la compatibilità e la funzionalità sono verificate ma non certificate:<br>Red Hat Enterprise Linux 7.x (64 bit)<br>Red Hat Enterprise Linux 6.x (64 bit).
|Componenti aggiuntivi immagine| Seleziona un'unità Intel Optane per il primo e il secondo componente PCIe o per entrambi.|
