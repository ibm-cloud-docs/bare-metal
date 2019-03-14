---

copyright:
  years: 1994, 2019
lastupdated: "2018-07-31"

keywords: assign server IP addresses, server IP addresses

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Assigning server IP addresses
{: #bm-assign-ip-address}

{{site.data.keyword.cloud}} configures servers with these addresses:
An IPv4 address on the private network
An IPv4 address for low-level management access on the
private network
A public IPv4 address, if requested.

An IPv6 address on the public network, is available if requested. All of
these IP addresses are collectively referred to as **Primary IP addresses**.

More IP addresses can be bound to servers after you purchase **Secondary
Subnets** through the [{{site.data.keyword.slportal}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com){: new_window}. IP addresses that you purchased through the Customer Portal
and managed by you are called **Secondary IP addresses**.

For more information about acquiring IP addresses, see [Subnets and IPs ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/docs/infrastructure/subnets/).


# Binding Secondary IP addresses
{: #bm-bind-secondary-ip-address}

After you purchase a secondary subnet, you need to
configure the operating system to use one or more IP addresses. Each operating system configures IP addresses differently, but is typically referred to as setting up "interface aliases".
