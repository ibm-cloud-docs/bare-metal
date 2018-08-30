---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning di un server bare metal compatibile con Intel Optane
Per eseguire il provisioning di un server bare metal con un'unità Intel Optane:
1. Usa la procedura: [Creazione di un server bare metal personalizzato](../bare-metal/baremetal-provision.html).
* Seleziona le seguenti opzioni nel modulo di ordine:

|Sezione|Opzione da selezionare
|------|------|
|Data Center|Per utilizzare l'unità Intel Optane, seleziona uno dei seguenti data center:<br>AMS03 - Amsterdam<br>DAL09 - Dallas<br>DAL10 - Dallas<br>DAL12 - Dallas<br>FRA02 - Francoforte<br>LON02 - Londra<br>MEL01 - Melbourne<br>MON01 - Montreal<br>OSL01 - Oslo<br>SJC03 - San Jose<br>TOR01 - Toronto<br>WDC04 - Washington, DC|
|Server|I seguenti server sono compatibili con l'unità Intel Optane<br>Intel Xeon 4110 con un massimo di 12 unità<br>Intel Xeon 5120 con un massimo di 12 unità<br>Intel Xeon 6140 con un massimo di 12 unità<br>Intel Xeon E5-2620 v4 con supporto GPU<br>Intel Xeon E5-2650 v4 con supporto GPU<br>Intel Xeon E5-2690 v4 con supporto GPU<br><br>  **Nota**: se selezioni E5-2620 v4, E5-2650 v4 o E5-2650 v4, l'unità Intel Optane sostituisce la tua GPU e quindi non puoi avere sia una GPU che un'unità Intel Optane.|
|Componenti PCIe| Seleziona un'unità Optane Intel per il primo o il secondo componente PCIe oppure per entrambi.|
|Sistema operativo|Per le unità Optane fornite da Intel, i seguenti sistemi operativi sono certificati da Intel:<br>Windows Server 2016 (tutte le edizioni)<br>Windows Server 2012 R2 (tutte le edizioni)<br><br>Per le unità In-box, open-source e non Intel, la compatibilità e la funzionalità sono convalidate ma non certificate:<br>Red Hat Enterprise Linux 7.x (64 bit)<br>Red Hat Enterprise Linux 6.x (64 bit).
