---

copyright:
  years: 2019, 2021
lastupdated: "2021-02-01"

keywords: network port options, port options, network options, custom server, {{site.data.keyword.baremetal_short}}, {{site.data.keyword.cloud_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}
{:tip: .tip}
{:important: .important}
{:shortdesc: .shortdesc}

# Network options
{: #network-options}

{{site.data.keyword.baremetal_long}} have a number of network choices available to suit your unique needs.
{: shortdesc}

## Interface
{: #network-interfaces}

Select this option to choose whether you want your server to have public internet access, or only a private interface. Private network access is always included so the decision here is if you want your server to also have public internet access. If so, select **Public and Private**. Keep in mind that it is not possible to add a public interface to a server after it is provisioned with only a private interface.

The user that places the server order must have the **Add Compute with Public Network Port** permission to select an interface option, which contains a public interface.
{: note}

## Port redundancy
{: #network-port-redundancy}

Select this option to determine how you'd like to handle network connection redundancy. Choose from these options:


- **Automatic** is the default and recommended setting. It provides two physical network ports that are configured with LACP bonding on both the network and the operating system at time of provisioning. This is the most hands-free option for continuous network availability.

- **User Managed** is available for advanced configurations. It provides two physical network ports, but the ports are configured independently on both the network and the operating system. For this option to provide any redundancy, you must take action in your application, operating system, or both to use the secondary port. If you use the second port in a manner that does not provide redundant connectivity to your application, you will not have redundant connectivity. By selecting this option, you are communicating that you have the knowledge and skill to configure redundancy on your system (or within your application) and are aware that not doing so results in a lack of network communication redundancy during routine network maintenance.

- **None** provides a single physical port to each network. It is maintained as an option for customers who continue to order within legacy data centers and that might require PXE booting capability. (See [Port speed](#network-port-speed) for information concerning the specialized need for **unbonded**.) While it is possible to choose this option in all data centers, you should select **None** only in consultation with IBM Sales or Support under specific conditions.

Network maintenance is normal. While you are notified, you can avoid disruption only when using **Automatic** redundancy, or making a special effort under the **User Managed** redundancy option.
{: note}

## Port speed
{: #network-port-speed}

Select either 100 Mbps, 1 Gbps, 10 Gbps, or 25 Gbps as the maximum operating speed of all network interfaces. 

The 25 Gbps port speed option is limited to select bare metal server options. For more information, see [25 Gbps port speed](/docs/bare-metal?topic=bare-metal-network-options#25gb-port-speed). 
{: important}

If you selected **None** for port redundancy, you might see an option that includes the word **unbonded**. These options account for specific interactions between our default port bonding configurations and PXE booting. They are only relevant in older pods, such as **`sjc01.pod01`**, and **`wdc01.pod01`**. By default, all ports are configured into a redundant bond, even if not all ports are active; this allows for a seamless redundancy upgrade in the future. However, this default bonding can prevent PXE booting in some locations. The option causes ports to _not_ be configured within a bond by default, regardless of the number of active interfaces. Modern data centers do not have a conflict with PXE booting and our default bonding configuration. Avoid use of this feature unless instructed by IBM Sales or Support.

### 25 Gbps port speed
{: 25gb-port-speed}

The 25 Gbps port speed option is compatible with only 2U (12 drive) Cascade Lake processor servers and is available in select pods in only the following data centers:

| 25 Gbps data centers | | |
| ----- | ----- | --- |
| DAL12 | DAL13 | |
| FRA02 |  | |
| LON04 | | |
| SYD04 | SYD05 | |
| TOK02 | TOK04 | TOK05 |
| TOR04 | | |
| WDC06 | WDC07 | |
{: caption="Table 1. 25 GB network data centers" caption-side="top"}

25 Gbps port speeds are available with the following operating systems:

* CentOS 8.2
* RHEL 8.2 
* RHEL 8.2 for SAP
* Windows server 2016, 2019

## Public egress bandwidth
{: #network-bandwidth-public}

Select this option to choose the amount of included outbound, or egress, public traffic that you'd like with your server. The selected value is per billing period. Any traffic that is recorded over the selection for the period is charged per gigabyte (GB) as an overage. A value of `0 GB` means that _all_ traffic is charged. Inbound, or ingress, public traffic is free of charge.

## Provisioning VLAN selection
{: #network-vlan-selection}

When configuring a server, you are sometimes provided a VLAN selector. This selection is optional, and only shows existing VLANs located within the selected data center. The selector is for a private VLAN, and when you choose a private VLAN, a public VLAN selector is presented. It shows public VLANs available in the same pod as the selected private VLAN (if a public interface is applicable). These selections allow you to control what VLANs, and therefore what pod, in which your server resides. VLAN selection becomes more relevant when taking advantage of [gateway](/docs/gateway-appliance?topic=gateway-appliance-getting-started) or [hardware firewall](/docs/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-) products, or if constructing a multi-tier network architectures. Review [Premium VLANs](/docs/vlans?topic=vlans-about-vlans#about-premium-vlans) if you are looking to deploy a specific network topology prior to server provisioning.

## Provisioning subnet selection
{: #network-subnet-selection}

If a VLAN is selected for a network connection, you are presented with a list of [primary subnets](/docs/subnets?topic=subnets-about-subnets-and-ips#primary-subnets) from which to choose. This selection is also optional, and it is recommended to retain the default option of **Auto assigned**. Primary IP addresses and subnets are assigned as needed. Selecting a subnet for multiple device orders can cause that subnet to no longer have available IP addresses. If you request a specific subnet that no longer has IP addresses available, IBM must contact you, which drastically increases provisioning time, and reduces ordering convenience. Use this advanced feature only when a specific procedure is needed.

## Primary IP addresses
{: #network-ip-address-primary}

Primary IP addresses are the name that we give the IP addresses assigned to your private and public network interfaces by default. An IPv4 address is included with the price of your server for each network. These addresses provide server-unique connectivity on their respective network, and are non-transferable. It is important to understand what primary IP addresses, and thus what [primary subnets](/docs/subnets?topic=subnets-about-subnets-and-ips#primary-subnets) do and do not allow. It is highly recommended to use [secondary IP addresses](#network-ip-address-secondary) when announcing external services so your IP addresses are not tightly coupled to any particular server.

**IPv6** - Within the **Add-ons** section of the network options is the **IPv6 address** option. If you want a public primary IPv6 address, select this option. Your server must have a primary IPv6 address to interact with any other products that use IPv6 connectivity.

## Secondary IP addresses
{: #network-ip-address-secondary}

You can request additional IP addresses for your server (which is recommended when announcing services externally) during server ordering. The **Public secondary IP addresses** option is in the **Add-ons** section of the network options. Select the number of IP addresses you want, then a [secondary static subnet](/docs/subnets?topic=subnets-about-subnets-and-ips#static-subnets) of the appropriate size will automatically be provisioned and routed to your server's public primary IP address. If you require more IP addresses later, you can [order additional secondary subnets](/docs/subnets?topic=subnets-getting-started#ordering-subnets).

## Server hardware firewall
{: #network-firewall-server}

Applicable when a public network interface is requested, this option places a firewall in front of your server. The rules of the firewall apply only to the IP addresses associated with the server. Read [Hardware Firewalls (Shared)](/docs/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-) to learn more.

## Always included options and services
{: #server-network-included}

The following network options and services are always included with your {{site.data.keyword.baremetal_short}}:
- **Private network interface** - All {{site.data.keyword.baremetal_short}} include access to the private network, which allows access to other IBM Services.
- **Primary IP addresses** - A private IPv4 address is included with a private network interface. If a public network interface is selected, a public IPv4 address is also included. These addresses provide basic connectivity to the server. Learn more about [primary IP addresses](/docs/subnets?topic=subnets-about-subnets-and-ips#primary-subnets).
- **VPN Management** - Manage access to the subnet the server resides on for users when connecting through [VPN](/docs/iaas-vpn?topic=iaas-vpn-about-iaas-vpn).

## Understanding network options on your invoice
{: #server-invoice-network}

The way that you select your network interface options during ordering differs from how they are represented on your invoice. On your invoice, for each server, an entry similar to the following is shown:

`1Gbps Public & Private Network Uplinks`

This indicates a private and public network connection was requested at a speed of 1 gigabit per second. The speed is always represented first, and indicates the speed of both the private and public network interfaces (if applicable). Additional keywords can be present:

- **Redundant** - Indicates that you selected **Automatic** for the **Port redundancy** option.
- **Dual** - Indicates that you selected **User Managed** for the **Port redundancy** option.
- **Unbonded** - Indicates that you selected either **User Managed** for the **Port redundancy** option, or a **Port speed** option containing the word **unbonded**.
- **Private Only** - Indicates that you selected **Private** for the server's network interface.
