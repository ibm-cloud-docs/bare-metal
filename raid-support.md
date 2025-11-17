---

copyright:
  years: 1994, 2025
lastupdated: "2025-11-17"

keywords: raid support, raid help

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# RAID support case information
{: #bm-raid-support-case}

When a support case is created to resolve a drive error, you need to provide RAID log files. The information in RAID log files is critical to the recovery of a lost RAID configuration. Providing your log files helps the {{site.data.keyword.cloud}} team identify drive order, array membership, array geometry, and cabling issues. Depending on the type of RAID controller that you are using, Adaptec or Broadcom, use the following commands to retrieve RAID log files.
{: shortdesc}

To identify which type you have, [navigate to devices](/docs/bare-metal?topic=bare-metal-navigating-devices) in the console, and then click the name of the server to view its system details.
- If the Drive Controller entry begins with "Lenovo Raid", you have an Adaptec controller.
- If the Drive Controller entry begins with "LSI", you have a Broadcom controller.
- If you do not see one of these types, then your server is not using a RAID controller.

Granting permission to restart or power down in the initial update or asking for the drive to be hot-swapped speeds up the support case process.
{: note}

## Adaptec RAID cards
{: #adaptec-raid-support-case}

Use the following command to obtain the log files for Adaptec RAID cards. Remember to include the full output of this log file in your support case.

```text
arcconf getconfig 1
arcconf getlogs 1 device tabular
```
{: codeblock}

## Broadcom RAID cards
{: #broadcom-raid-support-case}

Use the following commands to obtain the log files for Broadcom RAID cards.  If the server does not have StorCLI installed, refer to [Installing StorCLI](/docs/bare-metal?topic=bare-metal-bm-raid-controller-commands#installing-storcli). Remember to include the full output of these log files in your support case.

```text
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show eventloginfo  
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
{: codeblock}

For ESXi servers, use the following commands.

   ```text
   /opt/lsi/storcli64/storcli64 /c0 show all
   /opt/lsi/storcli64/storcli64 /c0 show eventloginfo
   /opt/lsi/storcli64/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
   /opt/lsi/storcli64/storcli64 /c0 show TermLog
   ```
   {: codeblock}

Make sure that you back up any work before troubleshooting begins.
{: important}
