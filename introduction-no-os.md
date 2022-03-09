---

copyright:
  years: 2017, 2022
lastupdated: "2022-03-09"

keywords: no os, no operating system, server with no os

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# No OS options
{: #bm-no-os}

**No OS** is an option to order {{site.data.keyword.baremetal_long}} without an operating system.

## Ordering {{site.data.keyword.baremetal_short}} with no OS
{: #ordering-no-os}

1. Use the steps that are outlined in [Building a Custom Bare Metal Server](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server) to order your server.
2. Select **No OS** under **Image**.
3. Complete your server order.

## Changing to no OS
{: #changing-to-no-os}

You can reconfigure a server to have no OS. The reconfiguration is done through an OS reload. For more information, see [Reloading the OS](/docs/bare-metal?topic=bare-metal-reloading-the-os).

1. Click **Devices** > **Device List**.
2. Select the server that you want to reconfigure with no OS.
3. Click **OS Reload** and enter the applicable information.

## Installing an operating system on a no OS server
{: #installing-os-on-no-os-server}

You have two methods to install operating systems on {{site.data.keyword.baremetal_short}} with no operating system.

### Option 1: PXE Server
{: #option-1}

You can set up {{site.data.keyword.baremetal_short}} with no operating systems to boot and load an OS from a PXE setup. Deployment of {{site.data.keyword.baremetal_short}} in a network environment with a PXE setup (usually involves running a DHCP and TFTP daemon) and configure the new servers BIOS to boot from the network adapter. For the no OS option to work properly, PXE setup needs to be in the same VLAN as the {{site.data.keyword.baremetal_short}}, or DHCP forwarding needs to be used.

It might be necessary to open a support case to request that the switch ports be regrouped in basic mode for this option to work. This request is necessary because the PXE protocol doesn't require compatibility with link aggregation (LACP), which is now a standard capability to provide redundancy. Another option is to order the server with unbonded uplinks (no link aggregation) and then change them to redundant uplinks after the OS is installed.
{: note}

### Option 2: IPMI device
{: #option-2}

Install operating systems on {{site.data.keyword.baremetal_short}} with no operating systems by booting from an ISO by using the included IPMI device. For more information about booting from an ISO, see [Mounting an ISO on a bare metal server](/docs/bare-metal?topic=bare-metal-bm-mount-iso).
