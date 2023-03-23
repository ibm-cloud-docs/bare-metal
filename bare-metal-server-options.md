---

copyright:
  years: 2016, 2023
lastupdated: "2023-03-23"

keywords:

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Bare metal server options
{: #about-bm}

Your {{site.data.keyword.cloud}} bare metal server is an hourly or monthly, single-tenant server that is dedicated to you. Your server isn't shared in any part, including server resources, with other customers. You manage your server, which is provisioned without a hypervisor, and deployed in one or more data centers. Multiple {{site.data.keyword.baremetal_short}} can communicate on the {{site.data.keyword.cloud_notm}} virtual private network as if stationed on the same rack.

## Servers for every workload
{: #servers-every-need}

{{site.data.keyword.cloud_notm}} has {{site.data.keyword.baremetal_short}} to fit every workload. For more information, see [Bare metal servers](https://www.ibm.com/cloud/bare-metal-servers){: external}.

### Fast provisioning servers
{: #Popular-bm}

{{site.data.keyword.cloud_notm}} offers preconfigured servers that meet the needs of most use cases. These servers are considered "fast provision" because your compute options (number of cores, speed, RAM, and number of drives) are preset. Preset servers are ready to configure 30 - 40 minutes after provisioning.

### Custom-based servers
{: #custom-based-bm}

If one of the fast provisioning servers don't meet your workload needs, you can customize your {{site.data.keyword.baremetal_short}} to meet your needs. Customized servers are generally provisioned in 2 - 4 hours. The provisioning time depends on complexity, quantity, and testing options.

### SAP-certified bare metal servers
{: #bm-SAP-cert}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} are certified to support your SAP HANA and SAP NetWeaver workloads. For more information, see [SAP-certified infrastructure](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}.

### VMware-certified servers
{: #vmware-certified-servers}

{{site.data.keyword.BluSoftlayer_full}} provides the unique capability for you to provision dedicated {{site.data.keyword.baremetal_short}} so you can deploy your own VMware&reg;-based private cloud. For more information, see [Getting started with VMware](/docs/vmware?topic=vmware-vmware-getting-started).

## Advanced hardware options
{: #options-for-bare-metal-servers}

{{site.data.keyword.cloud_notm}} offers advanced hardware options to fit your workload needs.

### Intel Sapphire Rapids CPUs
{: #bm-sapphire-rapids-support}

Sapphire Rapids processors are currently available as a beta offering and are available in only the DAL10 data center.
{: beta}

You can now choose the following Intel&reg; Sapphire Rapids CPUs when you provision a bare metal server.

| Sapphire Rapids CPU | Specifications | Memory | TPM 2.0 support |
| --- | --- | --- | --- |
| 8474C | 48 core, 2.1 GHz | 256 GB, 512 GB, 1024 GB, 2048 GB, 4096 GB | Yes |
{: caption="Table 1. Sapphire Rapids CPU options" caption-side="top"}

Sapphire Rapids processors support the following operating systems:

* Debian
* RHEL 8.6
* Rocky Linux
* Ubuntu 22.04
* No OS option

### AMD CPUs
{: #bm-amd-procs}

 AMD EPYC&reg; "Rome" generation CPUs are now an option. Rome generation processors are high-performance multiprocessors that are based on AMD's Zen 2 architecture. The EPYC "Rome" family offers several CPU options that offer up to 48 cores per socket.

EPYC processors are available in select data centers.
{: important}

You can choose from the following AMD EPYC "Rome" CPUs when you provision a bare metal server:

| AMD EPYC CPUs | Specifications |
| --- | --- |
| AMD EPYC 7642 | 48-core, 2.3 Ghz |
| AMD EPYC 7F72 | 48-core, 3.2 Ghz |
| AMD EPYC 7763 | 64-core, 2.45 Ghz |
{: caption="Table 2. AMD EPYC CPU options" caption-side="top"}

The following operating systems are supported by AMD EPYC "Rome" CPUs:
* RHEL 7.x, 8.x
* Ubuntu 18.04
* CentOS 7.x, 8.x
* Microsoft&reg; Server 2016, 2019
* Ubuntu 16.04, 18.04

Systems must be started in UEFI mode.
{: note}

For more information about AMD EPYC CPUs on {{site.data.keyword.cloud}}, see the [AMD on IBM Cloud Bare Metal Servers](https://www.ibm.com/cloud/amd).{: external}

### Intel Cascade Lake CPUs
{: #bm-cascade-lake-support}

You can choose from the following Intel Xeon&reg; Cascade Lake CPUs when you provision a bare metal server:

| Cascade Lake CPUs | Specifications |
|-----|-----|
| Intel Xeon 4210 | 10-Core, 2.2 GHz |
| Intel Xeon 5218 | 16-Core, 2.3 GHz |
| Intel Xeon 6248 | 20-Core, 2.6 GHz |
| Intel Xeon 6250 | 8-Core, 3.9 GHz |
| Intel Xeon 8260 | 48-core, 2.4 Ghz |
{: caption="Table 3. Cascade Lake CPU options" caption-side="top"}

### NVIDIA GPUs
{: #bm-gpu-support}

For certain bare metal servers, you can add the processing power of NVIDIA&reg; GPUs. When you select a bare metal server, look for **GPU** in the **Features** column on the provisioning page. Make sure that you install the appropriate drivers. See [NVIDIA drivers](https://www.nvidia.com/Download/index.aspx?lang=en-us){: external}

## Server enhancement options
{: #bm-server-enhancements}

When you provision a bare metal server, you have the following enhancement options to help make managing your server easier. Keep in mind that these options might vary depending on your server configuration.

### Dynamic inventory
{: #bm-dynamic-inv}

You can now see what servers are available in what data center when you provision a bare metal server. If a server is not available in the data center you selected, hover over the server name. A list is displayed that indicates the data centers in which the server is available. For more information about provisioning a bare metal server, see [Selecting from fast provisioning servers](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers).

### Network redundancy
{: #bm-network-redundancy}

Port redundancy provides networking failover by maintaining a primary and secondary network port. If the primary port fails, the secondary (redundant) port enables.

Only one port is active at a time.
{: note}

The following network redundancy options are available for bare metal servers.

| Redundancy options | Description |
| ---- | ----|
| Automatic redundancy (Recommended option) | Automatically configures the redundant ports for interface teaming through LACP (Link Aggregation Control Protocol) to preserve connectivity during routine maintenance. |
| User-managed redundancy | Must have interface teaming configured on the host operating system to use network redundancy. Without interface teaming, connectivity during routine maintenance is not preserved. |
| No redundancy | This is the only option for legacy data centers that don’t support automatic redundancy. This option is not recommended in a new data center.|
| Interface teaming (link aggregation)| Combines, in parallel, multiple network connections to provide redundancy and increase network throughput. |
{: caption="Table 4. Network redunancy options" caption-side="top"}

VMWare requires user-managed links.
{: tip}

For more information about network options, see [Network options](/docs/bare-metal?topic=bare-metal-network-options).

### Block and file storage add-on
{: #bm-block-and-file-add-on}

If you need extra storage, {{site.data.keyword.IBM_notm}} makes it easy! You can now order block and file storage (20 - 12,000 GB) when you provision a bare metal server.

Your add-on storage isn't automatically connected to your bare metal server. You need to connect the add-on storage to your bare metal server after your server provisions.

For more information about block and file storage, see the following links.
* [Getting started with Block Storage](/docs/BlockStorage?topic=BlockStorage-getting-started)
* [Getting started with File Storage](/docs/FileStorage?topic=FileStorage-getting-started)

## Bare metal server add-ons
{: #bm-add-ons}

The following add-ons are available when you provision a bare metal server.

| Option | Description |
|--------|-------------|
| Power supply | You can provision your bare metal server with two independent power supply units. These redundant units alternate power sources within the data center to help maintain uptime during unplanned or planned electrical maintenance. |
| IBM Cloud Backup | IBM Cloud Backup is an automated, agent-based backup and recovery system that is managed through the Cloud Backup WebCC browser utility. For more information, see [Getting started with IBM Cloud Backup](/docs/Backup?topic=Backup-getting-started).|
| Server security | Intel Trusted Execution Technology (TXT) provides hardware-assisted security technologies to enhance your security portfolio and act as an extra security for your infrastructure.|
| Business continuance insurance (BCI) | Business continuance insurance helps you avoid overage charges if you experience a network attack (DDOS) that uses all of your allowed bandwidth.|
| Firewall | A hardware firewall provides an extra layer of security that is provisioned on demand without service interruptions. This firewall prevents unwanted traffic from reaching your servers by reducing your attack surface, and by enabling your server resources to be dedicated for their intended use. For more information, see [Getting started with Hardware Firewall](/docs/hardware-firewall-shared?topic=hardware-firewall-shared-getting-started).|
| Monitoring - host ping | Basic monitoring is used to initiate service and slow pings to make sure that the device is online and responsive. For more information, see [Basic monitoring](/docs/cloud-infrastructure?topic=cloud-infrastructure-monitoring-iaas#basic-monitoring).|
| Notification | You can define an alert on a single metric or a set of metrics to notify you of events or issues that you want to monitor. For more information, see [Working with alerts](/docs/monitoring?topic=monitoring-alerts).|
| Response | Automated response to your monitored metrics notifications. |
| Public secondary IP addresses | You can request extra IP addresses for your server, which is recommended if you announce services externally. For more information about secondary IP addresses, see [Secondary subnets](/docs/subnets?topic=subnets-about-subnets-and-ips#static-subnets). If you need extra IP addresses later, you can always order extra secondary subnets. For more information, see [Ordering secondary subnets and global IP addresses](/docs/subnets?topic=subnets-order-subnets).|
| IPv6 IP addresses | An IPv6 is the most recent numeric label that is used to identify and locate a network interface of a computer or a network node that participates in a computer network by using the IPv6 protocol. A single IPv6 address is included.|
{: caption="Table 5. Bare metal server provisioning options" caption-side="top"}
