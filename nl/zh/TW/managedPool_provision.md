---

copyright:
  years:  2019
lastupdated: "2019-02-01"

keywrods: provision managed pool, managed pools

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 佈建客戶管理的儲存區
{: #bm-provision-managed-pools}

若要佈建客戶管理的伺服器儲存區，請直接與 IBM 聯絡：[取得協助及支援](/docs/bare-metal?topic=bare-metal-gettinghelp)。

請提供下列資訊：
* 您想要受管理儲存區位於哪個資料中心。（受管理儲存區中的所有伺服器都必須位於相同的資料中心。）
* 您想要在受管理儲存區中保留的伺服器數目
* 聯合排存伺服器所需的規格

建立儲存區之後，IBM 會提供下列參數值給您。當您傳送 API 指令以管理儲存區時，需要這些值。
* poolKeyName
* backendRouter

## 從受管理儲存區訂購伺服器
{: #bm-order-server-managed-pool}
請使用標準佈建程序來訂購儲存區中的伺服器。您的訂單會從儲存區履行，然後儲存區會以您訂購的伺服器數目補充。

## 後續步驟

從佈建客戶管理的儲存區，並從受管理儲存區訂購伺服器之後，您可以管理儲存區中的伺服器數目。請參閱[指定客戶管理之儲存區中的伺服器數目](/docs/bare-metal?topic=bare-metal-set-amount-servers-pool#set-amount-servers-pool)。
