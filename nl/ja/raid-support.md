---

copyright:
  years: 1994, 2019
lastupdated: "2018-5-31"

keywords: raid support, raid help

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# RAID サポート・チケット情報
{:# bm-raid-support-ticket}

ベアメタル・サーバーでの RAID の使用に関する問題や質問については、[IBM developerWorks dW に関する回答](https://developer.ibm.com/answers/topics/ibm-cloud/){:new_window}フォーラムをご覧になると、回答が見つかる場合があります。
さらに、サポート・チケットを開くこともできます。サポート・チケットについては、[サポート・チケットを開く](https://test.cloud.ibm.com/docs/get-support?topic=get-support-getting-customer-support#open-ticket){:new_window}を参照してください。
{:shortdesc}

<!--During a drive or RAID failure, support tickets are automatically created. You can create a support ticket for other problems.--> サポート・チケットを作成するときには、RAID ログ・ファイルを提供する必要があります。RAID ログ・ファイルにある情報は、失われた RAID 構成をリカバリーするために不可欠です。ログ・ファイルを提供すると、サポート・チームがドライブ順序、アレイのメンバーシップ、アレイの形状、およびケーブル接続の問題を特定する際に役立ちます。 使用している RAID コントローラーのタイプ (Adaptec または LSI) に応じて、以下のコマンドを使用して RAID ログ・ファイルを取得します。

**注:** 初期の更新時に再始動または電源オフの許可を与えるか、ドライブをホット・スワップするように依頼すると、サポート・チケット・プロセスが高速化されます。

<b>Adaptec RAID カード</b><br>
Adaptec RAID カードのログ・ファイルを取得するには、以下のコマンドを使用します。このログ・ファイルの出力全体をサポート・チケットに必ず含めてください。

`arcconf getconfig 1/arcconf getlogs 1 device tabular`.

<b>LSI RAID カード</b><br>
LSI RAID カードのログ・ファイルを取得するには、以下のコマンドを使用します。 これらのログ・ファイルの完全な出力をサポート・チケットに含める必要があります。
```/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
**重要:** トラブルシューティングを開始する前に、作業内容を必ずバックアップしてください。
