---

copyright:
  years: 1994, 2019
lastupdated: "2018-07-10"

keywords: raid controller commands, raid commands

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# RAID 控制器命令
{: #bm-raid-controller-commands}

可以使用 Adapecec 命令行实用程序来运行 RAID 控制器命令。下面是可能会使用的最常用 RAID 控制器命令。
{:shortdesc}

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_ 用于列出操作类型、逻辑驱动器编号、逻辑驱动器大小和操作进度。您还可以查看正在运行的任何后台命令的状态，例如以下各项：
<ul>
  <li> 最近的重建
  <li> 同步
  <li> 逻辑驱动器迁移
  <li> 压缩/扩展
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1</b></code><br>
_GETCONFIG_ 用于列出有关控制器、逻辑驱动器和物理驱动器的信息。您可以查看多种信息，例如以下各项：
<ul>
  <li> 控制器类型
  <li> BIOS、引导块、设备驱动程序和固件版本 
  <li> 物理设备类型、设备标识、存在 PFA 
  <li> 物理设备状态 
  <li> 机箱信息：风扇、电源和温度
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular</code></b>
_GETLOGS_ 使您能够访问控制器状态和事件日志。_DEVICE xxx_ 显示控制器遇到的任何设备错误的日志。

请参阅以下示例，以获取使用 _GETLOGS_ 命令生成的输出：
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
使用此命令可显示特定驱动器及其可能发生的任何可能的驱动器错误。 
以下示例显示了输出：
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
此命令用于显示所有驱动器的重建状态以及完成重建的估计时间。在运行此命令时，您将看到以下输出：
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

<b>RAID alert "Spam"</b>
将缺省配置 (/opt/lsi/mrmonitor/MegaMonitor/config-current.xml) 的“global”部分： 
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
更改为： 
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
**注：**除去级别“WARNING”的“do-email”标记。或者，将安全级别更改为“INFO”。

## 常见驱动器错误
{: #bm-common-drive-errors}

最常见的驱动器错误是智能错误、硬件错误和介质错误。如果驱动器发生故障，您会看到这些错误。为此，您需要尽快更换该驱动器。

异常中止的命令是另一个常见错误。但是，如果异常中止的命令的数量增加（如 100），请开具支持凭单。  

链接错误可能指示可能需要重新安装或更换电缆。

### 支持凭单信息
{: #bm-raid-support}

**Adaptec RAID 卡** <br>
创建支持凭单时，请确保包含 `arcconf getconfig 1/arcconf getlogs 1 device tabular` 的完整输出。提供这些信息可帮助支持团队识别驱动器订单、阵列成员资格、阵列几何以及连线问题。这些信息对于恢复丢失的 RAID 配置至关重要。在初始更新中授予重新启动/关闭电源的许可权或者要求进行热交换，可以加快支持凭单过程的处理速度。 

**LSI RAID 卡** <br>
使用以下命令获取 LSI RAID 卡的日志文件。您需要将这些日志文件的完整输出包含在支持凭单中。
```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```

**注**：确保在执行故障诊断之前备份所有工作。
