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

# Bare Metal Server 정보
{: #about-bm}

{{site.data.keyword.baremetal_long}}는 IaaS(Infrastructure-as-a-Service) 솔루션의 기초입니다. 고속 I/O가 필요한 게임 개발자인지 사용자를 위해 고성능 서버를 설정해야 하는지에 상관없이 {{site.data.keyword.baremetal_short}}에서는 컴퓨팅 요구사항에 대한 해결책을 제시할 수 있습니다.
{:shortdesc}

{{site.data.keyword.baremetal_short}}는 사용자 전용의 시간별 또는 월별 싱글 테넌트 서버이고, 서버 리소스 등의 어떤 부분도 다른 고객과 공유하지 않습니다. 사용자는 하이퍼바이저 없이 프로비저닝되고 하나 이상의 데이터 센터에 배치된 서버를 관리합니다. 다중 {{site.data.keyword.baremetal_short}}는 동일한 랙에 배치된 것처럼 {{site.data.keyword.cloud_notm}} 가상 사설망(VPN)에서 통신할 수 있습니다.

## 모든 워크로드용 서버
{: #servers-every-need}

{{site.data.keyword.cloud_notm}}에는 모든 워크로드에 적합한 {{site.data.keyword.baremetal_short}}가 있습니다. 자세한 정보는 [베어메탈 서버](https://www.ibm.com/cloud/bare-metal-servers){: external}를 참조하십시오.

### 빠른 프로비저닝 서버
{: #Popular-bm}

{{site.data.keyword.cloud_notm}}에서는 대부분의 유스 케이스 요구사항을 충족하는 사전 구성된 서버를 제공합니다. 해당 서버는 컴퓨팅 옵션(코어 수, 속도, RAM 및 드라이브 수)이 사전 설정되어 있으므로 "빠른 프로비저닝"으로 간주됩니다. 사전 설정된 서버는 프로비저닝 후 30 - 40분 내에 구성할 준비가 됩니다. 

### 사용자 정의 기반 서버
{: #custom-based-bm}

빠른 프로비저닝 서버 중 하나가 워크로드 요구사항을 충족하지 못하면 요구사항을 충족하도록 {{site.data.keyword.baremetal_short}}를 사용자 정의할 수 있습니다. 사용자 정의된 서버는 2 - 4시간 내에 프로비저닝되며 매우 다양한 코어, 속도, RAM 및 드라이브를 제공합니다. 

### 사용자 정의 POWER8 기반 서버
{: #bm-power8}

{{site.data.keyword.cloud_notm}}에서는 IBM POWER8 기반 Bare Metal Server를 프로비저닝하는 옵션을 제공합니다. POWER8 서버는 POWER8 프로세서와 OpenPower 기반 플랫폼이 내장되어 있습니다. 이 플랫폼은 데이터, 코그너티브 및 웹 워크로드를 Linux에 클라우드 기반으로 배치할 수 있도록 특별히 조정됩니다. 자세한 정보는 [POWER8 서버](https://www.ibm.com/cloud/bare-metal-servers/power){: external}를 참조하십시오.

### SAP 인증 Bare Metal Server
{: #bm-SAP-cert}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}는 SAP HANA 및 SAP NetWeaver 워크로드를 지원하도록 인증되었습니다. 자세한 정보는 [SAP 인증 인프라](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}를 참조하십시오.

## 베어메탈 서버에 사용 가능한 옵션 <!--test new section - test as each option goes GA-->
{: #options-for-bare-metal-servers}
{{site.data.keyword.cloud_notm}}에는 요구사항에 맞게 사용자 정의가 가능한 {{site.data.keyword.baremetal_short}} 옵션이 있습니다.

### Intel Cascade Lake CPU 지원
<!--Need to add which servers are also available for SAP once the certification is done-->
이제 베어메탈 서버의 프로비저닝 시에 다음의 Intel Cascade Lake CPU 중에서 선택할 수 있습니다. 

* Intel Xeon 4210(10-코어, 2.2GHz, 85W)
* Intel Xeon 5218(16-코어, 2.3GHz, 125W)
* Intel Xeon 6248(20-코어, 2.6GHz, 150W)
<!--Intel Xeon 8280M (28-Core, 2.7 GHz, 205 W)--><br>

<br>Cascade Lake 프로세서는 다음의 데이터 센터에서 사용할 수 있습니다.

<table style="width:100%">
<CAPTION>표 1. Cascade Lake 프로세서의 데이터 센터</CAPTION>
 <tr>
   
   <th colspan="6">데이터 센터</th>
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


### 동적 인벤토리
{: #bm-dynamic-inv}

이제 베어메탈 서버의 프로비저닝 시에 어떤 서버가 어떤 데이터 센터에서 사용 가능한지 확인할 수 있습니다. 그러나 이 옵션은 시간별 오퍼링에만 사용할 수 있습니다. 월별 오퍼링으로는 서버 가용성을 볼 수 없습니다. 베어메탈 서버의 프로비저닝에 대한 자세한 정보는 [빠른 프로비저닝 서버에서 선택](/bare-metal?topic=bare-metal-bm-select-popular-servers)을 참조하십시오.

### 블록 및 파일 스토리지 추가 기능
{: #bm-block-and-file-add-on}

추가 스토리지가 필요하면 {{site.data.keyword.IBM_notm}}에서 도와드립니다! 이제 베어메탈 서버의 프로비저닝 시에 블록 스토리지와 파일 스토리지(20 - 12,000GB)를 주문할 수 있습니다. 

추가 스토리지는 베어메탈 서버에 자동으로 연결되지 않습니다. 서버를 프로비저닝한 후에 추가 스토리지를 베어메탈 서버에 연결해야 합니다.
{: note} 

<!--The add-on storage shares the data center that your bare metal server is on.-->

블록 및 파일 스토리지에 대한 자세한 정보는 다음 링크를 참조하십시오.
* [블록 스토리지 정보](/docs/infrastructure/BlockStorage?topic=BlockStorage-About)
* [파일 스토리지 정보](/docs/infrastructure/FileStorage?topic=FileStorage-about)
