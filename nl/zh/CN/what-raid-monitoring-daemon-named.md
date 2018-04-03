---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID 监视守护程序的名称和位置
{{site.data.keyword.cloud}} 主要使用 Adaptec 和 LSI RAID 卡，但对于旧硬件有一些例外情况。下面的图表概述了 RAID 管理器位置、监视器位置、配置和 RAID 警报设置。

您可以通过更改给定 RAID 卡的配置中的 SMTP 服务器和通知电子邮件目标来配置 RAID 警报，以绕过门户网站监视进程。更改这些配置后，IBM 即无法通知您 RAID 问题，也无法自动跟踪问题直至解决。因此，除非您了解这些风险，否则请勿更改所提供的配置。

||LSI - Linux|LSI - Windows|Adaptec - Linux|Adaptec - Windows|
|---|---|---|---|---|
|**管理器名称**|LSI MegaRAID Storage Manager|LSI MegaRAID Storage Manager|Adaptec Storage Manager|Adaptec Storage Manager|
|**管理器位置**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**监视器名称**|MR_Monitor|MRMonitor|Adaptec Event Manager|Adaptec Event Manager|
|**监视器位置**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**进程名称**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**日志位置**|操作系统的缺省消息日志位置，例如 /var/log/messages|仅限 GUI|/usr/StorMan/RaidEvtA.log|仅限 GUI|
|**通知电子邮件目标**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**通知电子邮件源格式**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**电子邮件端口**|25|25|25|25|
|**SMTP 服务器**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**备用通知选项**|将“SMTP 服务器”更改为本地 SMTP 服务器。本地 SMTP 服务器需要相应的防火墙配置。|将“SMTP 服务器”更改为本地 SMTP 服务器。本地 SMTP 服务器需要相应的防火墙配置。|将“SMTP 服务器”更改为本地 SMTP 服务器。本地 SMTP 服务器需要相应的防火墙配置。|将“SMTP 服务器”更改为本地 SMTP 服务器。本地 SMTP 服务器需要相应的防火墙配置。|
