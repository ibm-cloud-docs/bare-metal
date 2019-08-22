---

copyright:
  years:  2019
lastupdated: "2018-05-15"

keywrods: bare metal, managed pools

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# About customer-managed pools
{: #bm-customer-managed-pools}

Customer-managed pools give you access to a set of servers that is always available to your organization. These servers are configured to your specifications. You can order servers from the pool when you need them.

This feature is ideal if your organization frequently needs to provision many servers for use during peak periods. With this feature, you can use only the minimum number of servers you need but always have a large set of servers available to meet your additional needs.

## Usage example
{: #bm-managed-pools-use-case}

Company A is using 1000 active servers for daily operations. However, at peak times, they might need up 500 extra servers. They need the extra servers to be up and running quickly.

To meet their need, Company A contacts IBM to set up a managed pool of servers. After the pool is set up, they make an API call to set the number of servers in the pool to 500.

In July, Company A needs 250 extra servers from their pool. They order 250 servers. This order is quickly fulfilled with 250 servers from the pool. After the order is complete, 250 servers are added to Company A's managed pool so that there are always 500 available.


## Next steps
{: #manage-pool-next}

If your organization wants to use a customer-managed pool, see [Provisioning customer-managed pools](/docs/bare-metal?topic=bare-metal-provisioning-customer-managed-pools)
