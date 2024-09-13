---

copyright:
  years: 1994, 2024
lastupdated: "2024-09-13"


keywords: server IP addresses, {{site.data.keyword.cloud}}, bind ip address, assign server ip address

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Assigning and binding IP addresses
{: #bm-assigning-and-binding-ip-addresses}

Use the following information to assign a server IP address to your server and bind a secondary IP address to your server, if required.
{: shortdesc}

## Assigning server IP addresses
{: #bm-assign-ip-address}

{{site.data.keyword.cloud}} configures servers with the following addresses.

* An IPv4 address on the private network
* An IPv4 address for low-level management access on the
private network
* A public IPv4 address, if requested.
* An IPv6 address on the public network is available, if requested. All of
these IP addresses are collectively referred to as the **primary IP addresses**.
* Extra IP addresses can be bound to servers after you purchase **Secondary
Subnets** through the [{{site.data.keyword.cloud_notm}} console](https://cloud.ibm.com){: external}. IP addresses that you purchased and managed by you are called **Secondary IP addresses**.

For more information about acquiring IP addresses, see [Subnets and IP addresses](https://cloud.ibm.com/docs/subnets/){: external}.

## Binding Secondary IP addresses
{: #bm-bind-secondary-ip-address}

After you purchase a secondary subnet, you need to configure the operating system to use one or more IP addresses. Each operating system configures IP addresses differently and is typically referred to as setting up "interface aliases".
