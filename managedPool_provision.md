---

copyright:
  years:  2018
lastupdated: "2018-05-15"

---


# Provisioning customer-managed pools

To provision a customer-managed pool of servers, contact IBM directly: [Getting help and support](/docs/bare-metal?topic=bare-metal-gettinghelp).

Provide the following information:
* The data center that you want your managed pools to be located. (All servers in a managed pool must be located in the same data center.)
* The number of servers you want in your managed pool
* The specifications that you need for your pooled servers

After your pool is created, IBM provides you with the following parameter values. You need these values when you send the API command to manage your pool.
* poolKeyName
* backendRouter

## Ordering servers from your managed pool
Use the standard provisioning process to order servers in your pool. Your order is fulfilled from your pool and your pool is replenished with the number of servers that you ordered.

## Next steps

After you provision your customer-managed pool, and ordering servers from your managed pool, you can manage the number of servers in your pool. Refer to [Specifying the number of servers in your customer-managed pool](/docs/bare-metal?topic=bare-metal-specifying-the-number-of-servers-in-your-customer-managed-pool)
