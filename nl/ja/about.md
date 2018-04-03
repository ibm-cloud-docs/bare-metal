---



copyright:
  years: 2016
lastupdated: "2016-01-19"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# {{site.data.keyword.baremetal_short}} 入門

{{site.data.keyword.baremetal_long}} は、パフォーマンスと制御の機能を提供します。{{site.data.keyword.baremetal_short}} は、ハイパーバイザーで実行されず、ハードウェア・リースに対する低レベルのアクセスが可能です。また、サーバーを共有する他のお客様が存在せず、専用で使用することになります。
{:shortdesc}

{{site.data.keyword.baremetal_short}} を作成する際には、プロセッサーや地域からオペレーティング・システムやハード・ディスクに至る各種仕様をカスタマイズできます。

{{site.data.keyword.baremetal_short}} をプロビジョンするには、以下のようにします。
  1. **「計算」>「{{site.data.keyword.baremetal_short}}**」に移動し、**「追加」**をクリックします。
  2. {{site.data.keyword.baremetal_short}} インスタンスをプロビジョンする場所を選択します。これは、{{site.data.keyword.Bluemix}} 地域のいずれかのデータ・センターです。
  3. サーバーの構成を選択します。この構成は、このインスタンスで作成されたすべてのサーバーに適用されます。
  4. このインスタンスで作成するサーバーの数を選択します。サーバーごとに固有のホスト名を入力します。
  5. **オプション:** サーバーを構成するために定義したスクリプトまたはテキスト・ファイルの URL を入力します。プロビジョニング・スクリプトでは、HTTPS プロトコルを使用する必要があります。スクリプトは、インスタンスのプロビジョン後にダウンロードされて実行されます (可能な場合)。URL が実行可能スクリプトに関連付けられていない場合、スクリプトは単にダウンロードされます。
  6. サーバーのオペレーティング・システムを選択します。このオペレーティング・システムは、このインスタンスで作成されたすべてのサーバーに適用されます。

1 時間以内に、{{site.data.keyword.baremetal_short}} がプロビジョンされ、使用可能になります。
