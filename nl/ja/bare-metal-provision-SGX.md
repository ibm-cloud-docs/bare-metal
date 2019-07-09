---

copyright:
  years: 2018, 2019
lastupdated: "2018-04-02"

keywords: provision, sgx, provision server Intel SGX architecture, Intel SGX architecture

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Intel SGX アーキテクチャーを使用したベアメタル・サーバーのプロビジョニング
{: #bm-server-provision-sgx}

1. [カスタム・ベアメタル・サーバーの作成](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server)に記載されている手順を使用します。
* 注文書に記載されている以下のオプションを選択します。

|セクション|選択するオプション|
|------|------|
|サーバー|シングル・プロセッサー<br> Intel Xeon E3-1270 v6 (最大 4 台のドライブのストレージを搭載)|
|イメージ|- Windows Server 2016 Standard Edition (64 ビット)<br>- Windows Server 2016 Standard Edition (64 ビット)<br> - Windows Server 2016 Datacenter Edition (64 ビット) <br>- CentOS 7.x (64 ビット) <br> - Ubuntu Linux 16.04 LTS Xenial Xerus (64 ビット)<br>- CentOS 7.x (64 ビット) <br>- Red Hat Enterprise Linux 7.x (64 ビット) (プロセッサー・ライセンス)|
|イメージ・アドオン|Software Guard Extensions|
