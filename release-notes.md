---

copyright:
  years: 2019, 2022

lastupdated: "2021-12-09"

keywords: bare metal release notes

subcollection: bare-metal

content-type: release-note

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:preview: .preview}
{:note: .note}
{:important: .important}
{:download: .download}
{:external: target="_blank" .external}
{:release-note: data-hd-content-type='release-note'}

# Release notes for {{site.data.keyword.baremetal_long}}
{: #release-notes}

Use the release notes to learn the latest updates to {{site.data.keyword.baremetal_long}} that are grouped by date.
{: shortdesc}

## December 2021
{: #subcollection-dec21}

### 02 December 2021
{: #subcollection-dec0221}
{: release-note}

**Custom image template add-ons**
:    Custom image templates now support the following add-ons. For more information, see the supported add-ons section in [About bare metal custom image templates](/docs/bare-metal?topic=bare-metal-getting-started-bm-custom-image-templates#bm-image-template-supported-addons).

     - McAfee (free license add-on)
     - MySQL (free license add-on)
     - Microsoft SQL Server
     - R1Soft client
     
:    You can now migrate a bare metal server by using add-on software such as cPanel, MS SQL Server, Plesk, or R1Soft Backup Agent. For more information, see [Migrating bare metal servers with add-on software](/docs/bare-metal?topic=bare-metal-bm-migrate-with-add-on-software).

## October 2021
{: #subcollection-oct21}

### 05 October 2021
{: #subcollection-oct0521}
{: release-note}

**Intel Xeon 8260 CPU**
:   You can now select the Intel Xeon 8260 CPU when you provision a bare metal server. For more information, see [Bare metal server options](/docs/bare-metal?topic=bare-metal-about-bm#bm-cascade-lake-support).

## February 2021
{: #subcollection-feb21}

### 01 February 2020
{: #subcollection-feb0121}
{: release-note}

**25 Gbps port space is now available**
:   You can now use 25 Gbps port speed on select Cascade Lake processor servers. For more information about 25 Gbps port speed, see the 25 Gbps port speed section of the Bare Metal Servers [Network options](https://test.cloud.ibm.com/docs/bare-metal?topic=bare-metal-network-options#25-gbps-port-speed) topic.

## Aug 2020
{: #subcollection-aug20}

### 12 August 2020
{: #subcollection-aug1220}
{: release-note}

**Intel Xeon 6250 CPU**
:   You can now select the Intel Xeon 6250 CPU when you provision a bare metal server. For more information, see [Bare metal server options](/docs/bare-metal?topic=bare-metal-about-bm#bm-cascade-lake-support).

### 10 August 2020
{: #subcollection-aug1020}
{: release-note}

**Custom images templates now available**
:   Image templates provide an imaging option for {{site.data.keyword.baremetal_long}}. With {{site.data.keyword.baremetal_short}} custom image templates, you can capture an image of a bare metal server to replicate its configuration with minimal changes in the order process. For more information, see [About bare metal custom image templates](/docs/bare-metal?topic=bare-metal-getting-started-bm-custom-image-templates).

## July 2020
{: #subcollection-jul20}

### 22 July 2020
{: #subcollection-jul2220}
{: release-note}

**IBM Cloud Monitoring**
:   {{site.data.keyword.mon_full_notm}} collects basic classic infrastructure and VPC virtual server instance metrics such as CPU usage, disk usage, network traffic, and memory. These metrics are stored in {{site.data.keyword.mon_full_notm}}. For more information, see [IBM Cloud Monitoring](/docs/cloud-infrastructure?topic=cloud-infrastructure-monitoring-iaas).

## May 2020
{: #subcollection-may20}

### 18 May 2020
{: #subcollection-may1820}
{: release-note}

**NVM solid-state drives**
:   Non-Volatile Memory Express (NVMe) is a high-performance storage protocol that supports direct connection of the memory subsystem to the CPU via the PCIe interface. The NVMe protocol capitalizes on parallel, low latency data paths to the underlying media. This protocol offers significantly higher performance and lower latencies compared to legacy SAS and SATA protocols. For more information, see [NVMe solid-state drives](/docs/bare-metal?topic=bare-metal-ordering-nvme-ssd).

## March 2020
{: #subcollection-mar20}

### 24 March 2020
{: #subcollection-mar2420}
{: release-note}

**AMD CPU support**
:   When you provision a bare metal server, AMD EPYC® "Rome" generation CPUs are now an option. Rome generation processors are high-performance multiprocessors that are based on AMD's Zen 2 architecture. The EPYC "Rome" family offers several CPU options that offer up to 48 cores per socket. For more information, see the AMD CPU support section in [Bare metal server options](/docs/bare-metal?topic=bare-metal-about-bm#bm-amd-procs).

## February 2020
{: #subcollection-feb20}

### 11 February 2020
{: #subcollection-feb1120}
{: release-note}

**Veeam backup for Office 365**
:   Veeam backup for Office 365 protects your Office 365 data by backing up your Exchange Online, SharePoint Online, and OneDrive for Business data. True data protection and RPO (recovery point objective) are not included with Office 365. Veeam provides a software defined solution that protects Office 365, performs granular restores, and recovers data to anywhere. For more information, [Veeam backup for Office 365](/docs/bare-metal?topic=bare-metal-veeam-backup-for-office-365).

## October 2019
{: #subcollection-oct19}

### 10 October 2019
{: #subcollection-oct1019}
{: release-note}

**Network port redundancy**
:   Port redundancy provides networking failover by maintaining a primary and secondary network port. If the primary port fails, the secondary (redundant) port enables. For more information, see the netword redundancy section of [Bare metal server options](/docs/bare-metal?topic=bare-metal-about-bm#bm-network-redundancy).

## August 2019
{: #subcollection-aug19}

### 05 August 2019
{: #subcollection-aug0519}
{: release-note}

**NVIDIA GPU support**
:   For certain bare metal servers, you can add the processing power of NVIDIA&reg; GPUs. When you select a bare metal server, look for GPU in the Features column on the provisioning page. For more information, see the NVIDIA GPU support section of [Bare metal server options](/docs/bare-metal?topic=bare-metal-about-bm#bm-gpu-support).

## April 2019
{: #subcollection-apr19}

### 02 April 2019
{: #subcollection-apr0219}
{: release-note}

**Cascade Lake CPU support**
:   You can choose from the following Intel® Xeon® Cascade Lake CPUs when you provision a bare metal server. For more information, see the Intel Cascade Lake CPU support section of [Bare metal server options](/docs/bare-metal?topic=bare-metal-about-bm#bm-cascade-lake-support).

## March 2019
{: #subcollection-mar19}

### 25 March 2019
{: #subcollection-mar2519}
{: release-note}

**Contract term pricing**
:   {{site.data.keyword.baremetal_long}} gives you the option to lock-in a lower price by signing a contract term. You choose between either a 1-year or a 3-year contract. A contact term bare metal server is a great option if you know that you need hardware for the long term and makes sure that your resources are available throughout your term. When your term is over, you keep your contracted price on a month-to-month basis. For more information, see [Contract term pricing for bare metal servers](/docs/bare-metal?topic=bare-metal-about-reserved-bare-metal-servers).

## April 2018
{: #subcollection-apr18}

### 05 April 2018
{: #subcollection-apr0518}
{: release-note}

**Spare pools**
:   The Spare Pool screen in the {{site.data.keyword.cloud}} allows users to manage the spare pool of devices associated with the account. Each device in the spare pool can be used as a backup device if more devices are needed. For more information, see [Spare pools](/docs/bare-metal?topic=bare-metal-bm-about-spare-pools).

## March 2018
{: #subcollection-mar18}

### 26 March 2018
{: #subcollection-mar2618}
{: release-note}

**Intel Software Guard Extension**
:   Intel® Software Guard Extension (SGX) is an architecture extension that is designed to increase security by using protected areas in memory that runs your sensitive code and data. For more information, see [Intel Software Guard Extension](/docs/bare-metal?topic=bare-metal-bm-intel-sgx).

### 16 March 2018
{: #subcollection-mar1618}
{: release-note}

**Block and file storage add-on**
:   If you need extra storage, {{site.data.keyword.IBM_notm}} makes it easy! You can now order block and file storage (20 - 12,000 GB) when you provision a bare metal server. Your add-on storage isn't automatically connected to your bare metal server. You need to connect the add-on storage to your bare metal server after your server provisions. For more information, see the block and file storage add-on section of [Bare metal server options](/docs/bare-metal?topic=bare-metal-about-bm#bm-block-and-file-add-on).

### 02 March 2018
{: #subcollection-mar0218}
{: release-note}

**Custom bare metal servers**
:   {{site.data.keyword.baremetal_long}} are single-tenant physical servers that provide you performance and control with low-level access to the hardware resources. You can create a custom {{site.data.keyword.baremetal_long}}. For more information, see [Building a custom Bare Metal Server](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server).
