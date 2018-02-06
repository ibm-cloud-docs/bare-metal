---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# ベア・メタル・サーバーへの Ubuntu サーバーのインストール

{{site.data.keyword.IBM&reg; Cloud}} で提供されていないオペレーティング・システムを使用する場合、カスタム ISO (ディスク・イメージ) をマウントすることで、ベア・メタル・サーバーにそのオペレーティング・システムをインストールできます。ISO をマウントするには、サーバーに関連付けられているファイル・ストレージ (NAS) にその ISO をアップロードします。ISO を NAS にアップロードするには、以下の手順を使用して、IPMI で ISO をマウントします。
1. **「オペレーティング・システムなし」**を指定して、ベア・メタル・サーバーを注文します。 
* NAS への接続に使用できるオペレーティング・システムとして無料の OS (例えば、CentOS) を選択することもできます。
* ブート可能 ISO を保管するための NAS ストレージを注文します。既に Windows CIFS サーバーを所有している場合は、それを使用して ISO イメージを共有できます。その Windows CIFS サーバーを使用して、20GB 容量のレガシー NAS を取得することになります。NAS のプロビジョン後、カスタマー・ポータルから NAS の説明を確認できます。
* ISO イメージを https://www.ubuntu.com/download/server からダウンロードします。
* ISO イメージを NAS または Windows CIFS サーバーにアップロードします。NAS ストレージがあれば、FTP を使用して ISO イメージ・ファイルをアップロードできます。

  サンプル FTP 手順:
  ```
  #ftp <nas address>.service.softlayer.com
  Connected to <nas address>.service.softlayer.com
  220 NAS FTP Service
  User (<nas address>.service.softlayer.com:(none)): <nas username>
  331 Please specify the password.
  Password: <nas password>
  230 Login successful.
  ftp> bin
  200 Switching to Binary mode
  ftp> put <iso imagefile name>.iso
  200 PORT command successful. Consider using PASV.
  150 Ok to send data.
  226 Transfer complete.
  ftp: 3170893824 bytes sent in 253.86 Seconds 12490.77Kbytes/sec.
  ```
  
* IPMI を使用して、{{site.data.keyword.Bluemix_notm}} への VPN 接続を確立します。「サポート」メニューまたは URL ([VPN アクセス](http://www.softlayer.com/VPN-Access)) から VPN メニューを起動できます。
* 管理 IP を介した IPMI への接続を使用して、IPMI の「仮想メディア (Virtual Media)」メニューから ISO イメージをマウントします。
  1. IPMI 資格情報を表示します。
  * IPMI ビューにログインします。
  * 「仮想メディア (Virtual Media)」タブを開きます。
  * IPMI での管理者特権を備えている root ユーザーが必要です。特権が*オペレーター* と表示されている場合は、特権を管理者に変更するためのサポート・チケットをオープンします。
  * ISO イメージの接続の詳細を入力します。
    共有ホスト (Share host) = NAS の IP アドレス<br/例: 10.3.x.x。
    イメージのパス (Path to image) = ISO ファイルの名前。フォーマット: \NASusername\imagefilesname.iso (つまり、\SLNxxxxxx\SLE-12-SP1-Server-DVD-x86_64-GM-DVD1.iso)
    ユーザー = NAS のユーザー名
    パスワード = NAS のパスワード
  * **「マウント (Mount)」**ボタンをクリックします。
  * デバイスを確認します。
* KVM ビューアーをクリックして起動し、「仮想メディア (Virtual Media)」メニューから「仮想ストレージ (Virtual Storage)」ページを開きます。CD-ROM デバイスとして ISO イメージを正常にマウントできた場合、**「接続状況履歴 (Connection Status History)」**にデバイスの説明が表示されます。
* SoftLayer チケットを使用して、サーバーが最初のデバイスとして仮想 CD-ROM をブートするように要求します。サーバーごとにこの要求を行います。ブート設定は、OSのインストール後に変更します。
  **注**: BIOS でブート順序を変更するためにサポートに連絡する必要が生じない場合があります。これは、ご使用のサーバーによって異なります。ブート順序を確認するために、一度リブートを試行してください。
* KVM ビューからサーバーをリブートします。
* マウントされた ISO イメージから OS をインストールします。
* ISO からベア・メタル・サーバーに Ubuntu OS をインストールします。
* ネットワーク設定 (IP アドレス/サブネット/ゲートウェイ/DNS など) を構成します。インストール・ステップで正しく構成しなかった場合、リブート後に KVM コンソールを介してのみ、このサーバーに接続できます。

* 仮想メディアをアンマウントします。IPMI の「仮想メディア (Virtual Media)」タブを使用して、サーバーから仮想メディアをアンマウントする必要があります。
* サーバーをリブートします。
* リブート後、SSH を介してサーバーにアクセスできます。
