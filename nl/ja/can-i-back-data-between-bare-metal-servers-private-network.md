---

copyright:
  years: 1994, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# バックアップおよびリカバリー

{{site.data.keyword.Bluemix_notm}} は、お客様のバックアップ要件を満たすために、各種のスケーラブルな[バックアップおよびストレージ用ソリューション ](https://www.softlayer.com/cloud-storage) を提供します。 ただし、{{site.data.keyword.Bluemix_notm}} では、お客様のデバイスのバックアップは実行しません。お客様のデバイスでのすべてのスケジュールされたバックアップおよび 1 回限りのバックアップは、アカウントのユーザーが開始する必要があります。

1 つのアカウントで 2 つ以上の {{site.data.keyword.baremetal_short}} が存在している場合、1 つのデバイスからのデータを別のデバイスにバックアップできます。 プライベート・ネットワークのトラフィックについては帯域幅に制限が課されていないので、アカウントが共有されているデバイス同士なら、随時、任意のデバイスにデータを転送またはバックアップすることができます。{{site.data.keyword.baremetal_short}} では、以下に示すソリューションを含めて、いくつかのバックアップ・ソリューションが使用可能です。

1. [Evault Backup](../infrastructure/backup/index.html)。複数のサーバーでのバックアップを自動化できるエンタープライズ・バックアップ・ソリューションです。 データは、エンタープライズ SAN (ストレージ域ネットワーク) に保管されます。
* [Network Attached Storage (NAS)](../infrastructure/network-attached-storage/nas.html)。業界標準であり、重要なデータのサーバー外でのストレージを提供します。 データは、エンタープライズ SAN (ストレージ域ネットワーク) に保管されます。
* [R1Soft CDP](../infrastructure/backup/r1soft.html)。中央管理およびデータ・リポジトリーを備えた、ハイパフォーマンスのディスク間サーバー・バックアップを提供します。 R1Soft CDP は、ブロック・レベルでデータを保護します。サーバー上の固有のディスク・ブロックが保管されるのは、すべてのリカバリー・ポイントを通して 1 回のみのため、ストレージの効率が向上します。
