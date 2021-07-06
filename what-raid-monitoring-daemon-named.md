---

copyright:
  years: 2017, 2020
lastupdated: "2020-11-11"

keywords: raid monitoring daemon

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Name and location of the RAID monitoring daemon
{: #bm-raid-monitoring-daemon}

{{site.data.keyword.cloud}} primarily uses Adaptec and Broadcom RAID cards with a few exceptions for traditional hardware. The following table outlines the RAID manager locations, monitor locations, configurations, and RAID alert settings.

You can configure RAID alerts to bypass the monitoring process by changing the SMTP server and notification email destination in the configuration for a RAID card. If you change these configurations, IBM cannot notify you of RAID issues or automatically track the problem until resolution. Do not alter the provided configuration unless you are aware of the risks.

<caption>Table 1. RAID configurations and settings</caption>

||Broadcom Linux|Broadcom Windows|Adaptec Linux|Adaptec Windows|
|---|---|---|---|---|
|**Manager Name**|Broadcom MegaRAID Storage Manager|Broadcom MegaRAID Storage Manager|Adaptec Storage Manager|Adaptec Storage Manager|
|**Manager Location**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Monitor Name**|MR_Monitor|MRMonitor|Adaptec Event Manager|Adaptec Event Manager|
|**Monitor Location**|/opt/Broadcom/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\Broadcom\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Process Name**|/opt/Broadcom/mrmonitor/bin/mrmonitord|||||
|**Log Location**|Default Message Log Location for OS such as /var/log/messages|GUI Only|/usr/StorMan/RaidEvtA.log|GUI Only|
|**Notification E-Mail Destination**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**Notification E-Mail Source Format**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**E-Mail Port**|25|25|25|25|
|**SMTP Server**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**Alternate Notification Options**|Change SMTP Server to a local SMTP server. The local SMTP server needs appropriate firewall configurations.|Change SMTP Server to a local SMTP server. The local SMTP server needs appropriate firewall configurations.|Change SMTP Server to a local SMTP server. The local SMTP server needs appropriate firewall configurations.|Change SMTP Server to a local SMTP server. The local SMTP server needs appropriate firewall configurations.|
