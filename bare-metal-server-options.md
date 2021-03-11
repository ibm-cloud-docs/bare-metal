---

copyright:
  years: 2016, 2021
lastupdated: "2021-03-10"

keywords: bare metal, bare metal servers, SAP-certified, {{site.data.keyword.baremetal_long}}, {{site.data.keyword.baremetal_short}}, available bare metal, cascade lake, amd EPYC, amd, Rome

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

### SAP-certified bare metal servers
{: #bm-SAP-cert}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} are certified to support your SAP HANA and SAP NetWeaver workloads. For more information, see [SAP-certified infrastructure](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}.

 ### VMware-certified servers
{: #vmware-certified-servers}

{{site.data.keyword.BluSoftlayer_full}} provides the unique capability for you to provision dedicated {{site.data.keyword.baremetal_short}} so you can deploy your own VMware-based private cloud. For more information, see [Getting started with VMware](/docs/vmware?topic=vmware-vmware-getting-started).

## Available options for bare metal servers
{: #options-for-bare-metal-servers}
{{site.data.keyword.cloud_notm}} has {{site.data.keyword.baremetal_short}} options that you can customize to fit your needs.

### AMD CPU support
{: #bm-amd-procs}

When you provision a bare metal server, AMD EPYC "Rome" generation CPUs are now an option. Rome generation processors are high-performance multiprocessors that are based on AMD's Zen 2 architecture. The EPYC "Rome" family offers several CPU options that offer up to 48 cores per socket.  

You can choose from the following AMD EPYC "Rome" CPUs:
* AMD EPYC 7642 (48-core, 2.3 Ghz)
* AMD EPYC 7F72 (48-core, 3.2 Ghz)

The following operating systems are supported by 7642 AMD EPYC "Rome" CPUs:
* RHEL 7
* Ubuntu 18.04
* CentOS 7.6
* Microsoft Server 2019/2016

Systems must be started in UEFI mode.
{: note}

EPYC processors are available in select data centers.
{: important}

### Intel Cascade Lake CPU support
{: #bm-cascade-lake-support}

You can choose from the following Intel Cascade Lake CPUs when you provision a bare metal server:

| Cascade Lake CPUs | Specifications |
|-----|-----|
| Intel Xeon 4210 | 10-Core, 2.2 GHz, 85 W |
| Intel Xeon 5218 | 16-Core, 2.3 GHz, 125 W |
| Intel Xeon 6248 | 20-Core, 2.6 GHz, 150 W |
| Intel Xeon 6250 | 8-Core, 3.9 GHz, 185 W |
{: caption="Table 1. Cascade Lake CPU options" caption-side="top"}

### NVIDIA GPU support
{: #bm-gpu-support}

For certain bare metal servers, you can add the processing power of NVIDIA GPUs. When you select a bare metal server, look for **GPU** in the **Features** column on the provisioning page. You will need to install the appropriate drivers. See [NVIDIA drivers ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.nvidia.com/Download/index.aspx?lang=en-us){: new_window}

### Dynamic inventory
{: #bm-dynamic-inv}

You can now see what servers are available in what data center when you provision a bare metal server. If a server is not available in the data center you selected, hover over the server name. A list is displayed that indicates the data centers in which the server is available. For more information about provisioning a bare metal server, see [Selecting from fast provisioning servers](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers).

### Network redundancy
{: #bm-network-redundancy}
 
Port redundancy provides networking failover by maintaining a primary and secondary network port. If the primary port fails, the secondary (redundant) port enables.

Only one port is active at a time.
{: note}

The following network redunancy options are availble for bare metal servers.

| Redundancy options | Description |
| ---- | ----|
| Automatic redundancy (Recommended option) | Automatically configures the redundant ports for interface teaming through LACP (Link Aggregation Control Protocol) to preserve connectivity during routine maintenance. |
| User-managed redundancy | Must have interface teaming configured on the host operating system to use network redundancy. Without interface teaming, connectivity during routine maintenance is not preserved. |
| No redundancy | This is the only option for legacy data centers that don’t support automatic redundancy. This option is not recommended in a new data center.|
| Interface teaming (link aggregation)| Combines, in parallel, multiple network connections to provide redundancy and increase network throughput. |
{: caption="Table 2. Network redunancy options" caption-side="top"}

VMWare requires user-managed links.
{: tip}

For more information about network options, see [Network options](/docs/bare-metal?topic=bare-metal-network-options).

### Block and file storage add-on
{: #bm-block-and-file-add-on}

If you need extra storage, {{site.data.keyword.IBM_notm}} makes it easy! You can now order block and file storage (20 - 12,000 GB) when you provision a bare metal server.

Your add-on storage isn't automatically connected to your bare metal server. You need to connect the add-on storage to your bare metal server after your server provisions.
{: note}

For more information about block and file storage, see the following links.
* [About block storage](/docs/BlockStorage?topic=BlockStorage-About)
* [About file storage](/docs/FileStorage?topic=FileStorage-about)
