---
copyright:
  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID 監視常駐程式的名稱及位置
{{site.data.keyword.cloud}} 主要使用 Adaptec 及 LSI RAID 卡，但針對舊式硬體有一些例外。下表概述 RAID 管理程式位置、監視器位置、配置及 RAID 警示設定。

藉由變更 RAID 卡配置中的 SMTP 伺服器及通知電子郵件目的地，即可配置 RAID 警示以略過入口網站監視處理程序。如果您變更這些配置，IBM 就無法通知您有關 RAID 的問題，或自動追蹤問題，直到解決為止。除非您知道有其風險，否則請不要變更所提供的配置。

<caption>表 1. RAID 配置及設定</caption>

||LSI Linux|LSI Windows|Adaptec Linux|Adaptec Windows|
|---|---|---|---|---|
|**管理程式名稱**|LSI MegaRAID Storage Manager|LSI MegaRAID Storage Manager|Adaptec Storage Manager|Adaptec Storage Manager|
|**管理程式位置**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**監視器名稱**|MR_Monitor|MRMonitor|Adaptec Event Manager|Adaptec Event Manager|
|**監視器位置**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**處理程序名稱**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**日誌位置**|OS 的預設訊息日誌位置，例如 /var/log/messages|僅限 GUI|/usr/StorMan/RaidEvtA.log|僅限 GUI|
|**通知電子郵件目的地**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**通知電子郵件來源格式**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**電子郵件埠**|25|25|25|25|
|**SMTP 伺服器**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**替代通知選項**|將「SMTP 伺服器」變更為本端 SMTP 伺服器。本端 SMTP 伺服器需要適當的防火牆配置。|將「SMTP 伺服器」變更為本端 SMTP 伺服器。本端 SMTP 伺服器需要適當的防火牆配置。|將「SMTP 伺服器」變更為本端 SMTP 伺服器。本端 SMTP 伺服器需要適當的防火牆配置。|將「SMTP 伺服器」變更為本端 SMTP 伺服器。本端 SMTP 伺服器需要適當的防火牆配置。|
