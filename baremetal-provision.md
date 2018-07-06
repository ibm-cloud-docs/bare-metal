---



copyright:
  years: 2017, 2018
lastupdated: "2018-07-06"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Building a custom bare metal server
{: #ordering-baremetal-server}

Prerequsites:
  * You must have an upgraded {{site.data.keyword.BluSoftlayer_full}} account.
  * You must be logged into one of the following sites:
    * [The {{site.data.keyword.cloud_notm}} catalog](https://console.bluemix.net/catalog/)
    * [The {{site.data.keyword.cloud_notm}} infrastructure customer portal](https://control.softlayer.com/)

Use the following steps to build a custom {{site.data.keyword.baremetal_short}}.

1. Launch the order form  and provision your server:<br>
<a href="https://control.bluemix.net/?orderType=bareMetalServerMonthlyOrder" target="_blank">Custom bare metal server provisioning</a>
1. Select a data center location for your server.
* Select a server from the three categories of servers by clicking the **Starting Price Per** link.
  * SAP Certified Servers (For more information on provisioning an SAP Certified Server, see [{{site.data.keyword.cloud_notm}} SAP-Certified Infrastructure](/docs/bare-metal/bare-metal-sap-applications.html))
  * Single Processor Multi-Core Servers
  * Dual Processor Multi-Core Servers

* Select from your configuration options. **Data Center**, **RAM**, and **Operating System** are required fields. All other fields are optional. For more information about the optional fields, see to **[Additional server configuration options](#addl-server-options)** .

    **Note**: an error message is displayed if a conflict exists between the server and operating system. For example, selecting Linux on a Microsoft SQL server.
* Click **Add to Order**. The Checkout page is displayed.

  From the Checkout page, you can return to the configuration page by clicking one of the Reconfigure options.
* In the Advanced System Configuration section, specify additional configuration options. For more information, see **[Advanced System Configuration](#adv-system-config)**.

*   Click the **Cloud Service terms** and the **Third-Party Service Agreement** check boxes.
*   Confirm or enter your payment information and click **Submit Order**. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

  You can also save this order without purchasing by clicking **Save as Quote**.

 A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page after you login to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

 ## Additional server configuration options
 {: #addl-server-options}

 You have additional options available to you when you're provisioning your bare metal server, for example public bandwidth, uplink port speeds, public secondary IP addresses, and more. Table 1 describes your additional options.
 
 | **Field** | **Description** |
 |-------------------|---------------|
 |Server security|Such as Trusted Execution Technology (Intel TXT)|||
 |Software Guard Extensions|Increased security for sensitive code and data (Intel SGX). <br><br>Refer to [Provisioning a bare metal server with Intel SGX](../bare-metal/bare-metal-provision-SGX.html).|
 |RAM|Choose a level of RAM that meets your server needs.|
 |Operating System |Select from CentOS, FreeBSD, Microsoft, Red Hat, Ubuntu, or Other. |
 |Hard Drives |Use the tool in the user interface set-up your hard disks by pre-filling the fields based on your OS selection. <br><br> You can also select to use an Intel Optane SSD drive. Refer to [Provisioning an Intel Optane SSD DC P4800X](../bare-metal/bm-provision_ssd.html).
 |Public Bandwidth |Determines the amount of data that can be transferred through the public interface during a month. For test environments, which need installation data to be transferred through this interface, values need to be adapted beyond the amount of data initially transferred. Consider the [{{site.data.keyword.cloud_notm}} Content Delivery Network](https://www.ibm.com/cloud/cdn) to ship an initial data load to one of the {{site.data.keyword.cloud_notm}} datacenters. Any {{site.data.keyword.baremetal_short}} can be upgraded to include unmetered (unlimited) bandwidth. All unmetered devices are on private, dedicated ports.|
 |Uplink Port Speeds |Determines the speed of internal and external interfaces. |
 |Public Secondary IP Addresses |Assigns more IP address to your server. Depending on your scenario, you may require further IP addresses assigned to your server. More IPv4 addresses are available in quantities of 1, 2, 4, 8, 16, or 32. |
 |Primary IPv6 Addresses |Assigned to your server's internal, as well as on external, interfaces. |
 |Public Static IPv6 Addresses |Assigns more IPv6 addresses from a /64 block. |
 |Operating System Addons|Select options such as VMware, backup solutions, control panel, database, Hardware & Software Firewalls, Anti-Virus & Spyware Protection, Intrusion Detection & Protection. <br><br>It is strongly recommended to align your corporate security department with {{site.data.keyword.cloud_notm}} Support to discuss the details of these options.
 |Evault |An agent-based backup tool that can be installed on your server to replicate backups between servers. |
 |Service addons|Select any service addons such as monitoring, automated response, and insurance.|
 {: caption="Table 1. Additional server options" caption-side="top"}

## Advanced System Configuration
{: #adv-system-config}

The fields under **Advanced System Configuration** complete your provisioning process. 

| **Field** | **Description** |
|---|---|
| Hostname | A permanent or temporary name for your server, for example, ```server1```. **Note**: If you're provisioning an SAP Certified Server, your SAP hostname must consist of a maximum of 13 alpha-numeric characters. For more information on SAP hostnames, see [SAP Notes 611361](https://launchpad.support.sap.com/#/notes/2611361) and [129997](https://launchpad.support.sap.com/#/notes/129997). Requires an SAP S-user ID. |
| Domain | Sub-domain name that should not collide with an internet domain name, for example, ```test.acme.com```. |
| VLAN Selection | If there is a VLAN under your account because you already ordered at least on server, you can add the new server to that VLAN. |
| Provisioning Script | You can provide a script that allows you to automate certain steps after provisioning. |
| SSH Keys | You can provide the public key of your SSH key, which will allow you to log in to your server after it's provisioned. |
{: caption="Table 2. Advanced System Configuration" caption-side="top"}

 Consult {{site.data.keyword.cloud_notm}} Support for further information.

 **NOTE:** You can order secondary subnets with your compute devices. However, if you order secondary subnets, they are reclaimed when the compute device is reclaimed. If you order the secondary subnet independently (not as an add-on option of a compute order), you can retain the subnet until you cancel it explicitly. This distinction is important to remember, so that you do not inadvertently lose some IP addresses if a compute device is reclaimed.

## Next Steps
After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
