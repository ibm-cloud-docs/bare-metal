---

copyright:
  years:  2018, 2022
lastupdated: "2022-04-15"

keywords: 

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Specifying the number of servers in your customer-managed pool
{: #set-amount-servers-pool}

Set the number of servers in your managed pool by using the following API call.
{: shortdesc}

|API Call|Parameters|Description|
|---|---|---|
| [Set managed pool quantity](https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity) | poolKeyName | Key name that identifies your pool. IBM provides this value to you. |
|  | backendRouter | Identifies the backend router for your pool. IBM provides this value to you.|
|  | quantity | The total number of servers you want in your pool. If the current number of servers in your pool is less than the value that you provide here, servers are added. If the current number of servers in your pool is more than the value you provide here, servers are removed.|
{: caption="Table 1. Managed pool API calls" caption-side="top"}
