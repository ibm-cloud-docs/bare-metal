---
copyright:
  years: 1994, 2018
lastupdated: "2018-5-10"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID 控制器指令

請使用 Adaptec 指令行公用程式來執行 RAID 控制器指令。以下是您可能使用的最常見 RAID 控制器指令。
{:shortdesc}

**附註：**Windows 和 VMware 執行 storcli 指令的路徑不同。請參閱下列範例，以取得適當的指令路徑。

Windows（使用 CMD）
`C:\Program Files (x86)\MegaRAID Storage Manager>`      
或
`C:\Program Files\LSIStorCli>`

VMware（您需要先安裝 storcli，才能執行 storcli 指令）
`/opt/lsi/storcli/`

## 常見 RAID 控制器指令

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_ 會列出作業類型、邏輯磁碟機號碼、邏輯磁碟機大小，及作業的進度。您也可以看到執行中之任何背景指令的狀態，例如下列項目：
<ul>
  <li> 最近的重建
  <li> 同步化
  <li> 邏輯磁碟機移轉
  <li> 壓縮/展開
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1</b></code> <br>
_GETCONFIG_ 會列出控制器、邏輯磁碟機和實體磁碟機的相關資訊。您可以看到例如下列項目的資訊：
<ul>
  <li> 控制器類型
  <li> BIOS、開機區塊、裝置驅動程式及韌體版本 
  <li> 實體裝置類型、裝置 ID、PFA 是否存在 
  <li> 實體裝置狀態 
  <li> 機箱資訊：風扇、電源供應器和溫度
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular</code></b>
_GETLOGS_ 可讓您存取控制器的狀態及事件日誌。_DEVICE xxx_ 會顯示控制器遇到之任何裝置錯誤的日誌。

請參閱下列範例，以取得使用 _GETLOGS_ 指令產生的輸出：
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

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show all | grep -iE "det|cou|tem|SN|S.M|fir" </code></b><br>
您可以使用這個指令來顯示特定的磁碟機以及它可能有的任何可能磁碟機錯誤。下列範例顯示輸出：
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
這個指令會顯示所有磁碟機的重建狀態，以及完成重建的預估時間。當您執行指令時，會看到此輸出：
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

<b>RAID 警示「垃圾郵件」</b>
請將預設配置 (/opt/lsi/mrmonitor/MegaMonitor/config-current.xml) 的 "global" 區段：
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
變更為：
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
**附註：**請移除 "WARNING" 層次的 "do-email" 標籤。或者，將安全層次變更為 "INFO"。

## 常見磁碟機錯誤

最常見的驅動程式錯誤是智慧型錯誤、硬體錯誤及媒體錯誤。如果磁碟機故障，您會看到這些錯誤。因此，您需要儘快更換磁碟機。

雖然不尋常，但中斷的指令仍是另一個常見的錯誤。但是，如果中斷的指令數目增加（例如 100），請開立支援問題單。  

鏈結錯誤可以表示纜線可能需要重新安置或更換。

## 支援問題單資訊

<b>Adaptec RAID 卡</b>
請確定您在建立支援問題單時，包含 `arcconf getconfig 1/arcconf getlogs 1 device tabular` 的完整輸出。提供此資訊可協助支援團隊識別磁碟機順序、陣列成員資格、陣列幾何佈置及纜線安裝問題。此資訊對於遺失 RAID 配置的回復至關重要。在起始更新授與重新啟動/關閉電源的許可權，或要求將它熱交換，可加速支援問題單程序。

<b>LSI RAID 卡</b>
請使用下列指令來取得 LSI RAID 卡的日誌檔。您需要在支援問題單包含這些日誌檔的完整輸出。
```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```

**附註**：請確定在進行疑難排解之前，先備份任何工作。
