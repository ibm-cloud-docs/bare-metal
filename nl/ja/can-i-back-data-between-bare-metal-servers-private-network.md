---

copyright:
  years: 1994, 2019
lastupdated: "2019-05-02"

keywords: back up, recovery, IBM Cloud Backup, r1soft

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# バックアップおよびリカバリー
{: #sm-back-up-recovery}

{{site.data.keyword.Bluemix_notm}} は、お客様のバックアップ要件を満たすために、各種のスケーラブルな[バックアップおよびストレージ用ソリューション ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/cloud/storage){: new_window} を提供します。 ただし、{{site.data.keyword.Bluemix_notm}} では、お客様のデバイスのバックアップは実行しません。 お客様のデバイスでのすべてのスケジュールされたバックアップおよび 1 回限りのバックアップは、アカウントのユーザーが開始する必要があります。

1 つのアカウントで 2 つ以上の {{site.data.keyword.baremetal_short}} が存在している場合、1 つのデバイスからのデータを別のデバイスにバックアップできます。 プライベート・ネットワークのトラフィックについては帯域幅に制限が課されていないので、アカウントが共有されているデバイス同士なら、随時、任意のデバイスにデータを転送またはバックアップすることができます。 {{site.data.keyword.baremetal_short}} では、以下に示すソリューションを含めて、いくつかのバックアップ・ソリューションが使用可能です。

* [IBM Cloud バックアップ](/docs/infrastructure/Backup?topic=Backup-getting-started#getting-started)。複数のサーバーでのバックアップを自動化できるエンタープライズ・バックアップ・ソリューションです。データは、エンタープライズ SAN (ストレージ域ネットワーク) に保管されます。
* [Network Attached Storage (NAS)](/docs/infrastructure/network-attached-storage?topic=network-attached-storage-GettingStarted#GettingStarted)。業界標準であり、重要なデータのサーバー外でのストレージを提供します。 データは、エンタープライズ SAN (ストレージ域ネットワーク) に保管されます。
* [R1Soft CDP](/docs/infrastructure/software?topic=software-ordering-r1soft#ordering-r1soft)。中央管理およびデータ・リポジトリーを備えた、ハイパフォーマンスのディスク間サーバー・バックアップを提供します。 R1Soft CDP は、ブロック・レベルでデータを保護します。サーバー上の固有のディスク・ブロックが保管されるのは、すべてのリカバリー・ポイントを通して 1 回のみのため、ストレージの効率が向上します。
