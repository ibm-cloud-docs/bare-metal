---

copyright:
  years: 2016, 2019
lastupdated: "2019-06-19"

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

# About bare metal servers
{: #about-bm}

{{site.data.keyword.baremetal_long}} are the cornerstone for your infrastructure-as-a-service solution. Whether you're a gaming developer who requires high-speed I/O or you need to up high-performance servers for your users, {{site.data.keyword.baremetal_short}} can answer your compute needs.
{:shortdesc}

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
<!--Intel Xeon 8280M (28-Core, 2.7 GHz, 205 W)--><br>

<br>Cascade Lake processors are available in the following data centers:

<table style="width:100%">
<CAPTION>Table 1. Data centers with Cascade Lake processors</CAPTION>
 <tr>
   
   <th colspan="6">Data centers</th>
 </tr>
 <tr>
   <td>DAL10</td>
   <td>FRA02</td>
   <td>LON04</td>
   <td>SYD01</td>
   <td>TOK02</td>
   <td>WDC04</td>
   
</tr>

<tr>
  <td>DAL12</td>
  <td>FRA04</td>
  <td>LON05</td>
  <td>SYD04</td>
  <td>TOK04</td>
  <td>WDC06</td>
  
</tr>

<tr>
  <td>DAL13</td>
  <td>FRA05</td>
  <td>LON06</td>
  <td>SYD05</td>
  <td>TOK05</td>
  <td>WDC07</td>
</tr>
</table>


### Dynamic inventory
{: #bm-dynamic-inv}

You can now see what servers are available in what data center when you provision a bare metal server. But, this option is available for only the hourly offering. You cannot see server availability with the monthly offering. For more information about provisioning a bare metal server, see [Selecting from fast provisioning servers](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers).

### Block and file storage add-on
{: #bm-block-and-file-add-on}

If you need extra storage, {{site.data.keyword.IBM_notm}} makes it easy! You can now order block and file storage (20 - 12,000 GB) when you provision a bare metal server. 

Your add-on storage isn't automatically connected to your bare metal server. You need to connect the add-on storage to your bare metal server after your server provisions.
{: note} 

<!--The add-on storage shares the data center that your bare metal server is on.-->

For more information about block and file storage, see the following links.
* [About block storage](/docs/infrastructure/BlockStorage?topic=BlockStorage-About)
* [About file storage](/docs/infrastructure/FileStorage?topic=FileStorage-about)
