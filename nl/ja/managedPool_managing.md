---

copyright:
  years:  2019
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

# 顧客管理プール内のサーバー数の指定
{: #set-amount-servers-pool}

以下の API 呼び出しを使用して、管理対象プール内のサーバーの数を設定します。

|API 呼び出し|パラメーター|説明|
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank">管理対象プールの数量の設定</a>|poolKeyName|プールを識別するキー名。 IBM がこの値を指定します。|
|  | backendRouter | プールのバックエンド・ルーターを識別します。 IBM がこの値を指定します。|
|  | quantity | プール内に必要なサーバーの総数。<br><br>プール内の現在のサーバー数が、ここで指定した値より少ない場合は、サーバーが追加されます。<br>プール内の現在のサーバー数が、ここで指定した値より多い場合は、サーバーが削除されます。|
