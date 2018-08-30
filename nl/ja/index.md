---



copyright:
  years: 2018, 2018
lastupdated: "2018-06-18"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# ベア・メタル・サーバーの概説
{: #getting-started}

{{site.data.keyword.baremetal_long}} は、ハードウェア・リソースへの下位レベルのアクセス権限によりパフォーマンスと制御の機能を提供する、シングル・テナントの物理サーバーです。サーバーは自分専用のサーバーであり、「他のユーザー」とは共有されません。
{: shortdesc}

表 1 には、{{site.data.keyword.baremetal_short}} を即時にプロビジョンおよび構成するためのステップが記載されています。
<table>
   <CAPTION>表 1. クイック・スタート・ステップ</CAPTION>
   <THEAD>
   <TR>
   <th>タスク</th>
   <th>詳細</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>1. 実装環境に役立つコンテンツを確認する</td>
   <td>IBM Cloud およびベアメタル・サーバーを初めてご利用になる場合、以下のサイトに、ご使用の環境を計画するために役立つ有益な情報が記載されています。
   <li><a href="https://ibm.com/cloud-computing/">IBM Cloud とは</a></li>
   <li><a href="https://ibm.com/cloud/get-started">Getting started with IBM Cloud</a></li>
   <li><a href="https://www.ibm.com/cloud/bare-metal-servers">Bare Metal Servers</a></li>
   </td>
 <tr>
   <td>2. IBM Cloud に登録する</td>
   <td><a href="https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-ibm-cloud">IBM Cloud への登録</a>には、IBM Cloud アカウントのセットアップ手順が記載されています。</td>
 <tr>
   <td>3. ワークロード仕様を決定する</td>
   <td>サーバーをプロビジョンする前に、サーバーが使用される方法と、正常にプロビジョンされるために必要なサーバーのサイズを決定します。例えば、開発およびテスト用途ですか、それとも実動用途ですか? ユーザー・エクスペリエンスをテストしますか、長いアルゴリズムを処理しますか、データをバックアップおよびリストアしますか、待ち時間の速度を向上させますか?</td>  
 <tr>
   <td>4. サーバーのサイズとコストを見積もる</td>
   <td><a href="https://www.ibm.com/cloud-computing/bluemix/bare-metal-search">ベアメタル検索ツール</a>を使用すると、サーバーのサイズとコストを見積もることができます。</td>
 <tr>
   <td>5. IBM Cloud アカウントにログインする</td>
   <td>IBM Cloud カタログまたは IBM Cloud インフラストラクチャー・カスタマー・ポータルのいずれかからベアメタル・サーバー注文フォームにアクセスできます。カタログおよびインフラストラクチャー・カスタマー・ポータルにアクセスするには、<a href="https://console.bluemix.net/docs/customer-portal/getting-started.html#getting-started">IBM ID とパスワード</a>が必要です。
   <li><a href="https://console.bluemix.net/catalog/">IBM Cloud カタログ</a></li>
   <li><a href="https://control.softlayer.com">IBM Cloud インフラストラクチャー・カスタマー・ポータル</a></li>  
   </td>   
<tr>   
   <td>6. サーバーをプロビジョンする</td>
   <td>サーバーのプロビジョンに関しては、ポピュラー、カスタム、および SAP 認定の 3 つのオプションがあります。ポピュラー・サーバーは、ほとんどの顧客のニーズを満たし、プロビジョン後に 30 分から 40 分で構成準備が整う、事前構成されたサーバーです。 
   
     
<br>カスタム・サーバーは、ニーズを満たすために、特定のコンピュート、接続、ストレージ、およびネットワークの各オプションを選択することで作成するサーバーです。カスタム・サーバーのプロビジョンには長時間 (通常は 2 時間から 4 時間) かかり、運用コストが高いことに注意してください。また、<a href="bm_provision_ssd.html">Intel Optane 互換のベアメタル・サーバーをプロビジョン</a>するか、<a href="bare-metal-provision-SGX.html">Intel SGX アーキテクチャー</a>搭載のベアメタル・サーバーをプロビジョンするオプションもあります。 
     
<br>SAP 認定サーバーは、SAP HANA および SAP NetWeaver のランドスケープをサポートするために特別に認定されています。
該当タイプのサーバーに関するプロビジョニング情報に移動するリンクを使用してください。SAP 認定サーバーでは、プロビジョンするランドスケープのタイプ (SAP HANA または SAP NetWeaver) を選択する必要があることに注意してください。  
  <li><a href="baremetal-provision-popular.html">高速プロビジョン・ベアメタル・サーバー</a></li>
  <li><a href="baremetal-provision.html">カスタム・ベアメタル・サーバー</a></li>
  <li><a href="bare-metal-sap-applications.html">IBM Cloud SAP 認定インフラストラクチャー </a></li>
  </td>
 <tr>
   <td>7. ベアメタル・サーバーを構成する</td>
   <td>これで、サーバーを構成する準備ができました。『*構成*』のトピックを参照してください。</td>
   </td>
   </tr>
   </TBODY>
   </table>
