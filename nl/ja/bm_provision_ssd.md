---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Intel Optane 互換ベアメタル・サーバーのプロビジョニング
Intel Optane ドライブを搭載したベアメタル・サーバーをプロビジョンするには、以下のようにします。
1. [カスタム・ベアメタル・サーバーの作成](../bare-metal/baremetal-provision.html)に記載されている手順を使用します。
* 注文書に記載されている以下のオプションを選択します。

|セクション|選択するオプション
|------|------|
|データ・センター|Intel Optane ドライブを使用するには、以下のいずれかのデータ・センターを選択します。<br>AMS03 - アムステルダム<br>DAL09 - ダラス<br>DAL10 - ダラス<br>DAL12 - ダラス<br>FRA02 - フランクフルト<br>LON02 - ロンドン<br>MEL01 - メルボルン<br>MON01 - モントリオール<br>OSL01 - オスロ<br>SJC03 - サンノゼ<br>TOR01 - トロント<br>WDC04 - ワシントンDC|
|サーバー|以下のサーバーは Intel Optane ドライブと互換性があります<br>Intel Xeon 4110 (最大 12 ドライブ搭載)<br>Intel Xeon 5120 (最大 12 ドライブ搭載)<br>Intel Xeon 6140 (最大 12 ドライブ搭載)<br>Intel Xeon E5-2620 v4 (GPU サポートあり)<br>Intel Xeon E5-2650 v4 (GPU サポートあり)<br>Intel Xeon E5-2690 v4 (GPU サポートあり)<br><br>  **注**: E5-2620 v4、E5-2650 v4、または E5-2650 v4 を選択すると、GPU に代わって その Intel Optane ドライブが使用されるため、GPU と Intel Optane ドライブの両方を持つことはできません。|
|PCIe コンポーネント|最初の PCIe コンポーネントと 2 番目の PCIe コンポーネントのいずれかまたは両方の Intel Optane ドライブを選択します。|
|オペレーティング・システム|Intel 提供の Optane ドライバーについては、以下のオペレーティング・システムが Intel によって認定されています。<br>Windows Server 2016 (すべてのエディション)<br>Windows Server 2012 R2 (すべてのエディション)<br><br>インボックスでオープン・ソースの非 Intel ドライバーの場合、互換性と機能性は検証されていますが、認証されているわけではありません。<br>Red Hat Enterprise Linux 7.x (64 ビット)<br>Red Hat Enterprise Linux 6.x (64 ビット)。
