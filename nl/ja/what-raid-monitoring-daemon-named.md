---

copyright:
  years: 2017, 2019
lastupdated: "2018-05-22"

keywords: raid monitoring daemon

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# RAID モニタリング・デーモンの名前と場所
{: #bm-raid-monitoring-daemon}

{{site.data.keyword.cloud}} では、レガシー・ハードウェアのいくつかの例外を除き、主に Adaptec および LSI RAID カードを使用します。 以下の表に、RAID マネージャーの場所、モニターの場所、構成、および RAID アラート設定の概要を示します。

RAID カードの構成で SMTP サーバーおよび通知 E メールの宛先を変更することで、ポータル・モニタリング・プロセスをバイパスするように RAID アラートを構成できます。 これらの構成を変更した場合、IBM は RAID の問題を通知したり、解決されるまで問題を自動的に追跡したりすることができなくなります。 リスクを理解している場合を除き、提供されている構成を変更しないでください。

<caption>表 1. RAID 構成および設定</caption>

||LSI Linux|LSI Windows|Adaptec Linux|Adaptec Windows|
|---|---|---|---|---|
|**マネージャー名**|LSI MegaRAID Storage Manager|LSI MegaRAID Storage Manager|Adaptec Storage Manager|Adaptec Storage Manager|
|**マネージャーの場所**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**モニター名**|MR_Monitor|MRMonitor|Adaptec Event Manager|Adaptec Event Manager|
|**モニターの場所**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**プロセス名**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**ログの場所**|OS のデフォルトのメッセージ・ログの場所 (例えば、/var/log/messages)|GUI のみ|/usr/StorMan/RaidEvtA.log|GUI のみ|
|**通知 E メールの宛先**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**通知 E メールの送信元のフォーマット**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**E メールのポート**|25|25|25|25|
|**SMTP サーバー**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**代替通知オプション**|SMTP サーバーをローカル SMTP サーバーに変更する。 ローカル SMTP サーバーには、適切なファイアウォール構成が必要。|SMTP サーバーをローカル SMTP サーバーに変更する。 ローカル SMTP サーバーには、適切なファイアウォール構成が必要。|SMTP サーバーをローカル SMTP サーバーに変更する。 ローカル SMTP サーバーには、適切なファイアウォール構成が必要。|SMTP サーバーをローカル SMTP サーバーに変更する。 ローカル SMTP サーバーには、適切なファイアウォール構成が必要。|
