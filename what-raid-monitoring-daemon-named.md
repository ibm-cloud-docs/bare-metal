---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Name and location of the the RAID monitoring daemon
{{site.data.keyword.cloud}} primarily USES Adaptec and LSI RAID cards with a few exceptions for legacy hardware. The chart below outlines the RAID manager locations, monitor locations, configurations, and RAID alert settings.

You can configure RAID alerts to bypass the portal monitoring process by changing the SMTP server and notification E-Mail destination in the configuration for a given RAID card. When these configurations are changed IBM cannot notify you of RAID issues or automatically track the problem until resolution. Do not alter the provided configuration unless you are aware of the risks.

||LSI - Linux|LSI - Windows|Adaptec - Linux|Adaptec - Windows|
|---|---|---|---|---|
|**Manager Name**|LSI MegaRAID Storage Manager|LSI MegaRAID Storage Manager|Adaptec Storage Manager|Adaptec Storage Manager|
|**Manager Location**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Monitor Name**|MR_Monitor|MRMonitor|Adaptec Event Manager|Adaptec Event Manager|
|**Monitor Location**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Process Name**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**Log Location**|Default Message Log Location for OS e.g. /var/log/messages|GUI Only|/usr/StorMan/RaidEvtA.log|GUI Only|
|**Notification E-Mail Destination**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**Notification E-Mail Source Format**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**E-Mail Port**|25|25|25|25|
|**SMTP Server**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**Alternate Notification Options**|Change SMTP Server to a local SMTP server. The local SMTP server will need appropriate firewall configurations.|Change SMTP Server to a local SMTP server. The local SMTP server will need appropriate firewall configurations.|Change SMTP Server to a local SMTP server. The local SMTP server will need appropriate firewall configurations.|Change SMTP Server to a local SMTP server. The local SMTP server will need appropriate firewall configurations.|
