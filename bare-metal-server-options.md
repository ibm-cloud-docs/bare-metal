---

copyright:
  years: 2016, 2019
lastupdated: "2019-10-22"

keywords: bare metal, bare metal servers, POWER8, SAP-certified, {{site.data.keyword.baremetal_long}}, {{site.data.keyword.baremetal_short}}, available bare metal, cascade lake

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:note: .note}
{:tip: .tip}

# Bare metal server options
{: #about-bm}
Your {{site.data.keyword.baremetal_short}} is an hourly or monthly, single-tenant server that is dedicated to you; it is not shared in any part, including server resources, with other customers. You manage your server, which is provisioned without a hypervisor, and deployed in one or more data centers. Multiple {{site.data.keyword.baremetal_short}} can communicate on the {{site.data.keyword.cloud_notm}} virtual private network as if stationed on the same rack.

## Servers for every workload
{: #servers-every-need}

{{site.data.keyword.cloud_notm}} has {{site.data.keyword.baremetal_short}} to fit every workload. For more information, see [Bare Metal Servers](https://www.ibm.com/cloud/bare-metal-servers){: external}

### Fast provisioning servers
{: #Popular-bm}

{{site.data.keyword.cloud_notm}} offers preconfigured servers that meet the needs of most use cases. These servers are considered "fast provision" because your compute options (number of cores, speed, RAM, and number of drives) are preset. Preset servers are ready to configure 30 - 40 minutes after provisioning.

### Custom-based servers
{: #custom-based-bm}

If one of the fast provisioning servers don't meet your workload needs, you can customize your {{site.data.keyword.baremetal_short}} to meet your needs. Customized servers are provisioned in 2 - 4 hours and offer a greater variety of cores, speeds, RAM, and drives.

### Custom POWER8-based servers
{: #bm-power8}

{{site.data.keyword.cloud_notm}} offers you the option to provision an IBM POWER8-based bare metal server. POWER8 servers are built with the POWER8 processor and an OpenPower-based platform, which is tuned specifically for cloud-based deployments for data, cognitive, and web workloads on Linux. For more information, see [POWER8 Servers](https://www.ibm.com/cloud/bare-metal-servers/power){: external}.

### SAP-certified bare metal servers
{: #bm-SAP-cert}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} are certified to support your SAP HANA and SAP NetWeaver workloads. For more information, see [SAP-certified infrastructure](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}.

## Available options for bare metal servers <!--test new section - test as each option goes GA-->
{: #options-for-bare-metal-servers}
{{site.data.keyword.cloud_notm}} has {{site.data.keyword.baremetal_short}} options that you can customize to fit your needs.

### Intel Cascade Lake CPU support
<!--Need to add which servers are also available for SAP once the certification is done-->
You can now choose from the following Intel Cascade Lake CPUs when you provision a bare metal server:

* Intel Xeon 4210 (10-Core, 2.2 GHz, 85 W)
* Intel Xeon 5218 (16-Core, 2.3 GHz, 125 W)
* Intel Xeon 6248 (20-Core, 2.6 GHz, 150 W)

### Dynamic inventory
{: #bm-dynamic-inv}

You can now see what servers are available in what data center when you provision a bare metal server. If a server is not available in the data center you selected, hover over the server name. A list is displayed that indicates the data centers in which the server is available. For more information about provisioning a bare metal server, see [Selecting from fast provisioning servers](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers).

### Network redundancy 

**Port redundancy** provides networking failover by maintaining a primary and secondary network port. If the primary port fails, the secondary (redundant) port enables. 

Only one port is active at a time. 
{:note}

For more information about network options, see [Network options](https://test.cloud.ibm.com/docs/bare-metal?topic=bare-metal-network-options).

**Automatic redundancy (Recommended)** automatically configures the redundant ports for interface teaming through LACP (Link Aggregation Control Protocol) to preserve connectivity during routine maintenance.

**User-managed redundancy** must have interface teaming configured on the host operating system to use network redundancy. Without interface teaming, connectivity during routine maintenance is not preserved.

VMWare requires user-managed links.
{:tip}

**No redundancy** is not recommended in a new data center.

In legacy data centers that don’t support automatic redundancy, no redundancy is the only option.
{:note}

**Interface teaming** or link aggregation combines, in parallel, multiple network connections to provide redundancy and increase network throughput.

### Block and file storage add-on
{: #bm-block-and-file-add-on}

If you need extra storage, {{site.data.keyword.IBM_notm}} makes it easy! You can now order block and file storage (20 - 12,000 GB) when you provision a bare metal server.

Your add-on storage isn't automatically connected to your bare metal server. You need to connect the add-on storage to your bare metal server after your server provisions.
{: note}

<!--The add-on storage shares the data center that your bare metal server is on.-->

For more information about block and file storage, see the following links.
* [About block storage](/docs/infrastructure/BlockStorage?topic=BlockStorage-About)
* [About file storage](/docs/infrastructure/FileStorage?topic=FileStorage-about)
