---
copyright:
  years: 1994, 2018
lastupdated: "2018-5-10"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID controller commands

You use the Adapatec Command Line Utility to run RAID controller commands.
The following are the most common RAID controller commands that you might use.
{:shortdesc}

**Note:** Windows and VMware have different paths to run storcli commands:

Windows (use CMD)

`C:\Program Files (x86)\MegaRAID Storage Manager>'      
or
`C:\Program Files\LSIStorCli>`

VMware (You need to install storcli before you run storcli commands)

`/opt/lsi/storcli/`

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_ lists the type of operation, logical drive number, logical
drive size, and progress of the operation. You can also see the status of any background commands that are running, such as the following items:
<ul>
  <li> Most recent rebuild
  <li> Synchronization
  <li> Logical-drive migration
  <li> Compaction/expansion
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1</b></code> <br>
_GETCONFIG_ lists information about controllers, logical drives, and physical drives. You can see information such as the following items:
<ul>
  <li> Controller type
  <li> BIOS, boot block, device driver, and firmware versions 
  <li> Physical device type, device ID, presence of PFA 
  <li> Physical device state 
  <li> Enclosure information: fan, power supply, and temperature
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular</code></b>
_GETLOGS_ gives you access to the status and event logs of a controller. _DEVICE xxx_ displays a log of any device errors that the controller encounters.

See the following example for output that is made by using the _GETLOGS_ command:
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
You use this command to show the specific drives and any possible drive errors that it might have. 
The following example shows the output:
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
This command displays the rebuild status of all drives and the estimated time to complete the rebuild. You see this output when you run the command:
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
Change the "global" section of the default config (/opt/lsi/mrmonitor/MegaMonitor/config-current.xml): 
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
to this: 
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
**Note:** Remove the "do-email" tag for level "WARNING". Alternatively, change the security level to "INFO".

## Common drive errors

The most common driver errors are smart errors, hardware errors, and medium errors. You see these errors if a drive is failing. So, you need to replace the drive as soon as possible.

Although not unusual, aborted commands are another common error. But, if aborted commands increase in number (such as 100), open a support ticket.  

Link errors can indicate that a cable might need reseated or replaced.

### Support ticket information

<b>Adaptec RAID cards</b>
Make sure that you include the full output of `arcconf getconfig 1/arcconf getlogs 1 device tabular` when you create a support ticket. Providing this information helps the support team identify drive order, array membership, array geometry, and cabling issues. This information is critical to the recovery of a lost RAID configuration. Granting permission to restart/power down in the initial update or asking it to be hot swapped speeds up the support ticket process. 

<b>LSI RAID cards</b>
Use the following commands to obtain the log files for LSI RAID cards. You need to include the full output of these log files with your support ticket.
```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```

**Note**: Make sure that you back up any work before troubleshooting is done.
