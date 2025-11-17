---

copyright:
  years: 1994, 2025
lastupdated: "2025-11-17"


keywords: raid controller commands, raid commands

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# RAID controller commands
{: #bm-raid-controller-commands}

You can use the Adapatec&reg; arcconf CLI or the Broadcom StorCLI to run RAID controller commands. The following commands are the most common RAID controller commands that you might use.
{: shortdesc}

To identify which type you have, [navigate to devices](/docs/bare-metal?topic=bare-metal-navigating-devices) in the console, and then click the name of the bare metal server to view its system details.
- If the Drive Controller entry begins with "Lenovo Raid", you have an Adaptec controller and use arcconf commands.
- If the Drive Controller entry begins with "LSI", you have a Broadcom controller and use StorCLI commands.
- If you do not see one of these types, then your server is not using a RAID controller.

## arcconf getstatus
{: #arcconf_getstatus}

Use this command to list the status of an operation and any active background commands.

`/usr/Adaptec_Event_Monitor/arcconf getstatus 1`

`_GETSTATUS_` lists the type of operation, logical drive number, logical drive size, and progress of the operation. You can also see the status of any background commands that are running, such as the following items:

* Most recent rebuild
* Synchronization
* Logical-drive migration
* Compaction/expansion

## arcconf getconfig
{: #arcconf_getconfig}

Use this command to list configuration information.

`/usr/Adaptec_Event_Monitor/arcconf getconfig 1`

`_GETCONFIG_` lists information about controllers, logical drives, and physical drives. You can see information such as the following items:

* Controller type
* BIOS, boot block, device driver, and firmware versions
* Physical device type, device ID, presence of PFA
* Physical device state
* Enclosure information: fan, power supply, and temperature

## arcconf getlogs
{: #arcconf_getlogs}

Use this command to view the event logs.

`/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular`

`_GETLOGS_` gives you access to the status and event logs of a controller. `_DEVICE xxx_` displays a log of any device errors that the controller encounters.

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
{: codeblock}

## StorCLI show all
{: #check-raid-configuration}

Use this command to check the disk health of the server and to check for drives that need attention. This command shows information on specific drives and any potential drive errors that it might have.

   ```text
   /opt/MegaRAID/storcli/storcli64 /c0/eall/sall show all | grep -iE "det|cou|tem|SN|S.M|fir”
   ```
   {: codeblock}
   
For ESXi servers, use the following command:

   ```text
   /opt/lsi/storcli64/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
   ```
   {: codeblock}

From the output, look for the topology section where the RAID type is listed as a column. If the output shows an error, see [Common drive errors](/docs/bare-metal?topic=bare-metal-bm-raid-controller-commands#bm-common-drive-errors).

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
{: codeblock}

## StorCLI show rebuild
{: #storcli_rebuild}

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
{: codeblock}

## Change email option for RAID alerts
{: #change-raid-email}

If the volume of email that you receive for RAID alerts is more than expected, you can update the configuration file to prevent an email alert being sent for a severity level of "WARNING". Do not alter the provided configuration unless you are aware of the risks. You make changes to the "global" section of the default config (`/opt/Broadcom/mrmonitor/MegaMonitor/config-current.xml`):

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
{: codeblock}

Remove the `do-email` tag for the the "WARNING" level, to read like the following:

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
{: codeblock}

## Common drive errors
{: #bm-common-drive-errors}

The most common drive errors are SMART errors and hardware errors, which are commonly listed as media or medium errors. Any of these errors in the CLI output indicate that a drive failure has occurred or is likely to occur. If you see an error, you need the drive replaced as soon as possible. If you have drive errors, go to [RAID support case information](/docs/bare-metal?topic=bare-metal-bm-raid-support-case) for troubleshooting information and data to gather for a support case.

Link errors can indicate that a cable might need reseated or replaced. Although not unusual, aborted commands are another common error. But, if aborted commands increase in number (such as 100), open a support case.

After the drive is replaced, it should rebuild in place with no further action when the drive is part of a redundant RAID volume. If you are not using RAID, if the drive is part of a non-redundant RAID 0, or if it is a JBOD, you need to partition and format the drive before putting it to use after its replacement.

Make sure that you back up any work before you troubleshoot. 
{: important}

## Installing StorCLI
{: #installing-storcli}

If your server instance does not include StorCLI by default, you can download and install it. IBM Cloud provides a version of the StorCLI that you can download. If you need to ensure that you have the latest CLI version, for example, to troubleshoot or resolve compatibility issues, go to the website for the vendor of your RAID card to download the latest CLI version directly.

Use the following steps to install StorCLI for a Linux operating system:

1. Use SSH to connect to your server.

2. Go to your /tmp directory.

   `cd /tmp `

3. Download the StorCLI.

   `wget http://downloads.service.softlayer.com/lsitools/1.14.12_StorCLI.zip`

4. Extract 1.14.12_StorCLI.zip.

   `unzip 1.14.12_StorCLI.zip`

5.  Go to the StorCLI directory.

    `cd /tmp/storcli_all_os`

6. Find the directory for your operating system type. For {{site.data.keyword.redhat_notm}} and related distributions, go to the Linux directory.

   `cd Linux`
 
7. Install the StorCLI package.  For RPM based systems run:
   
   `rpm -ivh storcli-1.14.12-1.noarch.rpm`
  
Use the following steps to install StorCLI for a VMware ESXi system:

1. Go to your /tmp directory.

   `cd /tmp `

2. Download the StorCLI.

   `wget http://downloads.service.softlayer.com/lsitools/1.14.12_StorCLI.zip`

3. Uncompress the file.

   `unzip 1.14.12_StorCLI.zip`

4. Go to the Vmware-NDS directory.

   `cd /tmp/storcli_all_os/Vmware-NDS/`

5. Install the StorCLI.

   `esxcli software vib install -v=/tmp/storcli_all_os/Vmware-NDS/vmware-esx-storcli-1.14.12.vib --no-sig-check`
