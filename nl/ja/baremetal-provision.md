---



copyright:
  years: 2017
lastupdated: "2017-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# ベア・メタル・サーバーのプロビジョン

## 始める前に
パブリック {{site.data.keyword.baremetal_long}} をプロビジョンするには、2 つのオプションがあります。1 つ目は {{site.data.keyword.cloud}} カタログを使用する方法で、2 つ目は {{site.data.keyword.slportal_full}}を使用する方法です。カタログと {{site.data.keyword.slportal}}には、固有のログイン ID が必要です。カタログのユーザー名とパスワードはポータルへのログインには使用できず、ポータルのユーザー名とパスワードはカタログのログインには使用できません。
{:shortdesc}

始める前に、{{site.data.keyword.cloud_notm}} カタログまたは {{site.data.keyword.slportal}}のいずれかの資格情報がセットアップされた状態にします。 
  
**注:** {{site.data.keyword.cloud_notm}} カタログの場合、{{site.data.keyword.baremetal_short}} を注文するには、アップグレードされたアカウントが必要です。アカウントのアップグレードについて詳しくは、『[IBMid への切り替え (Switching to IBMid)](https://console.ng.bluemix.net/docs/admin/softlayerlink.html)』を参照してください。
  
## ログイン 
{{site.data.keyword.cloud_notm}} カタログまたは {{site.data.keyword.slportal}}のいずれかを使用してログインしていることを確認します。 

  <table>
   <CAPTION>表 1. ログイン場所の選択</CAPTION>
   <THEAD>
   <TR>
   <th>以下を使用してログインする場合</th>
   <th>手順</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud カタログ</td>
   <td>
   <ol>
   <li>新しいブラウザー・ウィンドウを開き、<a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a> と入力します。</li>
   <li><b>「ログイン」</b>リンクをクリックします。</li>
   <li>ご使用の E メールまたは IBM ID を入力し、<b>「続行」</b>をクリックします。</li>
   <li>パスワードを入力し、<b>「ログイン」</b>をクリックします。</li>
   <li><b>「インフラストラクチャー」</b> > <b>「計算」</b>を選択します。</li>
   <li><b>「{{site.data.keyword.baremetal_short}}」</b>タイルをクリックします。</li>
   <li><b>「作成」</b>をクリックします。{{site.data.keyword.slportal}}のメインページが開きます。</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>カスタマー・ポータル</td>
   <td>
   <ol>
   <li>新しいブラウザー・ウィンドウを開き、<a href="https://control.softlayer.com">https://control.softlayer.com</a> と入力します。</li>
   <li>ユーザー名とパスワードを入力し、<b>「ログイン」</b>をクリックします。あるいは、<b>「IBM ID でログイン」</b>をクリックします。次に、ご使用の E メールまたは IBM ID を入力し、<b>「続行」</b>をクリックします。パスワードを入力し、<b>「ログイン」</b>をクリックします。{{site.data.keyword.slportal}}のメインページが開きます。</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## ベア・メタル・サーバーのプロビジョン
{: #ordering-baremetal-server}
ログイン後に、{{site.data.keyword.baremetal_short}} のプロビジョンを開始できます。{{site.data.keyword.baremetal_short}} をプロビジョンするには、**「デバイス」**メニューまたは**「デバイス」**アイコンを使用します。

### 「デバイス」アイコンを使用したベア・メタル・サーバーのプロビジョン
*「デバイス」*アイコンを使用して {{site.data.keyword.baremetal_short}} をプロビジョンするには、以下のステップを実行します。

1.  {{site.data.keyword.slportal}}から、**「注文」**セクションを見つけ、**「デバイス」**をクリックします。
2.  「デバイス」ページで、{{site.data.keyword.baremetal_short}} の下の**「時間単位」**または**「月単位」**をクリックします。
3.  ご使用の**データ・センター**を選択し、ページをスクロールして、**「開始価格 (Starting Price Per)」**リンクをクリックしてサーバーを選択します。 
4.  **「{{site.data.keyword.baremetal_short}} の構成」**ページで情報を入力し、**「注文に追加」**ボタンをクリックして続行します。サーバーの構成方法について詳しくは、『[{{site.data.keyword.baremetal_short}} の構成](.../bare-metal/configuring.md)』を参照してください。注文が確認されると、**「ご清算」**ページにリダイレクトされます。
5.  サーバーの**「拡張システム構成」**を入力します。このセットアップ方法について詳しくは、『[{{site.data.keyword.baremetal_short}} の構成](.../bare-metal/configuring.md)』を参照してください。
6.  **「クラウド・サービスのご利用条件」**チェック・ボックスと**「サード・パーティー・サービスのご使用条件」**チェック・ボックスをクリックします。
7.  支払情報を確認または入力し、**「注文の送信」**ボタンをクリックします。プロビジョニングの注文番号を含む画面にリダイレクトされます。この画面は、プロビジョニングの注文の受信を示すものでもあるため、印刷できます。

 一連の E メール (プロビジョニングの注文の確認応答、プロビジョニングの注文の承認と処理、およびプロビジョニングの完了) が管理者に送信されます。プロビジョニング完了の E メールには、{{site.data.keyword.cloud_notm}} にログイン後の*「デバイスの詳細」* ページへのリンクが含まれています。また、直接 {{site.data.keyword.slportal}}にログインすることもできます。

### 「デバイス」メニューを使用したベア・メタル・サーバーのプロビジョン
{: #ordering-baremetal-devices-menu}

メイン {{site.data.keyword.slportal}}・ページ上の*「デバイス」*メニューを使用して {{site.data.keyword.baremetal_short}} をプロビジョンすることもできます。 

1. **「デバイス」>「デバイス・リスト」**をクリックします。「デバイス」ページに、ユーザーのアカウント内のすべてのデバイス・タイプ (専用ホスト、仮想サーバー、ベア・メタル・サーバー、および NetScaler アプリケーション・デリバリー・コントローラー) が表示されます。
2. 右上隅の**「デバイスの注文」**リンクをクリックします。
3. 「SoftLayer の製品とサービスの注文」ページで、{{site.data.keyword.baremetal_short}} の下の**「時間単位」**または**「月単位」**をクリックします。
4. ご使用の**データ・センター**を選択し、ページをスクロールして、**「開始価格 (Starting Price Per)」**リンクをクリックしてサーバーを選択します。 
5.  **「{{site.data.keyword.baremetal_short}} の構成」**ページで情報を入力し、**「注文に追加」**ボタンをクリックして続行します。サーバーの構成方法について詳しくは、『[{{site.data.keyword.baremetal_short}} の構成](.../bare-metal/configuring.md)』を参照してください。注文が確認されると、**「ご清算」**ページにリダイレクトされます。
6.  サーバーの**「拡張システム構成」**を入力します。このセットアップ方法について詳しくは、『[{{site.data.keyword.baremetal_short}} の構成](.../bare-metal/configuring.md)』を参照してください。
7. **「クラウド・サービスのご利用条件」**チェック・ボックスと**「サード・パーティー・サービスのご使用条件」**チェック・ボックスをクリックします。
8. 支払情報を確認または入力し、**「注文の送信」**ボタンをクリックします。プロビジョニングの注文番号を含む画面にリダイレクトされます。この画面は、プロビジョニングの注文の受信を示すものでもあるため、印刷できます。

一連の E メール (プロビジョニングの注文の確認応答、プロビジョニングの注文の承認と処理、およびプロビジョニングの完了) が管理者に送信されます。プロビジョニング完了の E メールには、{{site.data.keyword.cloud_notm}} にログイン後の*「デバイスの詳細」* ページへのリンクが含まれています。また、直接 {{site.data.keyword.slportal}}にログインすることもできます。

### 次のステップ
{{site.data.keyword.baremetal_short}} のプロビジョン後に、その管理を開始できます。詳しくは、『[{{site.data.keyword.baremetal_short}} の管理](../bare-metal/managing.html)』を参照してください。
