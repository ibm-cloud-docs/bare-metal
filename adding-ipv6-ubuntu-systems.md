---
copyright:
  years: 1994, 2017
lastupdated: "2017-09-26"

keywords: IPv6

subcollection: software

---
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Adding IPv6 to Ubuntu systems
{: #adding-ipv6-to-ubuntu-systems}

Use this procedure to bind IPv6 IP addresses to your Ubuntu server.
{:shortdesc}

1. Edit your **/etc/network/interfaces** file and add the following lines to the end of the file.

		#IPV6 configuration
	    iface eth1 inet6 static
	    pre-up modprobe ipv6 </br>
	    address 2607:f0d0:2001:0000:0000:0000:0000:0010</br>
	    netmask 64</br>
		gateway 2607:f0d0:2001:0000:0000:0000:0000:0001</br>
  The first line defines the interface on which the system uses IPv6.</br>
  The second line loads the module for IPv6.<br/>
  The third line identifies the IPv6 address.<br/>
  The fourth line defines the netmask for the IPv6 subnet.<br/>
  The fifth line defines the default gateway for the IPv6 subnet.

2. Restart networking with the following command:

	'/etc/init.d/networking restart'

## Verifying IPv6 connectivity
{: #verifying-ipv6-connectivity}

### Verify that IPv6 IP is bound
{: #verify-that-ipv6-ip-is-bound}

    root@server:~# ip -6 address show eth1
    3: eth1: mtu 1500 qlen 1000
        inet6 2607:f0d0:2001::/64 scope global
           valid_lft forever preferred_lft forever
        inet6 fe80::230:48ff:fe7e:330a/64 scope link
           valid_lft forever preferred_lft forever
    root@server:~#


### IPv6 Neighbor Cache
{: #ipv6-neighbor-cache}

    root@server:~# ip -6 neighbor show dev eth1
    2607:f0d0:2001::1 lladdr 00:1b:0d:e6:57:c0 router REACHABLE
    root@server:~#

If the neighbor cache shows a fe80 entry, one of the following conditions can apply:
- The gateway is not set
- The IP is not bound to the correct interface
- The IP is not bound correctly to the public interface
- The software firewall is blocking IPv6 ICMP.

### IPv6 Default Gateway
{: #ipv6-default-gateway}

    root@server:~# ip -6 route show dev eth1
    2607:f0d0:2001::/64  proto kernel  metric 256  mtu 1500 advmss 1440 hoplimit 4294967295
    fe80::/64  proto kernel  metric 256  mtu 1500 advmss 1440 hoplimit 4294967295
    default via 2607:f0d0:2001::1  metric 1024  mtu 1500 advmss 1440 hoplimit 4294967295
    root@server:~#

If the default gateway is not listed, you can use the `ping6` command to find your default gateway then add it manually using this IP command:

    root@server:~# ip -6 route add default via 2607:f0d0:2001::1
    root@server:~#
