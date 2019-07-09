---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: bare metal, no os, no operating system

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# OS なしオプション
{: #bm-no-os}

**「OS なし」**は、オペレーティング・システムなしの {{site.data.keyword.baremetal_long}} を注文するためのオプションです。

## OS なしの {{site.data.keyword.baremetal_short}} の注文
{: #ordering-no-os}

1. [カスタム・ベアメタル・サーバーの作成](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server)に記載されている手順を使用して、サーバーを注文します。
2. **「イメージ」**の下の**「OS なし」**を選択します。
3. サーバーの注文手順を完了します。 

## 「OS なし」への変更
{: #changing-to-no-os}

OS を持たないようにサーバーを再構成できます。再構成は OS 再ロードによって行われます。詳しくは、[OS の再ロード](/docs/infrastructure/software?topic=software-reloading-the-os)を参照してください。

1. **「デバイス」** > **「デバイス・リスト」**をクリックします。
2. OS なしで再構成するサーバーを選択します。
3. **「OS 再ロード」**をクリックし、該当する情報を入力します。

## OS がないサーバーでのオペレーティング・システムのインストール
{: #installing-os-on-no-os-server}

オペレーティング・システムを持たない {{site.data.keyword.baremetal_short}} にオペレーティング・システムをインストールする方法は 2 つあります。

### オプション 1: PXE サーバー
{: #option-1}

PXE セットアップから OS をブートしてロードするように、オペレーティング・システムなしの {{site.data.keyword.baremetal_short}} をセットアップできます。<!--(see [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) for more information)-->PXE セットアップを持つネットワーク環境に{{site.data.keyword.baremetal_short}}をデプロイして (通常、このために DHCP および TFTP デーモンを実行します)、ネットワーク・アダプターからブートするように新規サーバーの BIOS を構成します。 OS オプションが正しく機能しない場合、PXE セットアップを{{site.data.keyword.baremetal_short}}と同じ VLAN 内に配置するか、DHCP フォワードを使用する必要があります。

このオプションを機能させるには、スイッチ・ポートを基本モードで再グループ化するように要求するサポート・チケットをオープンしなければならない場合があります。 これは、冗長性を提供する標準的な機能となっているリンク集約 (LACP)<!--see [Link Aggregation](http://en.wikipedia.org/wiki/Link_aggregation))--> との互換性が、PXE プロトコルでは不要だからです。別のオプションとしては、未結合アップリンクを備えたサーバー (リンク集約なし) を注文し、OS のインストール後にそれらのアップリンクを冗長アップリンクに変更するという方法があります。
{: note}

### オプション 2: IPMI デバイス
{: #option-2}

含まれている IPMI デバイスを介して ISO からブートすることで、オペレーティング・システムのない {{site.data.keyword.baremetal_short}} にオペレーティング・システムをインストールします。ISO からのブートについて詳しくは、[ベアメタル・サーバーでの ISO のマウント](/docs/bare-metal?topic=bare-metal-mounting-an-iso-on-a-bare-metal-server)を参照してください。
