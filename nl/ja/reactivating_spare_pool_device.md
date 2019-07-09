---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

keywords: bare metal reactivate spare pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# スペア・プールからのデバイスの再アクティブ化
{: #bm-reactivating-spare-pools}

デバイスがスペア・プールに追加されると、「デバイス・リスト」内のそのデバイスの状況は、デバイスが標準の対話に適格であることを示す「アクティブ」から「スペア・プール」に変更されます。 ス
ペア・プールに含まれるデバイスはその機能専用であり、
他のデバイスのように従来の日常のアクションには使用できません。デバイスをスペア・プールから削除して従来の機能に戻るようにするには、
再アクティブ化する必要があります。{:shortdesc}

## スペア・プールからのデバイスの再アクティブ化

1. ユーザー固有の資格情報を使用して、[{{site.data.keyword.cloud}} ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://cloud.ibm.com/){: new_window} にアクセスします。
2. ナビゲーション・バーから**「デバイス」>「スペア・プール」**を選択して、*「スペア・プール」*画面にアクセスします。
3. 目的のデバイスの**「アクション」>「デバイスの再アクティブ化」**を選択します。
4. サーバーを再アクティブ化するには、**「はい」**をクリックします。 このアクションをキャンセルするには、**「いいえ」**をクリックします。

## 次のステップ
再アクティブ化プロセスを開始すると、デバイスはオフラインになり、ファームウェアが更新され、デバイスは通常の用途に使用可能になります。 再アクティブ化プロセスは約 1 時間かかります。 スペア・プールから削除されたデバイスは、フェイルオーバー方式として使用するには適格ではなくなります。 このデバイスは、スペア・プールに再度追加することでいつでもスペア・プールに戻すことができます。 詳しくは、[スペア・プールへのデバイスの追加 (Adding a device to the spare pool) ](/docs/bare-metal?topic=bare-metal-adding-spare-pools#adding-spare-pools)を参照してください。
