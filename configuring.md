---



copyright:
  years: 2017
lastupdated: "2017-12-05"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuring your bare metal server

It's a good idea to take the time and make your configuration decisions ahead of provisioning your {{site.data.keyword.baremetal_long}}. It makes the provisioning process go faster and smoother. {:shortdesc}

## Determining the server's use and sizing it

Your first task is to determine how you're going to use your {{site.data.keyword.baremetal_short}}. For example, do you intend to use it for dev/test or production? Are you testing a user experience, processing lengthy algorithms, backing up and restoring data, or increasing latency speed?

After determining how your {{site.data.keyword.baremetal_short}} is to be used, you need to size it. The [SoftLayer Total Cost of Ownership Calculator](http://www.softlayer.com/tco/) can help determine what of {{site.data.keyword.baremetal_short}} best meets your needs.

## Selecting your server

{{site.data.keyword.cloud_notm}} offers seven fast-provision servers to make sure that you have the performance that you need for your workload. These servers are currently available in the United Kingdom and US South regions.

| **Configuration** | **Processor** | **Memory** | **Hard drive** | **Port speed** |
|-------------------|---------------|------------|----------------|----------------|
| Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 cores, 3.50 GHz) |32 GB RAM |1 internal hard disc drive |100 Mbps maximum port speed|
|Intel Xeon E5-2620 v3 |Dual Intel Xeon E5-2620 v3 (6 cores, 2.40 GHz) |64 GB RAM |2 internal hard disc drives |100 Mbps maximum port speed|
|Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 cores, 3.50 GHz) |32 GB RAM |2 internal hard disc drives |100 Mbps maximum port speed|
|Intel Xeon E5-2650 v3 |Dual Intel Xeon E5-2650 v3 (10 cores, 2.30 GHz) |128 GB RAM |1 internal hard disc drive |100 Mbps maximum port speed|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 cores, 2.60 GHz) |128 GB RAM |2 internal hard disc drives |100 Mbps maximum port speed|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 cores, 2.60 GHz) |64 GB RAM |4 internal hard disc drives |1,000 Mbps maximum port speed|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 cores, 2.60 GHz) |256 GB RAM |4 internal hard disc drives |1,000 Mbps maximum port speed|

In addition to the seven fast-provision servers, {{site.data.keyword.cloud_notm}} expanded its {{site.data.keyword.baremetal_short}} offering to include POWER8-based bare metal systems. These systems are built with the {{site.data.keyword.IBM_notm}} POWER8 processor and an OpenPOWER-based platform, which is tuned specifically for cloud-based deployments of data, cognitive, and web workloads on Linux.

Any {{site.data.keyword.baremetal_short}} can be upgraded to include unmetered (unlimited) bandwidth. All unmetered devices are on private, dedicated ports.

## Setting up your bare metal servers

After you select your datacenter, server, and billing option (monthly or hourly), you need to decide how to configure your server. Some fields (Server, RAM, Graphics Processing Unit, and Secondary Graphics Processing Unit) on the **Configure your {{site.data.keyword.baremetal_short}}** page will default based on your server selection. The following table describes the fields for which you can define a value.

| **Field** | **Description** | 
|-------------------|---------------|
|Operating System |Select from CentOS, FreeBSD, Microsoft, Red Hat, Unbuntu, or Other. |
|Hard Drives |The Disk Configuration tool helps you set up your hard disks by prefilling the fields based on your OS selection. |
|Public Bandwidth |Determines the amount of data that can be transferred through the publick interface during a month. For test environments, which need installation data transferred through this interface, values need to be adapted beyond the amount of data initially transferred. You may want to consider the [{{site.data.keyword.cloud_notm}} Content Delivery Network](https://www.ibm.com/cloud/cdn) to ship an initial data load to one of the {{site.data.keyword.cloud_notm}} datacenters. |
|Uplink Port Speeds |Determines the speed of internal and external interfaces. |
|Public Secondary IP Addresses |Assigns an additional IP address to your server. Depending on your scenario, you may require further IP addresses assigned to your server. Additional IPv4 addresses are available in quantities of 1, 2, 4, 8, 16, or 32. |
|Primary IPv6 Addresses |Assigned to your server's internal, as well as on external, interfaces. |
|Public Static IPv6 Addresses |Assigns additional IPv6 addresses from a /64 block. |
|Hardware & Software Firewalls, Anti-Virus & Spyware Protection, and Intrusion and Detection & Protection |Select the appropriate options if the server will be Internet facing. It is strongly recommended to align your corporate secruity department with {{site.data.keyword.cloud_notm}} Support to discuss the details of these options. |
|Evault |An agent-based backup tool that can be installed on your server to replicate backups between servers. |

Consult the [Design Decision Tool](http://knowledgelayer.softlayer.com/learning/softlayer-design-decision-tool) or {{site.data.keyword.cloud_notm}} Support for further information.


## Advanced System Configuration

Advanced system configuration is done after you click the **Add to Order** button and you're redirected to the Checkout page. The following table describes the fields under Advanced System Configuration.

| **Field** | **Description** | 
|-------------------|---------------|
|Hostname |A permanent or temporary name for your server, for example, _server1_. |
|Domain |Sub-domain name that should not collide with an Internet domain name, for example, _test.acme.com_. |
|VLAN Selection |If there is a VLAN under your account because you already ordered at least one server, you can add the new server to that VLAN. |
|Provisioning Script |You can provide a script that allows you to automate certain steps after the server has been provisioned. |
|SSH Keys |You can provide a public key for your SSH key, which will allow you to log in to your server after it's provisioned. |
