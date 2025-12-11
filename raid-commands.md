---

copyright:
  years: 1994, 2025
lastupdated: "2025-12-11"


keywords: raid controller commands, raid commands

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# RAID controller commands
{: #bm-raid-controller-commands}

You can use the Adapatec&reg; arcconf CLI or the Broadcom StorCLI to run RAID controller commands. The following commands are the most common RAID controller commands that you might use.
{: shortdesc}

To identify which type you have, [go to devices](/docs/bare-metal?topic=bare-metal-navigating-devices) in the console, and then click the name of the bare metal server to view its system details.
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
* Compaction or expansion

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

Use this command to view event logs. Because logs can exist for drives that were replaced, you need to match the serial number to identify the output for existing drives.

`/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular`

`_GETLOGS_` gives you access to the status and event logs of a controller. `_DEVICE xxx_` displays a log of any device errors.

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

The following example shows the expected output:

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

## Common drive errors
{: #bm-common-drive-errors}

The most common drive errors are SMART errors and hardware errors. These errors are commonly listed as media or medium errors. Any of these errors in the CLI output indicate a drive failure or that a failure is likely to occur. If you see an error, then you need to replace the drive as soon as possible. If you have drive errors, go to [RAID support case information](/docs/bare-metal?topic=bare-metal-bm-raid-support-case) for troubleshooting information and data to gather to open a support case.

Link errors indicate that a cable might need to be reseated or replaced. Although not unusual, aborted commands are another common error. But, if aborted commands increase in number (such as 100), open a [support case](/docs/bare-metal?topic=bare-metal-bm-raid-support-case).

After the drive is replaced, it rebuilds in place with no further action if the drive is part of a redundant RAID volume. If you are not using RAID and if the drive is part of a nonredundant RAID 0, or if it is a JBOD, you need to partition and format the drive before you use it.

Make sure that you back up any work before you troubleshoot. 
{: important}

## Installing StorCLI
{: #installing-storcli}

If your server does not include StorCLI by default, you can download and install it. {{site.data.keyword.cloud_notm}} provides a StorCLI version to download for some operating systems. You can go to the RAID card vendor website to download the most recent CLI version directly if StorCLI isn't available for your operating system.

To verify that the installation is successful, run the [show all](/docs/bare-metal?topic=bare-metal-bm-raid-controller-commands#check-raid-configuration) command that applicable to your operating system.

### Linux
{: #install-storcli-linux}

Use the following steps to install StorCLI for a Linux operating system:

1. Use SSH to connect to your server.

2. Go to your /tmp directory.

   `cd /tmp `

3. Download the StorCLI.

   `wget http://downloads.service.softlayer.com/lsitools/007.2106.0000.0000_Unified_StorCLI-PUL.zip`

4. Extract the files.

   `unzip 007.2106.0000.0000_Unified_StorCLI-PUL.zip`

5. Go to the StorCLI directory.

    `cd /tmp/Unified_storcli_all_os`

6. Find the directory for your operating system. For {{site.data.keyword.redhat_notm}} and related distributions, go to the Linux directory.

   `cd Linux`
 
7. Install the StorCLI package. For RPM-based systems, run the following command:
   
   `rpm -ivh storcli-007.2106.0000.0000-1.noarch.rpm` 
  
### Microsoft Windows
{: #install-storcli-windows}

Use the following steps to install StorCLI on a Windows system:

1. Use SSH to connect to your server.

2. Download the StorCLI package to the server from the following path:

   `http://downloads.service.softlayer.com/lsitools/007.2106.0000.0000_Unified_StorCLI-PUL.zip`

3. Create a folder that is named `storcli` in C:\ so that the path is `C:\storcli`.

4. Extract the files from the download.

   `unzip 007.2106.0000.0000_Unified_StorCLI-PUL.zip`

5. Copy the file that is named `storcli64` from the Windows folder into the `C:\storcli` directory that you created.

### VMware ESXi 7.0
{: #install-storcli-esxi7}

Use the following steps to install StorCLI on a VMware ESXi 7.0 system:

1. Use SSH to connect to your ESXi host.

2. Go to your /tmp directory.

   `cd /tmp `

3. Download the StorCLI.

   `wget http://downloads.service.softlayer.com/lsitools/007.2106.0000.0000_Unified_StorCLI-PUL.zip`

4. Extract the file.

   `unzip 007.2106.0000.0000_Unified_StorCLI-PUL.zip`

5. Go to the VMware directory.

   `cd /tmp/Unified_storcli_all_os/Vmware/VMwareOP64/`

6. Extract the ESXi7 file.

   `unzip VMWare-ESXi7.0-StorCLI.zip`

7. Install the StorCLI.

   `esxcli software vib install -v=/tmp/Unified_storcli_all_os/VMware/VMwareOP64/vib20/vmware-storcli64/BCM_bootbank_vmware-storcli64_007.2106.0000.0000-01.vib --no-sig-check`

### VMWare ESXi 8.0
{: #install-storcli-esxi8}

Use the following steps to install StorCLI on a VMware ESXi 8.0 system:

1. Go to [Broadcom - Support Documents and Downloads](https://www.broadcom.com/support/download-search){: external} to download the file that is named "Latest Storcli for all OS." Search for `Storcli` with the search filter set to "Storage Adapters, Controllers, and ICs" to find this file in the Management Software and Tools section.

2. Using an application such as WinSCP, upload the .zip file to the `/tmp` directory of your ESXi host through SFTP.
   - Make sure that SSH is enabled and that any firewalls allow traffic on port 22.

3. Use SSH to connect to your ESXi host.

4. Go to your /tmp directory.

   `cd /tmp `

5. Extract the `<VERSION>_storcli.zip` file that you downloaded, where 'VERSION' represents the version that you downloaded, to get to the `VMware/ESXi8/`directory.

6. Extract the `BCM-storcli_<VERSION>-package.zip` and the `BCM-storcli_<VERSION>.zip` to get to the directory that contains the "vib20" folder.

   Example commands:

   `unzip BCM-storcli_007.3306.0000.0000-01_24660126-package.zip`

   `unzip BCM-storcli_007.3306.0000.0000-01_24660126.zip`

7. Install the StorCLI by using the following syntax: `esxcli software vib install -v=<Filepath of the StorCLI VIB>`.

    Example command:
   
    `esxcli software vib install -v=/tmp/storcli_rel/Unified_storcli_all_os/VMware/ESXi8/vib20/storcli/BCM_bootbank_storcli_007.3306.0000.0000-01.vib`

8. Restart the system for the change to take effect.
   - Put the host in maintenance mode.
   - Restart the host.
   - Take the host out of maintenance mode.
