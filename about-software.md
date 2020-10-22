---
copyright:
  years: 2017, 2020
lastupdated: "2020-10-15"

keywords: software

subcollection: bare-metal
---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}
{:important: .important}

# About software
{: #about-software}

{{site.data.keyword.BluSoftlayer_full}} has strategic relationships with vendors to provide month-to-month licenses on 32-bit and 64-bit compatible software. When you order a device, you select the type of operating system and software for your device. You can add more software to your device within the {{site.data.keyword.slportal_full}} and change to another operating system by reloading the OS on your existing device. The IBM automated system provisions software onto your server by following best practice guidelines of each vendor to make sure that you have maximum stability and availability.

See the following list for currently supported software: [{{site.data.keyword.BluSoftlayer_full}} software solutions](https://cloud.ibm.com/catalog#software){: external}.

Not all software options are available for all server types and not all software options are the same for monthly and hourly billing.
{: note}

If you need software that is not currently supported, use your root access to the server to install and configure your own version of that software.  To return to a supported version on your device, reload the OS.

IBM includes instructions or considerations for using products in the {{site.data.keyword.BluSoftlayer_notm}} environment. For software documentation, see the documentation of the vendor who produces the software.

## Anti-Virus, Spyware, and host IDs information
{: #anti-virus-spyware-and-host-ids-information}

IBM offers multiple solutions for both Anti-Virus, Spyware, and host ID protection on every device. Anti-Virus and Spyware products are provided by McAfee. You can get a standard, free solution for Windows. You can also get a Total Protection for Windows for a monthly fee.

You must add Anti-Virus, Spyware, and host ID solutions to your device for it to be protected. You can manage these solutions in the IBM Customer Portal.

## Supported operating systems for IBM Cloud virtual servers
{: #supported-operating-systems-for-ibm-cloud-virtual-servers}

IBM Cloud virtual servers support the following operating systems.

- Cent OS 6 (PV)
- Cent OS 7 (HVM)
- Cent OS 8 (HVM)*
- Debian 8 (HVM)
- Debian 9 (HVM)
- Debian 10 (HVM)*
- RHEL 6 (PV)
- RHEL 7 (HVM)
- RHEL 8 (HVM)*
- Ubuntu 16 (PV/HVM) defaults to PV boot mode, but you can to toggle to HVM boot mode
- Ubuntu 18 (PV/HVM) defaults to PV boot mode, but you can to toggle to HVM boot mode
- Windows 2012 (HVM)
- Windows 2012 R2 (HVM)
- Windows 2016 (HVM)
- Windows 2019 (HVM)

Cent OS 8, Debian 10, and RHEL 8 don't support "Add On" software configurations. These OSs also don't support the **Provision script** and **User data** selections for virtual server configuration options. If you are migrating from a server that has "Add On" software configurations, you can choose migrate to an earlier version.
{: important}

Boot disk sizes vary by operating system: Linux OS supports 25 GB and 100 GB. Windows supports only 100 GB.
{: note}

For more information about toggling between PV and HVM boot modes, see the following links:
* [Virtual guest supported boot modes ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://sldn.softlayer.com/reference/services/SoftLayer_Virtual_Guest_Block_Device_Template_Group/getSupportedBootModes){: new_window}
* [Add boot mode option ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://github.com/softlayer/softlayer-python/pull/936/files/09c35a9595651d66f3e117a055efe585745ba2b3){: new_window}
