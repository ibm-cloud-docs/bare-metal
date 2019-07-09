---

copyright:
  years: 1994, 2019
lastupdated: "2019-05-02"

keywords: back up, recovery, IBM Cloud Backup, r1soft

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 备份和恢复
{: #sm-back-up-recovery}

{{site.data.keyword.Bluemix_notm}} 提供了各种可缩放的[备份和存储解决方案 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/cloud/storage){: new_window} 以满足您的备份需求。但是，{{site.data.keyword.Bluemix_notm}} 不会完成客户设备的备份。您帐户上的用户必须启动设备上所有安排的备份和一次性备份。

如果一个帐户上存在两个或更多 {{site.data.keyword.baremetal_short}}，那么可以在一个设备上备份另一个设备的数据。专用网络流量没有强制实施带宽限制，因此可以在任何时间将数据备份到共享帐户的任何设备或在这些设备之间传输数据。有若干备份解决方案可用于 {{site.data.keyword.baremetal_short}}，包括以下解决方案：

* [IBM Cloud Backup](/docs/infrastructure/Backup?topic=Backup-getting-started#getting-started) 是一种企业备份解决方案，可以跨多个服务器自动执行备份。数据会存储到企业 SAN（存储区域网络）中。
* [网络连接存储器 (NAS)](/docs/infrastructure/network-attached-storage?topic=network-attached-storage-GettingStarted#GettingStarted) 是一种业界标准，可在服务器关闭时为关键数据提供存储。数据会存储到企业 SAN（存储区域网络）中。
* [R1Soft CDP](/docs/infrastructure/software?topic=software-ordering-r1soft#ordering-r1soft) 提供高性能磁盘到磁盘服务器备份，支持集中管理和数据存储库。R1Soft CDP 可在块级别保护数据，并且服务器上的唯一磁盘块在所有恢复点中仅存储一次，从而提高存储效率。
