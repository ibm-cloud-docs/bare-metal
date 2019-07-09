---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-02"

keywords: provision Intel Optane compatible bare metal server, Intel Optane, optane 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Intel Optane 互換ベアメタル・サーバーのプロビジョニング
{: #bm-provision-optane-server}

Intel Optane ドライブを搭載したベアメタル・サーバーをプロビジョンするには、以下のようにします。
1. [カスタム・ベアメタル・サーバーの作成](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server)に記載されている手順を使用します。
* 注文書に記載されている以下のオプションを選択します。

|セクション|選択するオプション
|------|------|
|地域データ・センター|Intel Optane ドライブを使用するには、以下のいずれかのデータ・センターを選択します。<br>ヨーロッパ - AMS03、FRA02、LON02、OSL01<br>北米南 DAL09、DAL10、DAL12<br>アジア太平洋 - MEL01<br>北米東 - MON01、TOR01、WDC04<br>北米西 - SJC03<br>|
|サーバー|1.**「すべてのサーバー」**を選択します。<br>2.*「デュアル・プロセッサー」*を選択します。<br>3. 次のいずれかのサーバーを選択します。<br>-Intel Xeon 4110 (最大 12 ドライブ)<br>-Intel Xeon 5120 (最大 12 ドライブ搭載)<br>-Intel Xeon 6140 (最大 12 ドライブ搭載)<br>-Intel Xeon E5-2620 v4 (GPU サポートあり)<br>-Intel Xeon E5-2650 v4 (GPU サポートあり)<br>-Intel Xeon E5-2690 v4 (GPU サポートあり)<br><br>  **注**: E5-2620 v4、E5-2650 v4、または E5-2650 v4 を選択すると、GPU に代わって その Intel Optane ドライブが使用されるため、GPU と Intel Optane ドライブの両方を持つことはできません。|
|オペレーティング・システム|Intel 提供の Optane ドライバーについては、以下のオペレーティング・システムが Intel によって認定されています。<br>Windows Server 2016 (すべてのエディション)<br>Windows Server 2012 R2 (すべてのエディション)<br><br>インボックスでオープン・ソースの非 Intel ドライバーの場合、互換性と機能性は検証されていますが、認証されているわけではありません。<br>Red Hat Enterprise Linux 7.x (64 ビット)<br>Red Hat Enterprise Linux 6.x (64 ビット)。
|イメージ・アドオン| 最初の PCIe コンポーネントと 2 番目の PCIe コンポーネントのいずれかまたは両方の Intel Optane ドライブを選択します。|
