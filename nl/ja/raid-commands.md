---
copyright:
  years: 1994, 2018
lastupdated: "2018-5-10"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID コントローラー・コマンド

RAID コントローラー・コマンドを実行するには、Adapatec コマンド・ライン・ユーティリティーを使用します。
以下に、使用できる最も一般的な RAID コントローラー・コマンドを示します。
{:shortdesc}

**注:** Windows および VMware では、storcli コマンドを実行するためのパスが異なります。正しいコマンド・パスについては、以下の例を参照してください。

Windows (CMD を使用)
`C:\Program Files (x86)\MegaRAID Storage Manager>`      
または
`C:\Program Files\LSIStorCli>`

VMware (storcli コマンドを実行する前に、storcli をインストールする必要があります)
`/opt/lsi/storcli/`

## 一般的な RAID コントローラー・コマンド

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_ は、操作のタイプ、論理ドライブ番号、論理ドライブ・サイズ、および操作の進行をリストします。以下の項目など、実行されているバックグラウンド・コマンドの状況を表示することもできます。
<ul>
  <li> 最新の再ビルド
  <li> 同期
  <li> 論理ドライブのマイグレーション
  <li> 圧縮/拡張
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1</b></code> <br>
_GETCONFIG_ は、コントローラー、論理ドライブ、および物理ドライブに関する情報をリストします。以下の項目などの情報を表示できます。
<ul>
  <li> コントローラー・タイプ
  <li> BIOS、ブート・ブロック、デバイス・ドライバー、およびファームウェアのバージョン
  <li> 物理デバイス・タイプ、デバイス ID、PFA の存在
<li> 物理デバイスの状態
  <li> 格納装置の情報: ファン、電源機構、および温度
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular</code></b>
_GETLOGS_ は、コントローラーの状況およびイベント・ログにアクセスできるようにします。_DEVICE xxx_ は、コントローラーで発生したデバイス・エラーのログを表示します。

_GETLOGS_ コマンドを使用した場合に表示される出力については、以下の例を参照してください。
```
driveErrorEntry
smartError.. ............................ false 
vendorID ................................ WDC
serialNumber ............................ WD-XXX
wwn ..................................... xxxxxxxxxxxxxxxx - CC_FILTER
deviceID ................................ 10
productID ............................... WD1003FB
numParityErrors ......................... 0
linkFailures ............................ 0
hwErrors ................................ 0
abortedCmds ............................. 7
mediumErrors ............................ 20
smartWarning ............................ 0
```

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show all | grep -iE "det|cou|tem|SN|S.M|fir” </code></b><br>
このコマンドを使用して、特定のドライブと、発生する可能性があるドライブ・エラーを示します。
次に、出力例を示します。
```
Drive /c0/e252/s0 - Detailed Information: 
Shield Counter = 0
 Media Error Count = 0
 Other Error Count = 0 
Drive Temperature = 24C (75.20 F) 
Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No 
SN = XXXX 
Firmware Revision = SN04

 Drive /c0/e252/s1 - Detailed Information: 
Shield Counter = 0 
Media Error Count = 0 
Other Error Count = 0 
Drive Temperature = 22C (71.60 F) 
Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No 
SN = xxxx 
Firmware Revision = SN03 

Drive /c0/e252/s2 - Detailed Information:
 Shield Counter = 0 
Media Error Count = 0 
Other Error Count = 0 
Drive Temperature = 21C (69.80 F)
 Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No
 SN = xxxx 
Firmware Revision = SN04

 Drive /c0/e252/s3 - Detailed Information:
 Shield Counter = 0 
Media Error Count = 0
 Other Error Count =
 Drive Temperature = 23C (73.40 F) 
Predictive Failure Count = 0
 S.M.A.R.T alert flagged by drive = No 
SN = xxxx
Firmware Revision = SN03  
```

<!--<code><b>/opt/MegaRAID/storcli/storcli64 /c0 show all | less </code></b>-->
<!--You use this command to view RAID health, size, name, and other important information.-->

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show rebuild</code></b>
このコマンドは、すべてのドライブの再ビルド状況と、再ビルドを完了するための見積もり時間を表示します。このコマンドを実行すると、次の出力が表示されます。
```
---------------------------------------------
Drive-ID Progress% Status Estimated Time Left 
---------------------------------------------
/c0/e252/s0 - Not in progress
 /c0/e252/s1 - Not in progress
 /c0/e252/s2 - Not in progress
 /c0/e252/s3 - Not in progress
--------------------------------------------- 
```

<b>RAID アラートの「スパム」</b>
デフォルト構成 (/opt/lsi/mrmonitor/MegaMonitor/config-current.xml) の「global」セクションを変更します。
```<global>
 <severity level="FATAL"> 
<do-systemlog/> 
<do-email/>
 </severity>
<severity level="CRITICAL"> 
<do-email/>
 <do-systemlog/> 
</severity>
 <severity level="WARNING">
 <do-email/> 
<do-systemlog/> 
</severity>
 <severity level="INFO"> <do-systemlog/>
</severity>
 </global> 
```
次のように変更します。
```
<global> 
<severity level="FATAL"> 
<do-systemlog/> 
<do-email/>
 </severity> 
<severity level="CRITICAL"> 
<do-email/> 
<do-systemlog/> 
</severity> 
<severity level="WARNING"> 
<do-systemlog/> 
</severity> 
<severity level="INFO">
<do-systemlog/>
 </severity> 
</global> 
```
**注:** レベル「WARNING」の「do-email」タグを削除します。または、セキュリティー・レベルを「INFO」に変更します。

## 一般的なドライブ・エラー

最も一般的なドライブ・エラーは、スマート・エラー、ハードウェア・エラー、およびメディア・エラーです。このようなエラーは、ドライブに障害がある場合に表示されます。そのため、できるだけ早くドライブを交換する必要があります。

異常ではありませんが、異常終了したコマンドも一般的な別のエラーです。ただし、異常終了したコマンドの数が増えた (100 など) 場合は、サポート・チケットをオープンしてください。  

リンク・エラーは、ケーブルの取り付け直しまたは交換が必要な可能性があることを示しています。

## サポート・チケット情報

<b>Adaptec RAID カード</b>
サポート・チケットの作成時には、`arcconf getconfig 1/arcconf getlogs 1 device tabular` の完全な出力を含めるようにしてください。この情報を提供すると、サポート・チームがドライブ順序、アレイのメンバーシップ、アレイの形状、およびケーブル接続の問題を特定する際に役立ちます。この情報は、失われた RAID 構成をリカバリーするためには不可欠です。初期の更新時に再始動/電源オフするための許可を付与するか、ホット・スワップするように依頼すると、サポート・チケット・プロセスが高速化されます。

<b>LSI RAID カード</b>
LSI RAID カードのログ・ファイルを取得するには、以下のコマンドを使用します。これらのログ・ファイルの完全な出力をサポート・チケットに含める必要があります。
```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```

**注**: トラブルシューティングを実行する前に、作業を必ずバックアップしてください。
