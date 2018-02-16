---



copyright:
  years: 2017, 2018
lastupdated: "2018-02-09"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning an Intel Optane SSD DC P4800X
{: #ordering-ssd}

Intel® Optane™ SSD DC P4800X combines the attributes of storage and memory to create a new storage tier. The unique solution is achieved through an industry-leading combination of high throughput, low latency, high QoS and ultra-high endurance.

Key features include:

* Ultra-low latencies for reads and writes
* Consistently reliable Quality of Service (QoS)
* Excellent read and write performance at low queue depths
* Near symmetrical read and writer performance
* Very high endurance
* Variable sector size and end-to-end path protection
* Enhanced power-loss date protection
* Power loss capacitor self-test
* Out of band management (future)
* Thermal throttling and monitoring
* Self-Monitoring, Analysis and Reporting Technology (SMART) health reporting

The primary use cases for the Intel® Optane™ SSD DC-4800X include:

* Fast storage or cache. Optane SSDs offer the performance necessary to enable a new, higher performance cache or tier. They also offer the ultimate latency for use as direct attach storage for the most demanding applications or services. For these applications, Optane SSDs will vastly accelerate performance, breaking storage bottlenecks, improve workload scaling and reduce the total cost for deployments.
* Extended memory. The unique latency and Quality of Service (QoS) characteristics allow the SSD to be well suited as a memory device. The ability to use a larger capacity and lower cost device, as compared to dynamic RAM (DRAM), will help in the following ways:
    *  Facilitate opportunities to save money by replacing some of the DRAM set  
    *  Gain new insights by growing data set sizes and complexity by augmenting DRAM to grow into significantly larger memory pools

Note: The extended memory capability will not be available at launch. Scheduled availability is to be determined.
For more information about Intel® Optane™ SSD DC P4800X, see https://www.intel.com/content/www/us/en/solid-state-drives/optane-ssd-dc-p4800x-brief.html.

The 375GB drive is available in the following datacenters:

|  Supported datacenter     |   
| ------------------------- |  
| DAL10                     |
| WDC04                     |
| SJC03                     |
| LON02                     |
| MEL01                     |
{: caption="Table 1. Supported datacenters" caption-side="top"}

Operating system (OS) specifications are as follows:
Intel-provided driver (full production specification is guaranteed, booting is only supported for 64-bit OS)

  * Windows Server 2016
  * Windows Server 2012 R2
  * VMware ESXi 5.5 and 6.0

In-box driver (with an open-source non-Intel driver, compatibility and functionality is validated)

  * Red Hat Enterprise Linux (RHEL) 6.7, 6.8, 7.0, 7.1, 7.2, 7.3
  * Windows Server 2016

Ordering notes:

You can either order an Intel® Optane™ SSD DC P4800X disk OR a GPU for your server; not both.
Extended memory will be available at a future-to-be-determined date.

You have two options on how to provision an Intel® Optane™ SSD DC P4800X. The first is through the {{site.data.keyword.Bluemix}} catalog and the second is through the {{site.data.keyword.slportal_full}}. The catalog and {{site.data.keyword.slportal}} require unique log-in IDs. Your catalog user name and password won’t work for logging in to the portal and vice versa. See [Signing up for {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-bluemix){: new_window}  to set up either your {{site.data.keyword.Bluemix_notm}} catalog or {{site.data.keyword.slportal}} credentials.
{:shortdesc}

## Log into the IBM Cloud Catalog
Use the following steps to log in to the {{site.data.keyword.Bluemix_notm}} catalog to begin provisioning your dedicated hosts and dedicated host instances.

1. Open a new browser window and enter [https://console.bluemix.net/catalog/](https://console.ng.bluemix.net/catalog/){: new_window}.
2.	Click the **Log in** link (upper-right corner).
3.	Enter your email or IBMid and click **Continue**.
4.	Enter your Password and click **Log in**.
5.	Select **Infrastructure > Compute**.
6.  Click the **Bare Metal Server** tile.
7.  Click **Create**.

You will be on the main page of the {{site.data.keyword.slportal}}.

## Log in to the Customer Portal
Use the following steps to log in to the {{site.data.keyword.slportal}} to begin the order for your dedicated hosts and dedicated host instances.

1.	Open a new browser window and enter [https://control.softlayer.com](https://control.softlayer.com){: new_window}.
2.	Enter your Username and Password, and click **Log In** OR click **Log in with IBMid**.
3.	Enter your email or IBMid and click **Continue**.
4.	Enter your Password and click **Log In**.

You will be on the main page of the {{site.data.keyword.slportal}}.

## Provision your Intel® Optane™ SSD DC P4800X disk
Use the following steps to your server with an Intel® Optane™ SSD DC P4800X disk.

1.	Click the **Devices** icon.
2.  Click on either the **Bare Metal Server Hourly** or **Bare Metal Server Monthly** link.

You’re taken to the *Configure your Cloud Server* page.

3. Scroll down to *Dual Core Multi-Core Servers* and select your server by clicking on the link under *Starting Price Per Month*.
4. Enter the following information:

|              Field        |  Description                |
| ------------------------- | --------------------------- |
|Quantity                   | Defaults to 1               |
|Data Center                | Select the IBM® Cloud Data Center where you want your server to be provisioned. |
|Server                     | Defaults based on your selection from the prior page.            |
|RAM                        |                             |
|Operating system           | Select from Microsoft, Red Hat, or VMware.  Options will display based on the OS you select.|
|NVMe PCIe drives           | Select the drive that will best fit your work load needs. Note that if you select a drive, the Hard Drive selection will grey out. |
| Hard drive                | Select the drive that will best fit your work load needs. Note that if you select a drive, the NVMe PCIe section will be greyed out. |
{: caption="Table 2. Deployment options" caption-side="top"}

5. Scroll to the options and make selections based on how you will be using your server(s). Listed below are some that you will want to consider when setting up your server(s).

|              Field        |  Description                |
| ------------------------- | --------------------------- |
|Public Bandwidth           | Determines the total amount of data that can be transferred through the public interface during a month. For test environments, which need their installation data transferred through this interface, values need to be adapted beyond the amount of data initially transferred. You may want to consider the Bluemix Content Delivery Network (CDN) (https://www.ibm.com/cloud-computing/bluemix/content-delivery-network) to ship an initial data load to one of IBM Cloud’s data centers.|
|Upling Port Speeds | Determines the speed of internal and external interfaces. |
|Public Secondary IP Addresses | Assigns additional IP addresses to your server(s). Depending on your scenario, you may require further IP addresses assigned to your server(s). Additional IPv4 addresses are available in quantities of 1, 2, 4, 8, 16 or 32.|
|Primary IPv6 Addresses      | Assigned to your server’s internal as well as on external interfaces.|
|Public Static IPv6 Addresses | Assigns additional IPv6 addresses from a /64 block for Primary IPv6 Addresses.|
|Hardware & Software Firewalls, Anti-Virus & Spyware Protection, and Intrusion Detection & Protection          | Select the appropriate options if the server will be Internet facing. It is strongly recommended to align your corporate security department with Bluemix support to discuss the details of these options. |
| Redundant Power Supply     |  |
| eVault                     | An agent-based backup tool can be installed on your server to replicate backups between servers. |
{: caption="Table 3. Deployment options" caption-side="top"}

6. Click *Add to Order* and you’ll be directed to the Checkout page once your order is verified.
7. Scroll down the Checkout page and enter the following values under Advanced System Configuration.

|              Field        |  Description                |
| ------------------------- | --------------------------- |
|Host name                  | A permanent or temporary name for your server, for example, server1.                           |
|Domain                     | Sub-domain name that should not collide with an Internet domain name, for example, test.acme.com. |
|VLAN selection             | If there is a VLAN under your account (in other words, you already ordered at least one server) you can add the new server to that VLAN.                            |
|Provision script      | You can provide a script that allows you to automate certain steps after provisioning.|
|SSH Keys | You can provide a public key for your SSH key, which will allow you to log in to your server after it’s provisioned.|
{: caption="Table 4. Advanced system configuration" caption-side="top"}

Your Order Summary displays on the right side of the *Configuration* page.

8. Click the *Cloud Service Terms* checkbox and, if applicable, click the *3rd Party Software Terms* checkbox.
9. Scroll down to Create Account: Enter Billing and enter the *Payment Type*, *Name*, *Card information* and *Expiration date* for the credit card to be used for billing.
10. Click *Submit Order*.

A confirmation email with the subject Your IBM Cloud Order ## has been approved will be sent to the email address in your profile. This email is notice that your server has been approved and is in the process of being provisioned.

## Next Steps
Once it’s provisioned, another notice will be sent notifying you that the server is available and can be managed through control.softlayer.com. For more information about managing a bare metal server, see [Managing your bare metal server](../bare-metal/managing.html).
