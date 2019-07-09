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

# ベア・メタル・サーバーについて
{: #about-bm}

{{site.data.keyword.baremetal_long}} は、お客様の Infrastructure as a Service ソリューションの基盤となるものです。 高速な入出力が必要なゲーム開発者でも、ユーザー向けに高性能サーバーの性能をさらに向上させる必要がある場合でも、{{site.data.keyword.baremetal_short}} なら、その計算ニーズに応えることができます。
{:shortdesc}

{{site.data.keyword.baremetal_short}} は、時間課金または月額課金の自分専用シングル・テナント・サーバーです。このサーバーには、他のお客様と共有している部分は、サーバーのリソースを含めて何もありません。 サーバーはハイパーバイザーなしでプロビジョンされ、1 つ以上のデータ・センターにデプロイされますが、このサーバーをユーザーはご自分で管理します。複数の {{site.data.keyword.baremetal_short}} が、同じラック上に配置されているかのように、{{site.data.keyword.cloud_notm}} 仮想プライベート・ネットワークで通信できます。

## あらゆるワークロードに対応するサーバー
{: #servers-every-need}

{{site.data.keyword.cloud_notm}} には、あらゆるワークロードに適合する {{site.data.keyword.baremetal_short}} があります。 詳しくは、[Bare Metal Server](https://www.ibm.com/cloud/bare-metal-servers){: external} を参照してください。

### 高速プロビジョニング・サーバー
{: #Popular-bm}

{{site.data.keyword.cloud_notm}} では、ほとんどのユースケースのニーズを満たす、事前構成済みのサーバーを提供しています。 このようなサーバーは、コンピュート・オプション (コアの数、速度、RAM、およびドライブ数) が事前設定されているので、「高速プロビジョン」と考えられています。 事前設定されているサーバーは、プロビジョニング後 30 分ないし 40 分で構成の準備が整います。 

### カスタム・ベースのサーバー
{: #custom-based-bm}

どの高速プロビジョニング・サーバーを使用してもワークロードのニーズに合わない場合は、ご自分のニーズに合うように {{site.data.keyword.baremetal_short}} をカスタマイズできます。カスタマイズされたサーバーがプロビジョンされるのは 2 時間ないし 4 時間後になりますが、提示されるコア、速度、RAM、そしてドライブの種類は大幅に広がります。 

### POWER8 ベースのカスタム・サーバー
{: #bm-power8}

{{site.data.keyword.cloud_notm}} では、IBM POWER8 ベースのベアメタル・サーバーをプロビジョンするオプションを提供しています。 POWER8 サーバーは POWER8 プロセッサーと OpenPower ベースのプラットフォームを使用してビルドされており、特に、データ、コグニティブ・システム、および Web のワークロードを Linux にクラウド・ベースでデプロイするようチューニングされています。 詳しくは、「[POWER8 Servers](https://www.ibm.com/cloud/bare-metal-servers/power){: external}」を参照してください。

### SAP 認定ベアメタル・サーバー
{: #bm-SAP-cert}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} は、SAP HANA と SAP NetWeaver のワークロードをサポートしていることが認定されています。 詳しくは、[SAP 認定インフラストラクチャー](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}を参照してください。

## ベアメタル・サーバーで使用可能なオプション<!--test new section - test as each option goes GA-->
{: #options-for-bare-metal-servers}
{{site.data.keyword.cloud_notm}} には、ニーズに合わせてカスタマイズできる {{site.data.keyword.baremetal_short}} オプションがあります。

### Intel Cascade Lake CPU サポート
<!--Need to add which servers are also available for SAP once the certification is done-->
ベアメタル・サーバーのプロビジョン時に、以下の Intel Cascade Lake CPU から選択できるようになりました。

* Intel Xeon 4210 (10 コア、2.2 GHz、85 W)
* Intel Xeon 5218 (16 コア、2.3 GHz、125 W)
* Intel Xeon 6248 (20 コア、2.6 GHz、150 W)
<!--Intel Xeon 8280M (28-Core, 2.7 GHz, 205 W)--><br>

<br>Cascade Lake プロセッサーは、以下のデータ・センターで使用可能です。

<table style="width:100%">
<CAPTION>表 1. Cascade Lake プロセッサーを備えたデータ・センター</CAPTION>
 <tr>
   
   <th colspan="6">データ・センター</th>
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


### 動的インベントリー
{: #bm-dynamic-inv}

ベアメタル・サーバーのプロビジョン時に、どのデータ・センターのどのサーバーを選択できるか確認できるようになりました。ただし、このオプションは毎時オファリングでのみ選択できます。月次オファリングでは、どのサーバーが使用可能かを確認することができません。ベアメタル・サーバーのプロビジョンについて詳しくは、[複数の高速プロビジョニング・サーバーからの選択](/bare-metal?topic=bare-metal-bm-select-popular-servers)を参照してください。

### ブロック/ファイル・ストレージ・アドオン
{: #bm-block-and-file-add-on}

追加のストレージが必要な場合、{{site.data.keyword.IBM_notm}} で簡単に追加することができます。ベアメタル・サーバーのプロビジョン時に、ブロック/ファイル・ストレージ (20 から 12,000 GB) を注文できるようになりました。 

アドオン・ストレージは、ベアメタル・サーバーに自動的には接続されません。サーバーのプロビジョン後にアドオン・ストレージをベアメタル・サーバーに接続する必要があります。
{: note} 

<!--The add-on storage shares the data center that your bare metal server is on.-->

ブロック/ファイル・ストレージについて詳しくは、以下のリンクを参照してください。
* [ブロック・ストレージについて](/docs/infrastructure/BlockStorage?topic=BlockStorage-About)
* [ファイル・ストレージについて](/docs/infrastructure/FileStorage?topic=FileStorage-about)
