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

# 關於裸機伺服器
{: #about-bm}

{{site.data.keyword.baremetal_long}} 是基礎架構即服務解決方案的基準。不論您是需要需要高速 I/O 的遊戲開發人員，還是需要為使用者設定高效能伺服器，{{site.data.keyword.baremetal_short}} 都可以回應您的運算需求。
{:shortdesc}

您的 {{site.data.keyword.baremetal_short}} 是按小時或按月的單一承租戶伺服器，它為您所專用，且未與其他客戶共用任何部分（包括伺服器資源）。伺服器由您管理，並在沒有 Hypervisor 的情況下進行佈建，而且可以部署在一個以上的資料中心內。多個 {{site.data.keyword.baremetal_short}} 可以在 {{site.data.keyword.cloud_notm}} 虛擬私密網路上進行通訊，就像位在相同的機架上一樣。

## 每個工作負載的伺服器
{: #servers-every-need}

{{site.data.keyword.cloud_notm}} 有 {{site.data.keyword.baremetal_short}} 可以適合每個工作負載。如需相關資訊，請參閱 [Bare Metal Server](https://www.ibm.com/cloud/bare-metal-servers){: external}。

### 快速佈建伺服器
{: #Popular-bm}

{{site.data.keyword.cloud_notm}} 提供符合大部分使用案例需求的預先配置伺服器。這些伺服器被視為「快速佈建」，因為您的運算選項（核心數量、速度、RAM，以及磁碟機數目）都已事先設定。事先設定的伺服器在佈建之後 30 - 40 分鐘便可以配置。 

### 自訂型伺服器
{: #custom-based-bm}

如果其中一個快速佈建伺服器不符合您的工作負載需求，您可以自訂 {{site.data.keyword.baremetal_short}} 以符合您的需求。自訂伺服器會在 2 到 4 小時內佈建，並且提供更多樣化的核心、速度、RAM 和磁碟機。 

### 自訂 POWER8 型伺服器
{: #bm-power8}

{{site.data.keyword.cloud_notm}} 為您提供佈建 IBM POWER8 型裸機伺服器的選項。POWER8 伺服器的建置是使用 POWER8 處理器及 OpenPower 型平台，而此平台是針對 Linux 上的雲端型資料部署、認知及 Web 工作負載特別調整。如需相關資訊，請參閱 [POWER8 Servers](https://www.ibm.com/cloud/bare-metal-servers/power){: external}。

### SAP 認證裸機伺服器
{: #bm-SAP-cert}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} 經過認證，可支援您的 SAP HANA 和 SAP NetWeaver 工作負載。如需相關資訊，請參閱 [SAP 認證基礎架構](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}。

## 裸機伺服器的可用選項<!--test new section - test as each option goes GA-->
{: #options-for-bare-metal-servers}
{{site.data.keyword.cloud_notm}} 有 {{site.data.keyword.baremetal_short}} 選項，您可以自訂這些選項以符合您的需求。

### Intel Cascade Lake CPU 支援
<!--Need to add which servers are also available for SAP once the certification is done-->
佈建裸機伺服器時，您現在可以從下列 Intel Cascade Lake CPU 當中進行選擇：

* Intel Xeon 4210（10 個核心、2.2 GHz、85 W）
* Intel Xeon 5218（16 個核心、2.3 GHz、125 W）
* Intel Xeon 6248（20 個核心、2.6 GHz、150 W）
<!--Intel Xeon 8280M (28-Core, 2.7 GHz, 205 W)--><br>

<br>下列資料中心提供 Cascade Lake 處理器：

<table style="width:100%">
<CAPTION>表 1. 具有 Cascade Lake 處理器的資料中心</CAPTION>
 <tr>
   
   <th colspan="6">資料中心</th>
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


### 動態庫存
{: #bm-dynamic-inv}

您現在可以在佈建裸機伺服器時，查看在哪個資料中心有哪些伺服器可用。但是，只有按小時計費的供應項目可以使用此選項。您無法查看按月計費供應項目的伺服器可用性。如需佈建裸機伺服器的相關資訊，請參閱[從快速佈建伺服器選取](/bare-metal?topic=bare-metal-bm-select-popular-servers)。

### 區塊與檔案儲存空間附加程式
{: #bm-block-and-file-add-on}

如果您需要額外的儲存空間，{{site.data.keyword.IBM_notm}} 讓您輕鬆做到！佈建裸機伺服器時，您現在可以訂購區塊及檔案儲存空間 (20 - 12,000 GB)。 

附加程式儲存空間不會自動連接至裸機伺服器。您必須在伺服器佈建後，將附加程式儲存空間連接至裸機伺服器。
{: note} 

<!--The add-on storage shares the data center that your bare metal server is on.-->

如需區塊和檔案儲存空間的相關資訊，請參閱下列鏈結。
* [關於區塊儲存空間](/docs/infrastructure/BlockStorage?topic=BlockStorage-About)
* [關於檔案儲存空間](/docs/infrastructure/FileStorage?topic=FileStorage-about)
