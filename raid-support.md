---

copyright:
  years: 1994, 2024
lastupdated: "2024-07-22"

keywords: raid support, raid help

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# RAID support case information
{: #bm-raid-support-case}

When a support case is created, you need to provide RAID log files. The information in RAID log files is critical to the recovery of a lost RAID configuration. Providing your log files helps the support team identify drive order, array membership, array geometry, and cabling issues. Depending on the type of RAID controller that you are using, Adaptec or Broadcom, use the following commands to retrieve RAID log files.
{: shortdesc}

Granting permission to restart or power down in the initial update or by asking for the drive to be hot-swapped, speeds up the support case process.
{: note}

You can open a [support case](/docs/get-support?topic=get-support-using-avatar#getting-support) if you need help with RAID.

## Adaptec RAID cards
{: #adaptec-raid-support-case}

Use the following command to obtain the log files for Adaptec RAID cards. Remember to include the full output of this log file in your support case.

```text
arcconf getconfig 1/arcconf getlogs 1 device tabular
```
{: codeblock}

## Broadcom RAID cards
{: #broadcom-raid-support-case}

Use the following commands to obtain the log files for Broadcom RAID cards. Remember to include the full output of these log files in your support case.

```text
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
{: codeblock}

Make sure that you back up any work before troubleshooting begins.
{: important}
