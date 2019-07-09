---

copyright:
  years: 2016, 2019
lastupdated: "2018-11-06"

keywords: activity tracker, bare metal, {{site.data.keyword.Bluemix}}

subcollection: bare-metal

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Activity Tracker イベント
{: #bm-at-events}

セキュリティー担当者、監査員、およびマネージャーは、
{{site.data.keyword.cloudaccesstrailfull}} サービスを使用して、ユーザーおよびアプリケーションが {{site.data.keyword.Bluemix}} 内のベアメタル・サーバーとどのように対話しているかをトラッキングできます。アカウント所有者およびアカウントにリンクされたユーザーは、
{{site.data.keyword.cloudaccesstrailshort}}に記録されるベアメタル・サーバー・イベントをトリガーできます。
{:shortdesc}

{{site.data.keyword.cloudaccesstrailshort}} サービスは、
{{site.data.keyword.Bluemix_notm}} 内のサービスの状態を変更するユーザー開始アクティビティーを記録します。詳しくは、
[{{site.data.keyword.cloudaccesstrailshort}} について](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov )を参照してください。

ユーザーのアクションのモニタリングを開始するには、[IBM Cloud Activity Tracker の概要](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started#getting-started)を参照してください。

イニシエーターは、ユーザー、サービス、またはアプリケーションのいずれかです。 ユーザーがイベントを生成するには、ユーザーは {{site.data.keyword.Bluemix}} コンソールの**「インフラストラクチャー」**リソースにアクセスできる必要があります。
{: tip}

## ベア・メタル・サーバー・インスタンス・イベント
{: #bare-metal-events}

{{site.data.keyword.cloudaccesstrailshort}} サービスを使用して、ベア・メタル・サーバーをそのライフサイクルを通じて監査できます。

以下の表に、イベントを生成するアクションをリストします。

| アクション | 説明 |
|----------|---------|
| `audit-log.bare-metal.provision`             | イニシエーターがベア・メタル・サーバーをプロビジョンするとイベントが生成されます。  |
| `audit-log.bare-metal-port.disable`          | イニシエーターがベア・メタル・サーバーでポートを無効化するとイベントが生成されます。 |
| `audit-log.bare-metal-port.enable`           | イニシエーターがベア・メタル・サーバーでポートを有効化するとイベントが生成されます。 |
| `audit-log.bare-metal-port-speed.update`     | イニシエーターがベア・メタル・サーバーでポート速度を更新するとイベントが生成されます。 |
| `audit-log.bare-metal.power-off`             | イニシエーターがベア・メタル・サーバーをパワーオフするとイベントが生成されます。  |
| `audit-log.bare-metal.reboot`                | イニシエーターがベア・メタル・サーバーをリブートするとイベントが生成されます。 |
| `audit-log.bare-metal.soft-reboot`           | イニシエーターがベア・メタル・サーバーでソフト・リブートを実行するとイベントが生成されます。 |
| `audit-log.bare-metal.hard-reboot`           | イニシエーターがベア・メタル・サーバーでハード・リブートを実行するとイベントが生成されます。 |
| `audit-log.bare-metal.power-on`              | イニシエーターがベア・メタル・サーバーをパワーオンするとイベントが生成されます。 |
| `audit-log.bare-metal.rename`                | イニシエーターがベア・メタル・サーバーを名前変更するとイベントが生成されます。 |
| `audit-log.bare-metal.rescue`                | イニシエーターがベア・メタル・サーバーをレスキューするとイベントが生成されます。 |
| `audit-log.bare-metal.reload`                | イニシエーターがベア・メタル・サーバーに対してオペレーティング・システム (OS) 再ロードを実行するとイベントが生成されます。 |
{: caption="表 2. ベア・メタル・サーバー・アクション" caption-side="top"}


## イベントの表示
{: #bm-view-events}

イベントが生成された {{site.data.keyword.Bluemix_notm}} 地域で
使用可能な {{site.data.keyword.cloudaccesstrailshort}} **アカウント・ドメイン**で、{{site.data.keyword.cloudaccesstrailshort}} イベントを確認することができます。詳しくは、
[アカウント・イベントの表示](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events) を参照してください。

{{site.data.keyword.cloudaccesstrailshort}} イベントは、
アクションが発生するのと同じ地域内の {{site.data.keyword.cloudaccesstrailshort}} サービスに自動的に転送されます。
