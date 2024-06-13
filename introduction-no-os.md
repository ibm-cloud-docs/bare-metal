---

copyright:
  years: 2017, 2024

lastupdated: "2024-06-06"


keywords: no os, no operating system, server with no os

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# No OS option
{: #bm-no-os}

**No OS** is an option to order {{site.data.keyword.baremetal_long}} without an operating system.

## Ordering {{site.data.keyword.baremetal_short}} with no OS
{: #ordering-no-os}

Use the following steps to order a bare metal server without an operating system.

1. Use the steps that are outlined in [Building a Custom Bare Metal Server](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server) to order your server.


   Because of compatibility issues, you can't select NMVe drives if you're going to install Windows&reg;.
   {: important}

2. Select **No OS** under **Image**.
3. Complete your server order.

## Reloading to no OS
{: #reloading-to-no-os}

If you ordered your server without an OS you want to reset it to a like-new configuration without an OS again, this reconfiguration is done through an OS Reload. For more information, see [Reloading the OS](/docs/bare-metal?topic=bare-metal-reloading-the-os).

1. Click **Devices** > **Device List**.
2. Select the server that you want to reconfigure with no OS.
3. Click **OS Reload** and enter the applicable information.

If you ordered a server with an operating system that is licensed through {{site.data.keyword.cloud}}, or if you reloaded your no OS server to have an operating system from {{site.data.keyword.cloud}}, the "no OS" option is no longer available. To revert to a no OS server, you need to cancel the existing server and order it again with the no OS option.
   {: important}

## Installing an operating system on a no OS server
{: #installing-os-on-no-os-server}

You have two methods to install operating systems on {{site.data.keyword.baremetal_short}} when you select the no OS option.

### Option 1: PXE Server
{: #option-1}

You can set up {{site.data.keyword.baremetal_short}} with no operating system to boot and load an OS from a PXE setup. Deployment of {{site.data.keyword.baremetal_short}} in a network environment with a PXE setup (this process usually involves running a DHCP and TFTP daemon) and configure the new server BIOS to boot from the network adapter. For the no OS option to work properly, you need to set up PXE in the same VLAN as the {{site.data.keyword.baremetal_short}}, or you need to use DHCP forwarding.

It might be necessary to open a support case to request that the switch ports be regrouped in basic mode for this option to work. This request is necessary because the PXE protocol doesn't require compatibility with link aggregation (LACP), which is now a standard capability to provide redundancy. Another option is to order the server with unbonded uplinks (no link aggregation) and then change them to redundant uplinks after the OS is installed.
{: note}

### Option 2: IPMI device
{: #option-2}

You can install an operating system on {{site.data.keyword.baremetal_short}} by booting from an ISO with the included IPMI device. For more information about booting from an ISO, see [Mounting an ISO on a bare metal server](/docs/bare-metal?topic=bare-metal-bm-mount-iso).
