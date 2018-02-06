---



copyright:
  years: 2017
lastupdated: "2017-12-05"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 配置裸機伺服器

在佈建 {{site.data.keyword.baremetal_long}} 之前，最好花一些時間來做出配置決策。這樣可讓佈建處理程序更為快速且平穩。
{:shortdesc}

## 判定伺服器的使用並調整其大小

第一項作業是判定要如何使用 {{site.data.keyword.baremetal_short}}。例如，您要將它用於開發/測試或正式作業環境？您要測試使用者體驗、處理冗長的演算法、備份及還原資料，或增加延遲速度嗎？

判定要如何使用 {{site.data.keyword.baremetal_short}} 之後，您需要調整其大小。[SoftLayer 總擁有成本計算機](http://www.softlayer.com/tco/)可協助您判定最符合您需求的 {{site.data.keyword.baremetal_short}} 內容。

## 選取伺服器

{{site.data.keyword.cloud_notm}} 提供七個快速佈建伺服器，確保您具有工作負載所需的效能。目前在英國及美國南部地區有提供這些伺服器。

| **配置** | **處理器** | **記憶體** | **硬碟** | **埠速度** |
|-------------------|---------------|------------|----------------|----------------|
| Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3（4 核心、3.50 GHz）|32 GB RAM |1 個內部硬碟 |100 Mbps 最大埠速度|
|Intel Xeon E5-2620 v3 |Dual Intel Xeon E5-2620 v3（6 核心、2.40 GHz）|64 GB RAM |2 個內部硬碟 |100 Mbps 最大埠速度|
|Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3（4 核心、3.50 GHz）|32 GB RAM |2 個內部硬碟 |100 Mbps 最大埠速度|
|Intel Xeon E5-2650 v3 |Dual Intel Xeon E5-2650 v3（10 核心、2.30 GHz）|128 GB RAM |1 個內部硬碟 |100 Mbps 最大埠速度|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3（12 核心、2.60 GHz）|128 GB RAM |2 個內部硬碟 |100 Mbps 最大埠速度|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3（12 核心、2.60 GHz）|64 GB RAM |4 個內部硬碟 |1,000 Mbps 最大埠速度|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3（12 核心、2.60 GHz）|256 GB RAM |4 個內部硬碟 |1,000 Mbps 最大埠速度|

除了七個快速佈建伺服器之外，{{site.data.keyword.cloud_notm}} 已展開其 {{site.data.keyword.baremetal_short}} 供應項目，以包括 POWER8 型裸機系統。這些系統的建置是使用 {{site.data.keyword.IBM_notm}} POWER8 處理器及 OpenPOWER 型平台，而此平台是針對 Linux 上的雲端型資料部署、認知及 Web 工作負載特別調整。

可以升級任何 {{site.data.keyword.baremetal_short}}，以包括未計量（無限制）頻寬。所有未計量的裝置都位在專用的專用埠上。

## 設定裸機伺服器

選取資料中心、伺服器及計費選項（每月或每小時）之後，您需要決定如何配置伺服器。**配置 {{site.data.keyword.baremetal_short}}** 頁面上的部分欄位（「伺服器」、RAM、「圖形處理裝置」及「次要圖形處理裝置」）預設都會根據您的伺服器選項。下表說明您可以定義值的欄位。

| **欄位** | **說明** | 
|-------------------|---------------|
|作業系統 |從 CentOS、FreeBSD、Microsoft、Red Hat、Unbuntu 或「其他」中進行選取。|
|硬碟 |「磁碟配置」工具會根據您選取的 OS 預先填入欄位，以協助您設定硬碟。|
|公用頻寬 |決定在一個月的期間，可以透過 publick 介面傳送的資料量。針對需要透過此介面所傳送之安裝資料的測試環境，需要調整超過一開始所傳送資料量的值。您可能要考量 [{{site.data.keyword.cloud_notm}} 內容遞送網路](https://www.ibm.com/cloud/cdn)，以將起始資料載入傳送至其中一個 {{site.data.keyword.cloud_notm}} 資料中心。|
|上行鏈路埠速度 |判定內部及外部介面的速度。|
|公用次要 IP 位址 |將其他 IP 位址指派給伺服器。根據您的情境，您可能需要進一步指派給伺服器的 IP 位址。另外還可以使用數量為 1、2、4、8、16 或 32 的 IPv4 位址。|
|主要 IPv6 位址 |指派給伺服器的內部及外部介面。|
|公用靜態 IPv6 位址 |從 /64 區塊指派其他 IPv6 位址。|
|硬體與軟體防火牆、防毒與防間諜軟體保護，以及侵入與偵測和保護 |如果伺服器將是網際網路面向，請選取適當的選項。強烈建議您讓公司安全部門符合 {{site.data.keyword.cloud_notm}} 支援中心的標準，以討論這些選項的詳細資料。|
|Evault |代理程式型備份工具，可以安裝在伺服器上，以抄寫伺服器之間的備份。|

如需進一步資訊，請參閱[設計決策工具](http://knowledgelayer.softlayer.com/learning/softlayer-design-decision-tool)或「{{site.data.keyword.cloud_notm}} 支援」。


## 進階系統配置

在您按一下**新增至訂單**按鈕並將您重新導向至「結帳」頁面之後，即完成進階系統配置。下表說明「進階系統配置」下的欄位。

| **欄位** | **說明** | 
|-------------------|---------------|
|主機名稱 |伺服器的永久或暫時名稱，例如，_server1_。|
|網域 |不應該與網際網路網域名稱衝突的子網域名稱，例如，_test.acme.com_。|
|VLAN 選擇 |如果您的帳戶下有 VLAN，因為您已訂購至少一部伺服器，則可以將新伺服器新增至該 VLAN。|
|佈建 Script |您可以提供 Script，以容許您在佈建伺服器之後自動執行某些步驟。|
|SSH 金鑰 |您可以提供 SSH 金鑰的公開金鑰，以容許您在佈建之後登入伺服器。|
