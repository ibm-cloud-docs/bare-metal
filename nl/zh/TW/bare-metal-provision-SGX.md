---

copyright:
  years: 2018, 2019
lastupdated: "2018-04-02"

keywords: provision, sgx, provision server Intel SGX architecture, Intel SGX architecture

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 使用 Intel SGX 架構佈建裸機伺服器
{: #bm-server-provision-sgx}

1. 使用程序：[建置自訂裸機伺服器](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server)。
* 在訂單表單上選取下列選項：

|區段|選取的選項
|
|------|------|
|伺服器|單一處理器，<br> Intel Xeon E3-1270 第 6 版，儲存空間為最多 4 台磁碟機|
|映像檔|- Windows Server 2016 Standard Edition（64 位元）<br>- Windows Server 2016 Standard Edition（64 位元）<br> - Windows Server 2016 Datacenter Edition（64 位元）<br>- CentOS 7.x（64 位元）<br> - Ubuntu Linux 16.04 LTS Xenial Xerus（64 位元）<br>- CentOS 7.x（64 位元）<br>- Red Hat Enterprise Linux 7.x（64 位元）（每個處理器授權）|
|映像檔附加程式|Software Guard Extensions|
