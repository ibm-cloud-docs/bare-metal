---

copyright:
  years:  2018
lastupdated: "2018-05-15"

subcollection: bare-metal

---

# Specifying the number of servers in your customer-managed pool

Set the number of servers in your managed pool by using the following API call:

|API Call|Parameters|Description|
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank">Set managed pool quantity</a>|poolKeyName|Key name that identifies your pool. IBM provides this value to you.|
|  | backendRouter | Identifies the backend router for your pool. IBM provides this value to you.|
|  | quantity | The total number of servers you want in your pool.<br><br>If the current number of servers in your pool is less than the value your provide here, servers are added.<br>If the current number of servers in your pool is more than he value you provide here, servers are removed.|
