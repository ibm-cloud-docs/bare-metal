---

copyright:
  years:  2018, 2021
lastupdated: "2018-05-15"

keywords: number servers managed pool, managed pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Specifying the number of servers in your customer-managed pool
{: #set-amount-servers-pool}

Set the number of servers in your managed pool by using the following API call:

|API Call|Parameters|Description|
|---|---|---|
| [Set managed pool quantity](https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity) | poolKeyName | Key name that identifies your pool. IBM provides this value to you. |
|  | backendRouter | Identifies the backend router for your pool. IBM provides this value to you.|
|  | quantity | The total number of servers you want in your pool. If the current number of servers in your pool is less than the value that you provide here, servers are added. If the current number of servers in your pool is more than the value you provide here, servers are removed.|
