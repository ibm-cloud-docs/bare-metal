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

# 供应采用 Intel SGX 体系结构的裸机服务器
{: #bm-server-provision-sgx}

1. 使用以下过程：[构建定制裸机服务器](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server)。
* 在订购表单上选择以下选项：

|部分|要选择的选项
|
|------|------|
|服务器|单处理器，<br> Intel Xeon E3-1270 v6，存储器最多 4 个驱动器|
|映像|- Windows Server 2016 Standard Edition（64 位）<br>- Windows Server 2016 Standard Edition（64 位）<br> - Windows Server 2016 Datacenter Edition（64 位）<br>- CentOS 7.x（64 位）<br> - Ubuntu Linux 16.04 LTS Xenial Xerus（64 位）<br>- CentOS 7.x（64 位）<br>- Red Hat Enterprise Linux 7.x（64 位）（按处理器许可）|
|映像附加组件|Software Guard Extensions|
