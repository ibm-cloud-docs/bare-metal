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

# 顧客管理プールのプロビジョン
{: #bm-provision-managed-pools}

サーバーの顧客管理プールをプロビジョンするには、IBM に直接お問い合わせください ([ヘルプおよびサポートの利用](/docs/bare-metal?topic=bare-metal-gettinghelp))。

以下の情報を指定します。
* 管理対象プールを配置するデータ・センター。 (管理対象プール内のすべてのサーバーを同じデータ・センターに配置する必要があります。)
* 管理対象プールに必要なサーバーの数
* プールされたサーバーで必要な仕様

プールの作成後に、IBM が以下のパラメーター値を指定します。 これらの値は、プールを管理するために API コマンドを送信する際に必要です。
* poolKeyName
* backendRouter

## 管理対象プールからのサーバーの注文
{: #bm-order-server-managed-pool}
プール内のサーバーを注文するには、標準のプロビジョニング・プロセスを使用します。 注文はプールから実行され、プールは、注文した数のサーバーで補充されます。

## 次のステップ

顧客管理プールをプロビジョンして、管理対象プールからサーバーを注文した後で、プール内のサーバーの数を管理できます。 [顧客管理プール内のサーバー数の指定](/docs/bare-metal?topic=bare-metal-set-amount-servers-pool#set-amount-servers-pool)を参照してください。
