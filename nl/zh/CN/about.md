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

# 关于裸机服务器
{: #about-bm}

{{site.data.keyword.baremetal_long}} 是基础架构即服务解决方案的基础。不管您是需要高速 I/O 的游戏开发者，还是需要为用户设置高性能服务器，{{site.data.keyword.baremetal_short}} 都可以满足您的计算需求。
{:shortdesc}

{{site.data.keyword.baremetal_short}} 是专供您使用的每小时或每月单租户服务器；没有任何部分（包括服务器资源）会与其他客户共享。服务器由您进行管理，它是不带系统管理程序进行供应的，并部署在一个或多个数据中心内。多个 {{site.data.keyword.baremetal_short}} 可以在 {{site.data.keyword.cloud_notm}} 虚拟专用网上就像部署在同一机架上一样进行通信。

## 适用于每种工作负载的服务器
{: #servers-every-need}

{{site.data.keyword.cloud_notm}} 的 {{site.data.keyword.baremetal_short}} 能够适应每种工作负载。有关更多信息，请参阅 [Bare Metal Servers](https://www.ibm.com/cloud/bare-metal-servers){: external}。

### 快速供应服务器
{: #Popular-bm}

{{site.data.keyword.cloud_notm}} 提供的是预配置的服务器，可满足大多数用例的需求。这些服务器被视为“快速供应”，因为已预置您的计算选项（内核数、速度、RAM 和驱动器数）。预置服务器在供应后 30 到 40 分钟即准备就绪可开始配置。 

### 基于定制的服务器
{: #custom-based-bm}

如果其中一个快速供应服务器不满足工作负载需求，那么可以定制 {{site.data.keyword.baremetal_short}} 以满足您的需求。定制的服务器在 2 到 4 小时内供应，并提供内核数、速度、RAM 和驱动器数的更丰富选项。 

### 基于 POWER8 的定制服务器
{: #bm-power8}

{{site.data.keyword.cloud_notm}} 提供了用于供应基于 IBM POWER8 的裸机服务器的选项。POWER8 服务器采用 POWER8 处理器和一个基于 OpenPOWER 的平台进行构建，该平台已专门针对在 Linux 上基于云部署数据、认知和 Web 工作负载而调整。有关更多信息，请参阅 [POWER8 服务器](https://www.ibm.com/cloud/bare-metal-servers/power){: external}。

### SAP 认证的裸机服务器
{: #bm-SAP-cert}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} 经过认证，支持 SAP HANA 和 SAP NetWeaver 工作负载。有关更多信息，请参阅 [SAP 认证的基础架构](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}。

## 裸机服务器的可用选项<!--test new section - test as each option goes GA-->
{: #options-for-bare-metal-servers}
{{site.data.keyword.cloud_notm}} 具有 {{site.data.keyword.baremetal_short}} 选项，您可以对这些选项进行定制以满足您的需求。

### Intel Cascade Lake CPU 支持
<!--Need to add which servers are also available for SAP once the certification is done-->
现在，供应裸机服务器时，可以从以下 Intel Cascade Lake CPU 进行选择：

* Intel Xeon 4210（10 核心，2.2 GHz，85 W）
* Intel Xeon 5218（16 核，2.3 GHz，125 W）
* Intel Xeon 6248（20 核，2.6 GHz，150 W）
<!--Intel Xeon 8280M (28-Core, 2.7 GHz, 205 W)--><br>

<br>Cascade Lake 处理器可用于以下数据中心：

<table style="width:100%">
<CAPTION>表 1. 具有 Cascade Lake 处理器的数据中心</CAPTION>
 <tr>
   
   <th colspan="6">数据中心</th>
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


### 动态库存
{: #bm-dynamic-inv}

现在，供应裸机服务器时，您可以看到在哪个数据中心内提供了哪些服务器。但是，此选项仅适用于按小时提供服务的产品。对于按月提供服务的产品，您无法查看服务器可用性。有关供应裸机服务器的更多信息，请参阅[从快速供应服务器中选择](/bare-metal?topic=bare-metal-bm-select-popular-servers)。

### 块存储器和文件存储器附加组件
{: #bm-block-and-file-add-on}

如果您需要额外的存储空间，{{site.data.keyword.IBM_notm}} 可轻松实现！现在，供应裸机服务器时，您可以订购块存储器和文件存储器 (20 - 12,000 GB)。 

您的附加组件存储器不会自动连接到裸机服务器。您需要在服务器供应之后将附加组件存储器连接到裸机服务器。
{: note} 

<!--The add-on storage shares the data center that your bare metal server is on.-->

有关块存储器和文件存储器的更多信息，请参阅以下链接。
* [关于块存储器](/docs/infrastructure/BlockStorage?topic=BlockStorage-About)
* [关于文件存储器](/docs/infrastructure/FileStorage?topic=FileStorage-about)
