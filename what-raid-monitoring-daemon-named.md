---

copyright:
  years: 2017, 2023
lastupdated: "2023-04-25"

keywords: raid monitoring daemon

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Name and location of the RAID monitoring daemon
{: #bm-raid-monitoring-daemon}

{{site.data.keyword.cloud}} primarily uses Adaptec and Broadcom RAID cards with a few exceptions for traditional hardware. The following table outlines the RAID manager locations, monitor locations, configurations, and RAID alert settings.

You can configure RAID alerts to bypass the monitoring process by changing the SMTP server and notification email destination in the configuration for a RAID card. If you change these configurations, IBM cannot notify, or automatically track the problem until resolution. Do not alter the provided configuration unless you are aware of the risks.

| RAID setting | Broadcom Linux | Broadcom Windows | Adaptec Linux | Adaptec Windows |
|---|---|---|---|---|
| Manager name | Broadcom MegaRAID Storage Manager | Broadcom MegaRAID Storage Manager | Adaptec Storage Manager | Adaptec Storage Manager |
| Manager location | `/opt/MegaRAID/storcli` | `C:\Program Files (x86)\MegaRAID Storage Manager` |`/usr/StorMan`| `C:\Program Files\Adaptec\Adaptec Storage Manager` |
| Monitor name | MR_Monitor | MRMonitor | Adaptec Event Manager | Adaptec Event Manager |
| Monitor location | `/opt/Broadcom/mrmonitor/bin/mrmonitord` | `C:\Program Files (x86)\Broadcom\MRMonitor` |`/usr/StorMan` | `C:\Program Files\Adaptec\Adaptec Storage Manager` |
| Process Name | `/opt/Broadcom/mrmonitor/bin/mrmonitord` | | | |
| Log location | Default message log location for OS such as `/var/log/messages` | GUI only | `/usr/StorMan/RaidEvtA.log` | GUI only |
| Notification email destination | [hwraid@softlayer.com](mailto:hwraid@softlayer.com) | [hwraid@softlayer.com](mailto:hwraid@softlayer.com) | [hwraid@softlayer.com](mailto:hwraid@softlayer.com) |[hwraid@softlayer.com](mailto:hwraid@softlayer.com) |
| Notification email force format | accountid_privatema@softlayer.com | accountid_privatemac@softlayer.com | accountid_privatemac@softlayer.com | accountid_privatemac@softlayer.com |
| Email port | 25 | 25 | 25 | 25 |
| SMTP server | raidalerts-smtp.networklayer.com | raidalerts-smtp.networklayer.com | raidalerts-smtp.networklayer.com | raidalerts-smtp.networklayer.com |
| Alternate notification options | Change SMTP server to a local SMTP server. The local SMTP server needs appropriate firewall configurations. | Change SMTP Server to a local SMTP server. The local SMTP server needs appropriate firewall configurations. | Change SMTP Server to a local SMTP server. The local SMTP server needs appropriate firewall configurations. | Change SMTP Server to a local SMTP server. The local SMTP server needs appropriate firewall configurations. |
{: caption="Table 1. RAID configurations and settings" caption-side="top"}
