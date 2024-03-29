---

copyright:
  years: 2020, 2022
lastupdated: "2021-04-20"

keywords: high availability, ha

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}


# Considerations for high availability and disaster recovery
{: #ha-dr}

Many events can cause server outages. Some are planned and within your control and others are unforeseen events such as hardware failures, software bugs, network issues, and even maintenance that didn’t go as planned. Multiple application servers need to be implemented to avoid and eliminate these potential outages. Spinning up multiple applications is not enough. Where the application server is deployed needs to be considered so that you avoid a single fault domain.

For bare metal servers, you want to spread the server application across multiple data centers. By placing the application servers across PODs, availability is improved.

While each POD supports multiple VLANs, you can order extra VLANs at the POD level rather than the data center level. As you order the bare metal server, you can assign the bare metal server to the VLANs to dictate server deployment across PODs within a data center.

## Linking your bare metal server
{: #linking-your-bm}

For bare metal servers, you can order a server as a single link or redundant link. If the workload doesn’t have any redundancy that is built into its application, it is best to order a redundant link for added link protection.

If your workload uses built-in redundancy to the application, whether it's through clustering or replication, you might be considering a single link rather than a redundant link to reduce costs. Keep in mind that having a redundant link is still a better option because it eliminates the link as the single point of failure and provides more bandwidth to the server.

## Network interface controller
{: #nic-controller}

The network interface controller (NIC) provides the link that connects your bare metal or virtual server to the network for communication. A common practice is to team two interfaces on the NIC to create a logical interface for redundancy and increase bandwidth. You have different options for teaming ports together.

1. Distribute traffic by using the operating system. This method provides switch-independent teaming.
2. Select automatic port redundancy. This redundancy allows the {{site.data.keyword.cloud}} provisioning service to create the NIC teaming by using LACP.
3. Perform the NIC teaming yourself through different NIC team modes such as active-passive, round-robin, adaptive transmit load-balancing, or adapter load-balancing.

For VMware&reg;, LACP is not available, but other NIC teaming mode is allowed.
{: note}
