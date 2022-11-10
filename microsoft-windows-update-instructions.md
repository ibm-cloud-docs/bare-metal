---
copyright:
  years: 1994, 2022
lastupdated: "2022-11-10"

keywords: Microsoft Windows Update, software update services

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Microsoft Windows update information
{: #microsoft-windows-update-information}

IBM provides OS and software update services for Microsoft Windows Server environments free of charge.
{: shortdesc}

All update services at {{site.data.keyword.Bluemix_notm}} share the following features:
* Update traffic is routed from your server (over your private VLAN) to the private service network
* Update traffic is part of your unlimited private network bandwidth. This traffic does not reduce public bandwidth allotments.
* Updates speeds are faster than updating from vendors directly (upgraded ports speeds available on demand)
* Updates are readily available during worldwide heavy critical update days.
* In emergency situations, public ports can be shut down while still allowing updates to occur over the private network
* Servers are pre-configured to update automatically at deployment with manual updates available on demand.


{{site.data.keyword.Bluemix_notm}} update servers are on the private service network with the following location identifiers.

Microsoft, **wsus01.service.softlayer.com**

Always test kernel or service pack upgrades before you install them in production server environments. You can find technical information that is related to specific hardware, OS, and applications deployed by IBM in the FAQ or drivers section inside the control portal. IBM continually tests kernel and service pack upgrades and post related information (including drivers) to help the upgrade process.


## WSUS Windows Server Update Services
{: #wsus-windows-server-update-services}

In many cases, Microsoft Windows servers automatically pull updates from local Windows Server Update Services (WSUS) servers. However, if your server is provisioned with a cloud-init enabled image, you might need to manually update the Windows registry to use local {{site.data.keyword.cloud_notm}} Windows Server Update Services (WSUS) servers, rather than the default Microsoft WSUS servers.

If you order a virtual server with a Windows Server operating system without any add-ons, such as more software, post-provisioning scripts, or monitoring, it is likely that your server is provisioned with a cloud-init image. For more information about updating your registry to point to {{site.data.keyword.cloud_notm}} WSUS servers, see [Updating instance to use local WSUS server](/docs/bare-metal?topic=bare-metal-updating-an-instance-to-use-a-local-wsus-server).

For Microsoft Windows operating systems, servers are configured by default to download and install updates as soon as they become available. The server restarts automatically if a restart is required. Updates are completed to protect servers from crucial vulnerabilities. If you prefer to schedule your updates differently, you can change the update schedule through the **Windows Updates** feature in the control panel.
