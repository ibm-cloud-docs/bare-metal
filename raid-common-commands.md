---

copyright:
  years: 1994, 2023
lastupdated: "2018-5-30"

keywords: common raid commands

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}


# Common RAID commands
{: #bm-common-raid-commands}

You use the CLI to run RAID controller commands. The following are the most common RAID controller CLI commands that you might use.
{: shortdesc}

Windows and VMware have different paths to run storcli commands.
{: important}

**Windows** (use CMD)

`C:\Program Files (x86)\MegaRAID Storage Manager>`
or
`C:\Program Files\LSIStorCli>`

**VMware** (You need to install storcli before you run storcli commands)

`/opt/lsi/storcli/`

## Adaptec commands
{: #bm-adaptec-commands}

`/usr/Adaptec_Event_Monitor/arcconf getstatus 1`

`GETSTATUS`lists the type of operation, logical drive number, logical drive size, and progress of the operation. You can also see the status of any background commands that are running, such as the following items:

* Most recent rebuild
* Synchronization
* Logical-drive migration
* Compaction/expansion

`/usr/Adaptec_Event_Monitor/arcconf getconfig 1`
`GETCONFIG` lists information about controllers, logical drives, and physical drives. You can see information such as the following items:

* Controller type
* BIOS, boot block, device driver, and firmware versions
* Physical device type, device ID, presence of PFA
* Physical device state
* Enclosure information: fan, power supply, and temperature

`/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular`
`GETLOGS` gives you access to the status and event logs of a controller. `DEVICE xxx` lists a log of any device errors that the controller encounters.

See the following example for output that is made by using the _GETLOGS_ command:

```text
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
{: screen}

## LSI commands
{: #lsi-commands}

You use this command to show the specific drives and any possible drive errors that it might have.
`/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show all | grep -iE "det|cou|tem|SN|S.M|fir”`

 The following example shows the output:

```text
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
{: screen}

This command displays the rebuild status of all drives and the estimated time to complete the rebuild.

`/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show rebuild`

You see this output when you run the command:

```text
---------------------------------------------
Drive-ID Progress% Status Estimated Time Left
---------------------------------------------
/c0/e252/s0 - Not in progress
/c0/e252/s1 - Not in progress
/c0/e252/s2 - Not in progress
/c0/e252/s3 - Not in progress
---------------------------------------------
```
{: screen}

RAID alert "Spam"

Change the "global" section of the default config (/opt/lsi/mrmonitor/MegaMonitor/config-current.xml):

```text
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
<do-email/>
<do-systemlog/>
</severity>
<severity level="INFO"><do-systemlog/>
</severity>
</global>
```
{: screen}

to this:

```text
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
{: screen}

Remove the "do-email" tag for level "WARNING". Alternatively, change the security level to "INFO".
{: note}
