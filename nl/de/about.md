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

# Informationen zu Bare-Metal-Servern
{: #about-bm}

{{site.data.keyword.baremetal_long}} sind das Fundament Ihrer IaaS-Lösung (Infrastructure-as-a-Service). Ob Sie ein Spieleentwickler sind, der Hochgeschwindigkeitseingabe und -ausgabe benötigt, oder ob Sie Hochleistungsserver für Ihre Benutzer einrichten müssen, {{site.data.keyword.baremetal_short}} hat die Lösung für Ihre Computeranforderungen.
{:shortdesc}

Ihr {{site.data.keyword.baremetal_short}} ist ein Server für einen einzelnen Tenant, mit stündlichen oder monatlichen Gebühren, der für Sie dediziert ist. Er wird in keinem Fall für andere Kunden freigegeben, auch nicht seine Ressourcen. Sie verwalten Ihren Server, der ohne einen Hypervisor bereitgestellt wird und in einem oder mehreren Rechenzentren implementiert wird. Mehrere {{site.data.keyword.baremetal_short}} können über das virtuelle private Netz von {{site.data.keyword.cloud_notm}} so kommunizieren, als ob sie sich in demselben Rack befinden würden.

## Server für jede Workload
{: #servers-every-need}

{{site.data.keyword.cloud_notm}} bietet passende {{site.data.keyword.baremetal_short}} für jede Workload. Weitere Informationen finden Sie unter [Bare-Metal-Server](https://www.ibm.com/cloud/bare-metal-servers){: external}.

### Server mit schneller Bereitstellung
{: #Popular-bm}

{{site.data.keyword.cloud_notm}} bietet vorkonfigurierte Server, die den Anforderungen der meisten Anwendungsfälle entsprechen. Diese Server ermöglichen eine schnelle Bereitstellung, da die Computeroptionen (Anzahl der Kerne, Geschwindigkeit, RAM und Anzahl der Laufwerke) voreingestellt sind. Vordefinierte Server sind 30-40 Minuten nach der Bereitstellung für die Konfiguration bereit. 

### Angepasste Server
{: #custom-based-bm}

Wenn keiner der Server mit schneller Bereitstellung Ihre Workloadanforderungen erfüllt, können Sie Ihren {{site.data.keyword.baremetal_short}} an Ihre Anforderungen anpassen. Angepasste Server werden in 2-4 Stunden bereitgestellt und bieten eine größere Vielfalt an Kernen, Geschwindigkeiten, RAM und Laufwerken. 

### Angepasste POWER8-basierte Server
{: #bm-power8}

{{site.data.keyword.cloud_notm}} bietet Ihnen die Möglichkeit, einen IBM POWER8-basierten Bare-Metal-Server bereitzustellen. POWER8-Server enthalten den POWER8-Prozessor und eine OpenPower-basierte Plattform, die speziell für cloudbasierte Implementierungen von Daten-, kognitiven und Web-Workloads unter Linux optimiert wurde. Weitere Informationen finden Sie unter [POWER8-Server](https://www.ibm.com/cloud/bare-metal-servers/power){: external}.

### Von SAP zertifizierte Bare-Metal-Server
{: #bm-SAP-cert}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} sind für die Unterstützung Ihrer SAP HANA- und SAP NetWeaver-Workloads zertifiziert. Weitere Informationen finden Sie unter [Von SAP zertifizierte Infrastruktur](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}.

## Verfügbare Optionen für Bare-Metal-Server <!--test new section - test as each option goes GA-->
{: #options-for-bare-metal-servers}
{{site.data.keyword.cloud_notm}} bietet Optionen für {{site.data.keyword.baremetal_short}}, die Sie an Ihren Bedarf anpassen können.

### Unterstützung für Intel Cascade Lake-CPU
<!--Need to add which servers are also available for SAP once the certification is done-->
Sie können jetzt beim Bereitstellen eines Bare-Metal-Servers aus den folgenden Intel Cascade Lake-CPUs auswählen:

* Intel Xeon 4210 (10-Core, 2,2 GHz, 85 W)
* Intel Xeon 5218 (16-Core, 2,3 GHz, 125 W)
* Intel Xeon 6248 (20-Core, 2,6 GHz, 150 W)
<!--Intel Xeon 8280M (28-Core, 2.7 GHz, 205 W)--><br>

<br>Cascade Lake-Prozessoren sind in den folgenden Rechenzentren verfügbar:

<table style="width:100%">
<CAPTION>Tabelle 1. Rechenzentren mit Cascade Lake-Prozessoren</CAPTION>
 <tr>
   
   <th colspan="6">Rechenzentren</th>
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


### Dynamisches Inventar
{: #bm-dynamic-inv}

Sie können jetzt sehen, welche Server in welchem Rechenzentrum verfügbar sind, wenn Sie einen Bare-Metal-Server bereitstellen. Diese Option ist jedoch nur für das Angebot auf Stundenbasis verfügbar. Bei dem Angebot auf Monatsbasis können Sie die Serververfügbarkeit nicht sehen. Weitere Informationen zur Bereitstellung eines Bare-Metal-Servers finden Sie unter [Server mit schneller Bereitstellung auswählen](/bare-metal?topic=bare-metal-bm-select-popular-servers).

### Add-on für Block- und Dateispeicher
{: #bm-block-and-file-add-on}

Wenn Sie zusätzlichen Speicher benötigen, hilft Ihnen {{site.data.keyword.IBM_notm}} dabei! Sie können jetzt Block- und Dateispeicher (20-12.000 GB) bestellen, wenn Sie einen Bare-Metal-Server bereitstellen. 

Ihr Add-on-Speicher wird nicht automatisch mit Ihrem Bare-Metal-Server verbunden. Sie müssen nach der Bereitstellung Ihres Servers den Add-on-Speicher mit Ihrem Bare-Metal-Server verbinden.
{: note} 

<!--The add-on storage shares the data center that your bare metal server is on.-->

Weitere Informationen zu Block- und Dateispeicher finden Sie unter den folgenden Links.
* [Informationen zu Blockspeicher](/docs/infrastructure/BlockStorage?topic=BlockStorage-About)
* [Informationen zu Dateispeicher](/docs/infrastructure/FileStorage?topic=FileStorage-about)
