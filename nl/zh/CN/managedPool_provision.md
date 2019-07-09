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

# 供应客户管理的池
{: #bm-provision-managed-pools}

要供应客户管理的服务器池，请直接与 IBM 联系：[获取帮助和支持](/docs/bare-metal?topic=bare-metal-gettinghelp)。

提供以下信息：
* 您希望受管池位于的数据中心。（受管池中的所有服务器都必须位于同一个数据中心内。）
* 您希望受管池中具有的服务器数
* 需要用于池中服务器的规范

创建池后，IBM 将向您提供以下参数值。发送 API 命令来管理池时，需要这些值。
* poolKeyName
* backendRouter

## 订购受管池中的服务器
{: #bm-order-server-managed-pool}
使用标准供应过程来订购池中的服务器。订单将通过池来供货，并且会向池补充所订购数量的服务器。

## 后续步骤

供应客户管理的池以及订购受管池中的服务器之后，可以管理池中的服务器数。请参阅[指定客户管理的池中的服务器数](/docs/bare-metal?topic=bare-metal-set-amount-servers-pool#set-amount-servers-pool)。
