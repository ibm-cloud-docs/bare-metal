---
copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# ベア・メタル・サーバーでの ISO のマウント

## 概説

ほとんどの {{site.data.keyword.Bluemix_notm}} のお客様は、サーバーに付属している標準オペレーティング・システムのいずれかを使用しますが、サーバーでカスタム ISO (ディスク・イメージ) をマウントすることもできます。 カスタム ISO をマウントするための 3 つのオプションがあります。

ここで説明する方法を行うには、SL VPN サービス (例えば、[SoftLayer SSL VPN Portal - AMS01](https://vpn.ams01.softlayer.com/prx/000/http/localhost/login)) を介して、またはネットワークに既に接続している別のサーバーを介して、プライベート・ネットワークに接続されている必要があります。

**注:** 50 MB より大きい Lenovo ハードウェア・ディスク・イメージは、IMM コンソール・インターフェース > 「メディア (media)」タブを使用してマウントする必要があります。

## オプション 1 (推奨): IPMI の使用 (CIFS 共有上の ISO)

{{site.data.keyword.Bluemix_notm}} にデプロイされているインフラストラクチャーが既にある場合は、CIFS 共有を内部ネットワークに提供するように既存のサーバーを構成できます。 その後、そこにある任意の ISO をベア・メタル・サーバーにマウントできます。

これは、ベア・メタル・サーバーにカスタム OS をインストールするための推奨される方法です。理由は、ローカル・ネットワークを介してインストールされるため、非常に高速であり、ログアウトしたり、管理インターフェースから切断されたりした場合でも、ISO をマウントしたままに保つことができるからです。

CIFS 共有からカスタム OS をインストールするには、以下のステップに従います。

1. CIFS 共有に ISO を配置したことを確認します。
* https://control.softlayer.com/ の「デバイス」-> ご使用のサーバー (「デバイスの詳細」) ->「リモート管理」で示されている IP を Web ブラウザーで指定し、IPMI 管理コンソールにログインします。ユーザー名とパスワードも同じ場所に示されています。
* **「仮想メディア (Virtual Media)」**の上にカーソルを移動し、**「CD-ROM イメージ (CD-ROM image)」**をクリックします。
* 該当する詳細を入力し、**「保存してマウント (Save and Mount)」**をクリックします。
* サーバーの BIOS を変更するための許可をすべてのユーザーが備えているわけではありません。 必要な場合は、サポートに対するチケットをオープンして、以下を要求できます。
  * IPMI での root ユーザー管理者特権 (仮想メディア接続モードを変更できるようにするため)
  * ブート・シーケンスを変更し、「IPMI 仮想ディスク (IPMI Virtual Disk)」を最初のブート・オプションにすること
* 上記の変更の完了後、IPMI 管理コンソールに戻り、「構成 (configuration)」->「リモート・セッション (Remote session)」に移動し、接続モードを**「接続 (attach)」**に変更します。 一部の古い IPMI コンソールでは、このオプションをスキップできます。
* サーバーをリブートし、仮想メディアからブートします。


## オプション 2: IPMIView の使用 (CIFS 共有上の ISO)

前提条件:<br/>
* ブート可能 ISO がある
* ブート可能 ISO を保管するための Windows CIFS サーバーまたは NAS ストレージがある
* サーバーに関連付けられているファイル・ストレージ (NAS) に ISO がアップロードされている
* IPMIView がインストールされているか、KVM コンソールにアクセスできる <!--  * http://knowledgelayer.softlayer.com/procedure/download-ipmiview
* http://knowledgelayer.softlayer.com/procedure/access-kvm-console -->
* wget を使用して ISO ファイルをダウンロードできる
* SSH にアクセスでき、パッケージにアクセスしてインストールするための特権およびマウントを作成するための特権がある


### Linux および Windows
IPMIView で ISO をマウントするには、以下のステップに従います。
1. サポート・チケットを使用して、サーバーで最初のデバイスとして仮想 CD-ROM をブートするように要求します。 各デバイスは、関連付けられている仮想 CD-ROM からブートする必要があります。 この設定は、OS のインストール後に元に戻すことができます。
* [VPN](http://www.softlayer.com/VPN-Access) への VPN 接続を確立します。 Microsoft Internet Explorer を使用している場合は、必ず「信頼済みサイト」リストに .softlayer.com を含め、JAVA を最新の状態にしてください。
* ISO メディアを NAS または Windows CIFS サーバーにコピーします。
  * SSH を使用して Linux ジャンプ・ボックスに接続します。
  * 以下のように、Linux ジャンプ・ボックスで NAS 共有をマウントします。

        mkdir /mnt/nasmount
        mount -t cifs //NAS_SERVER_NAME_ORIP/SLN#####-2 -o username=SLN#####-2,
        password=NAS_STORAGE_PW,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755 /mnt/nasmount
  * mount コマンドのパラメーターのキーは、以下のとおりです。
        NAS_SERVER_NAME_ORIP = NAS ストレージの名前または IP。
        /SLN#####-2 = NAS ストレージに接続するためのユーザー名とフォルダー名。
        NAS_STORAGE_PW = NAS ストレージのパスワード。
        /mnt/nasmount = NAS ストレージをマウントするフォルダー。
  * ディレクトリーを新規 NAS マウント・フォルダーに変更します。
        cd /mnt/nasmount
  * wget を使用して iso ファイルをダウンロードします。
        wget http://www.linktoyouriso.com/isofilename.iso
  ダウンロードが成功したことを示す確認が表示されます。
* 以下の場所から IPMI View をダウンロードします。
      http://knowledgelayer.softlayer.com/procedure/download-ipmiview
* 管理 IP を介してサーバーに接続します。
      http://knowledgelayer.softlayer.com/procedure/log-ipmiview
      http://knowledgelayer.softlayer.com/procedure/view-ipmi-credentials
* 「仮想メディア (Virtual Media)」タブを開きます。
* CD-ROM イメージの接続の詳細を入力します。
  *
    * 共有ホスト (Share host) = NAS ストレージの IP アドレス。 この値を確認するには、NAS ストレージ・サーバー名に ping します。 例えば、_ping nas501.service.softlayer.com_ などです。
    * 共有名 (Share Name) = NAS ストレージのユーザー名
    * イメージのパス (Path to image) = 以下の形式の ISO ファイルの名前:
          \NASusername\isoname.iso (つまり、\SLN123456\centos6.iso)
    * ユーザー = NAS ストレージのユーザー名
    * パスワード = NAS ストレージのパスワード
* サーバーをリブートします。
* KVM コンソール・ビューを開きます。
* システム・プロンプトに従って、ブート可能 ISO をブートします。
* OS をインストールします。
* 仮想メディアをアンマウントします。
* サーバーを再始動します。

## オプション 3: ローカル・コンピューターからの ISO のマウント
<a name="option3"></a>

Java iKVM ビューアー (コンソール) を使用して、ローカル・コンピューターから ISO をマウントできます。 これにより、コンソールに接続した状態で ISO をマウントできます。 インストールの進行速度は、ご使用のインターネット接続のアップロード速度と待ち時間、Java とご使用のコンピューターのパフォーマンスによって異なる可能性があります。

サーバーで BIOS を変更する許可がない場合は、サポートに対するチケットをオープンし、以下の変更を要求します。
* IPMI での root ユーザー管理者特権 (仮想メディア接続モードを変更できるようにするため)
* ブート・シーケンスを変更し、「IPMI 仮想ディスク (IPMI Virtual Disk)」を最初のブート・オプションにすること (ISO はまだマウントされていないため、この時点では、サポートは、ブート・デバイスの優先順位のみを変更します)


1. https://control.softlayer.com/ で示されている IP を Web ブラウザーで指定して、IPMI 管理コンソールにログインします。
* 「デバイス」> ご使用のサーバー (「デバイスの詳細」) >「リモート管理」をクリックします。 ユーザー名とパスワードを指定します。
* 「構成」>「リモート・セッション (Remote session)」をクリックし、接続モードを**「接続 (attach)」**に変更します。 一部の古い IPMI コンソールでは、このオプションは使用可能でないため、このステップをスキップできます。
* 「システム」>「システム情報」をクリックして、システム情報ページに戻ります。コンソール・ウィンドウ・アイコンが表示されます。
* コンソール・アイコンをクリックしてコンソールを開きます。 すべてのセキュリティー警告を受け入れます。
* コンソールが接続されると、ログイン・プロンプトが表示されます。
* 「仮想メディア (Virtual Media」>「仮想ストレージ (Virtual Storage)」をクリックします。
* **「CDROM&ISO」**タブに移動し、**「論理ドライブ・タイプ (Logical Drive Type)」**の下の ISO ファイルを選択します。
* **「イメージを開く (Open Image)」**をクリックし、ローカル・コンピューター上の ISO を選択します。
* **「プラグイン (Plug in)」**をクリックし、ISO を仮想 CD-ROM ドライブに挿入します。
* **「OK」**をクリックします。
* サーバーをリブートし、**仮想 CD-ROM ドライブからブートする**オプションを使用します。 ブート・デバイスを選択するには、iKVM ビューアーで仮想キーボードを使用する必要が生じることがあります。

## トラブルシューティング

* すべてのユーザーに、デフォルトで仮想メディアをマウントするためのアクセス権限があるわけではありません。 許可エラーが発生した場合は、Root IPMI ユーザー許可の更新についてサポートにお問い合わせください。
* ISO が既にマウントされている場合は、**「There is a disk mounted」**というテキストのエラー・メッセージが表示されます。 既存のディスクをアンマウントして、新しい ISO で置き換える必要があります。 2 つの ISO を同時にマウントすることはできません。
* BIOS でブート順序を変更するためにサポートに連絡する必要が生じる場合があります。
* ISO をマウントする際には、PPTP VPN ではなく、SSL VPN (http://vpn.softlayer.com) を使用してください。  VPN ネットワークに接続されると、IPMI アドレス (https://<private-ip-IPMI-management>) を使用してシステムの IPMI にアクセスすることもできるようになります。
* ISO のパスを入力する際には、パスに UNC 名前構文 (汎用命名規則) を使用します。例:
  _\\<NAS username>\<isoname>.iso_
