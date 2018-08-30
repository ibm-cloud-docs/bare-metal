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

# 佈建 Intel Optane 相容裸機伺服器
若要使用 Intel Optane 磁碟機佈建裸機伺服器，請執行下列動作：
1. 使用程序：[建置自訂裸機伺服器](../bare-metal/baremetal-provision.html)。
* 在訂單表單上選取下列選項：

|區段|選取的選項
|------|------|
|資料中心|若要使用 Intel Optane 磁碟機，請選取下列其中一個資料中心：<br>AMS03 - 阿姆斯特丹<br>DAL09 - 達拉斯<br>DAL10 - 達拉斯<br>DAL12 - 達拉斯<br>FRA02 - 法蘭克福<br>LON02 - 倫敦<br>MEL01 - 墨爾本<br>MON01 - 蒙特婁<br>OSL01 - 奧斯陸<br>SJC03 - 聖荷西<br>TOR01 - 多倫多<br>WDC04 - 華盛頓特區|
|伺服器|下列伺服器與 Intel Optane 磁碟機相容<br>Intel Xeon 4110（最多 12 台磁碟機）<br>Intel Xeon 5120（最多 12 台磁碟機）<br>Intel Xeon 6140（最多 12 台磁碟機）<br>Intel Xeon E5-2620 v4（含 GPU 支援）<br>Intel Xeon E5-2650 v4（含 GPU 支援）<br>Intel Xeon E5-2690 v4（含 GPU 支援）<br><br>  **附註**：如果您選取 E5-2620 v4、E5-2650 v4 或 E5-2650 v4，則 Intel Optane 磁碟機會取代您的 GPU，因此您不能同時具有 GPU 和 Intel Optane 磁碟機。|
|PCIe 元件|為第一個及/或第二個 PCIe 元件選取 Intel Optane 磁碟機。|
|作業系統|對於 Intel 提供的 Optane 驅動程式，下列作業系統已由 Intel 認證：<br>Windows Server 2016（所有版本）<br>Windows Server 2012 R2（所有版本）<br><br>對於 In-box、開放程式碼的非 Intel 驅動程式，相容性及功能已經過驗證，但未經過認證：<br>Red Hat Enterprise Linux 7.x（64 位元）<br>Red Hat Enterprise Linux 6.x（64 位元）。
