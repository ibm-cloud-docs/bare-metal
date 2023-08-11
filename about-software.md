---
copyright:
  years: 2017, 2023
lastupdated: "2023-08-11"

keywords: software, supported operationg systems, oses, os supported, operating system support, classic os, classic operating system

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# About software
{: #about-software}

{{site.data.keyword.BluSoftlayer_full}} has strategic relationships with vendors to provide month-to-month licenses on 32-bit and 64-bit compatible software. When you order a device, you select the type of operating system and software for your device. You can add more software to your device within the {{site.data.keyword.slportal_full}} and change to another operating system by reloading the OS on your existing device. The IBM automated system provisions software onto your server by following best practice guidelines of each vendor to make sure that you have maximum stability and availability.

See [{{site.data.keyword.BluSoftlayer_full}} software solutions](https://cloud.ibm.com/catalog#software){: external} for a complete list of {{site.data.keyword.BluSoftlayer_full}} supported software.

Not all software options are available for all server types and not all software options are the same for monthly and hourly billing.
{: note}

If you need software that isn't supported, use your root access to the server to install and configure your own version of that software. To return to a supported version on your device, reload the OS.

IBM includes instructions or considerations for using products in the {{site.data.keyword.BluSoftlayer_notm}} environment. For more information about specific software, see the vendor-specific software documentation.

## Anti-virus, Adaptive Threat Protection (ATP), ENS Firewall, ENS Threat Prevention, ENS Web Control
{: #anti-virus-spyware-and-host-ids-information}

IBM offers Trellix solutions for anti-virus, Adaptive Threat Protection (ATP), ENS Firewall, ENS Threat Prevention, ENS Web Control on Windows&reg; devices. You can get protection for Windows for a monthly fee.

You can manage your Trellix offerings from your server. IBM does not manage Trellix offerings on your server.

## Supported operating systems for {{site.data.keyword.BluSoftlayer_full}} server software
{: #supported-operating-systems-for-ibm-cloud-servers}

{{site.data.keyword.BluSoftlayer_full}} server software supports the following operating systems.

Boot disk sizes vary by operating system: Linux OS supports 25 GB and 100 GB. Windows supports only 100 GB.
{: note}

| Operating system | Version |
| --- | --- |
| CentOS | 8.x  \n 7.x  \n |
| Debian | 11.x  \n 10.x |
| Microsoft Windows | 2022 Standard  \n 2019 Standard  \n 2016 Standard  \n 2012 R2 Standard  \n 2012 Standard |
| Red Hat | 9.x  \n 8.x  \n 7.x |
| Rocky Linux | 8.x |
| Ubuntu | 20.04  \n 22.04 |
{: caption="Table 1. {{site.data.keyword.baremetal_short}} supported operating systems" caption-side='top"}
{: #virtual-servers-oses}
{: tab-title="Virtual servers"}
{: tab-group="operating-systems"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the hardware class."}

| Operating system | Version |
| --- | --- |
| CentOS | 7.x |
| Citrix | 8.2 |
| Debian | 11.x  \n 10.x |
| Microsoft Windows | 2022 Datacenter  \n 2022 Standard  \n 2019 Datacenter  \n 2019 Standard  \n 2016 Datacenter  \n 2016 Standard  \n 2012 R2 Standard  \n 2012 Datacenter  \n 2012 Standard |
| OSNEXUS | 5.x (4 TB)  \n 5.x (16 TB)  \n 5.x (48 TB) |
| Red Hat | 9.x  \n 8.x.  \n 7.x |
| Rocky Linux | 8.x |
| VMWare | ESXi 7.0u3i (Cascade Lake only) | 7.0 Update 2  \n 7.0 Update 1.  \n 6.7 Update 3  \n 6.5 Update 3  \n 6.5 Update 2 |
| vSphere | 7.0 |
| Unbuntu | 22.04  \n 20.04  |
| SUSE Linux Enterprise Server (SLES) | 15 SP2  \n 15 SP1  \n 12 SP5  \n 12 SP4  \n 12 SP3 |
{: caption="Table 1. {{site.data.keyword.baremetal_short}} supported operating systems" caption-side='top"}
{: #bare-metal-oses}
{: tab-title="Bare metal servers"}
{: tab-group="operating-systems"}
{: class="simple-tab-table"}
{: summary="Use the buttons before the table to change the context of the table. The column headers identify the hardware class."}

CentOS 8, Debian 10, and RHEL 8 and 9 don't support "Add on" software configurations. These operating systems also don't support the **Provision script** and **User data** selections for server configuration options. If you're migrating from a server that has "Add on" software configurations, you can choose to migrate to an earlier version.
{: important}

For more information about paravirtualized (PV) and hardware virtual machine (HVM) boot modes, see the following links:

* [PV](/docs/overview?topic=overview-glossary#x9736806){: external}
* [HVM](/docs/overview?topic=overview-glossary#x9736811){: external}
