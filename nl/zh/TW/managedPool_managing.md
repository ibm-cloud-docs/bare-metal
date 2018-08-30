---

copyright:
  years:  2018
lastupdated: "2018-05-15"

---

# 指定客戶管理之儲存區中的伺服器數目

使用下列 API 呼叫，設定受管理儲存區中的伺服器數目：

|API 呼叫|參數|說明 |
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank">設定受管理儲存區數量</a>|poolKeyName|識別儲存區的金鑰名稱。IBM 會為您提供此值。|
|  | backendRouter |識別儲存區的後端路由器。IBM 會為您提供此值。|
|  | quantity |您想要在儲存區中保留的伺服器總數。<br><br>如果儲存區中的伺服器數目小於您在這裡提供的值，則會新增伺服器。<br>如果儲存區中的伺服器數目超過您在這裡提供的值，則會移除伺服器。|
