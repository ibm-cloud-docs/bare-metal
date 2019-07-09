---

copyright:
  years: 2016, 2019
lastupdated: "2019-06-19"

keywords: bare metal, bare metal servers, POWER8, SAP-certified, {{site.data.keyword.baremetal_long}}, {{site.data.keyword.baremetal_short}}, available bare metal, cascade lake

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:note: .note}

# Informazioni sui server bare metal
{: #about-bm}

{{site.data.keyword.baremetal_long}} sono il punto cardine per la tua soluzione IaaS (infrastructure-as-a-service). Se sei uno sviluppatore di giochi che ha bisogno di I/O ad alta velocità o se hai bisogno di configurare dei server ad elevate prestazioni per i tuoi utenti, {{site.data.keyword.baremetal_short}} può essere la risposta alle tue esigenze di elaborazione.
{:shortdesc}

Il tuo {{site.data.keyword.baremetal_short}} è un server a singolo tenant orario o mensile dedicato a te; nessuna sua parte, comprese le risorse server, è condivisa con altri clienti. Sei tu a gestire il tuo server, di cui viene eseguito il provisioning senza un hypervisor e viene distribuito in uno o più data center. Più {{site.data.keyword.baremetal_short}} possono comunicare sulla VPN (virtual private network) di {{site.data.keyword.cloud_notm}} come se si trovassero sullo stesso rack.

## Server per ogni carico di lavoro
{: #servers-every-need}

{{site.data.keyword.cloud_notm}} dispone di {{site.data.keyword.baremetal_short}} per soddisfare ogni carico di lavoro. Per ulteriori informazioni, vedi [Bare Metal Servers](https://www.ibm.com/cloud/bare-metal-servers){: external}

### Server di provisioning veloce 
{: #Popular-bm}

{{site.data.keyword.cloud_notm}} offre server preconfigurati che soddisfano le esigenze della maggior parte dei casi di utilizzo. Questi server sono considerati di "provisioning veloce" perché le tue opzioni di calcolo (numero di core, velocità, RAM e numero di unità) sono preimpostate. I server preimpostati sono pronti per la configurazione 30 - 40 minuti dopo il provisioning. 

### Server personalizzati
{: #custom-based-bm}

Se uno dei server di provisioning veloce non soddisfa le esigenze del tuo carico di lavoro, puoi personalizzare il tuo {{site.data.keyword.baremetal_short}} per soddisfare i tuoi bisogni. Il provisioning dei server personalizzati viene eseguito in 2 - 4 ore e offre una maggiore varietà di core, velocità, RAM e unità. 

### Server basati su POWER8 personalizzati
{: #bm-power8}

{{site.data.keyword.cloud_notm}} ti offre l'opzione di eseguire il provisioning di un server bare metal basato su IBM POWER8. I server POWER8 sono sviluppati con il processore POWER8 e una piattaforma basata su OpenPower, regolata in modo mirato per le distribuzioni basate sul cloud di carichi di lavoro web, cognitivi e di dati su Linux. Per ulteriori informazioni, vedi [POWER8 Servers](https://www.ibm.com/cloud/bare-metal-servers/power){: external}.

### Server bare metal certificati per SAP
{: #bm-SAP-cert}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} sono certificati per supportare i tuoi carichi di lavoro SAP HANA e SAP NetWeaver. Per ulteriori informazioni, vedi [SAP-certified infrastructure](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}.

## Opzioni disponibili per i server bare metal <!--test new section - test as each option goes GA-->
{: #options-for-bare-metal-servers}
{{site.data.keyword.cloud_notm}} dispone di opzioni {{site.data.keyword.baremetal_short}} che puoi personalizzare per soddisfare le tue esigenze.

### Supporto per CPU Intel Cascade Lake
<!--Need to add which servers are also available for SAP once the certification is done-->
Puoi ora scegliete tra le seguenti CPU Intel Cascade Lake quando esegui il provisioning di un server bare metal:

* Intel Xeon 4210 (10-Core, 2.2 GHz, 85 W)
* Intel Xeon 5218 (16-Core, 2.3 GHz, 125 W)
* Intel Xeon 6248 (20-Core, 2.6 GHz, 150 W)
<!--Intel Xeon 8280M (28-Core, 2.7 GHz, 205 W)--><br>

<br>I processori Cascade Lake sono disponibili nei seguenti data center:

<table style="width:100%">
<CAPTION>Tabella 1. Data center con i processori Cascade Lake</CAPTION>
 <tr>
   
   <th colspan="6">Data center</th>
 </tr>
 <tr>
   <td>DAL10</td>
   <td>FRA02</td>
   <td>LON04</td>
   <td>SYD01</td>
   <td>TOK02</td>
   <td>WDC04</td>
   
</tr>

<tr>
  <td>DAL12</td>
  <td>FRA04</td>
  <td>LON05</td>
  <td>SYD04</td>
  <td>TOK04</td>
  <td>WDC06</td>
  
</tr>

<tr>
  <td>DAL13</td>
  <td>FRA05</td>
  <td>LON06</td>
  <td>SYD05</td>
  <td>TOK05</td>
  <td>WDC07</td>
</tr>
</table>


### Inventario dinamico
{: #bm-dynamic-inv}

Puoi ora vedere quali server sono disponibili in quali data center quando esegui il provisioning di un server bare metal. Ma questa opzione è disponibile solo per l'offerta oraria. Non puoi vedere la disponibilità server con l'offerta mensile. Per ulteriori informazioni sul provisioning di un server bare metal, vedi [Selezione dai server di provisioning veloce](/bare-metal?topic=bare-metal-bm-select-popular-servers).

### Componente aggiuntivo di archiviazione blocchi e file
{: #bm-block-and-file-add-on}

Se hai bisogno di ulteriore archiviazione, {{site.data.keyword.IBM_notm}} lo rende semplice! Puoi ora ordinare l'archiviazione blocchi o file (20 - 12.000 GB) quando esegui il provisioning di un server bare metal. 

La tua archiviazione aggiuntiva non viene automaticamente connessa al tuo server bare metal. Devi connettere l'archiviazione aggiuntiva al tuo server bare metal dopo il provisioning del tuo server.
{: note} 

<!--The add-on storage shares the data center that your bare metal server is on.-->

Per ulteriori informazioni sull'archiviazione blocchi e file, vedi i seguenti link.
* [Informazioni sull'archiviazione blocchi](/docs/infrastructure/BlockStorage?topic=BlockStorage-About)
* [Informazioni sull'archiviazione file](/docs/infrastructure/FileStorage?topic=FileStorage-about)
