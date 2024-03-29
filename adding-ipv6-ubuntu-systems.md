---
copyright:
  years: 1994, 2022
lastupdated: "2021-09-20"

keywords: IPv6, ipv6 ubuntu

subcollection: bare-metal

---
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}

# Adding IPv6 to Ubuntu systems
{: #adding-ipv6-to-ubuntu-systems}

Use this procedure to bind IPv6 IP addresses to your Ubuntu server.
{: shortdesc}

1. Edit your **/etc/network/interfaces** file and add the following lines to the end of the file.

   ```text
   #IPV6 configuration
   iface eth1 inet6 static
   pre-up modprobe ipv6 
   address 2607:f0d0:2001:0000:0000:0000:0000:0010
   netmask 64
   gateway 2607:f0d0:2001:0000:0000:0000:0000:0001
   ```
   {: pre}
   
   - The first line defines the interface on which the system uses IPv6.
   - The second line loads the module for IPv6.
   - The third line identifies the IPv6 address.
   - The fourth line defines the netmask for the IPv6 subnet.
   - The fifth line defines the default gateway for the IPv6 subnet.

2. Restart networking with the following command:

   ```text
   /etc/init.d/networking restart
   ```
   {: pre}

## Verifying IPv6 connectivity
{: #verifying-ipv6-connectivity}

### Verify that IPv6 IP is bound
{: #verify-that-ipv6-ip-is-bound}

   ```text
   root@server:~# ip -6 address show eth1
   3: eth1: mtu 1500 qlen 1000
       inet6 2607:f0d0:2001::/64 scope global
          valid_lft forever preferred_lft forever
       inet6 fe80::230:48ff:fe7e:330a/64 scope link
          valid_lft forever preferred_lft forever
   root@server:~#
   ```
   {: pre}

### IPv6 neighbor cache
{: #ipv6-neighbor-cache}

   ```text
   root@server:~# ip -6 neighbor show dev eth1
   2607:f0d0:2001::1 lladdr 00:1b:0d:e6:57:c0 router REACHABLE
   root@server:~#
   ```
   {: pre}

If the neighbor cache shows a fe80 entry, one of the following conditions can apply:
- The gateway is not set
- The IP is not bound to the correct interface
- The IP is not bound correctly to the public interface
- The software firewall is blocking IPv6 ICMP.

### IPv6 default gateway
{: #ipv6-default-gateway}

   ```text
   root@server:~# ip -6 route show dev eth1
   2607:f0d0:2001::/64  proto kernel  metric 256  mtu 1500 advmss 1440 hoplimit 4294967295
   fe80::/64  proto kernel  metric 256  mtu 1500 advmss 1440 hoplimit 4294967295
   default via 2607:f0d0:2001::1  metric 1024  mtu 1500 advmss 1440 hoplimit 4294967295
   root@server:~#
   ```
   {: pre}

If the default gateway is not listed, you can use the `ping6` command to find your default gateway then add it manually using this IP command:

   ```text
   root@server:~# ip -6 route add default via 2607:f0d0:2001::1
   root@server:~#
   ```
   {: pre}
