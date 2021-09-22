---

copyright:
  years: 1994, 2021
lastupdated: "2020-11-11"

keywords: raid support, raid help

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:note: .note}

# RAID support case information
{:# bm-raid-support-case}

If you have a question about using RAID on your bare metal server, you might find an answer in the [IBM Developer Answers](https://developer.ibm.com/answers/topics/ibm-cloud/){: external} forum.
You can also open a support case. For more information about support cases, see [Getting support](/docs/get-support?topic=get-support-using-avatar#getting-support).
{: shortdesc}

When a support case is created, you need to provide RAID log files. The information in RAID log files is critical to the recovery of a lost RAID configuration. Providing your log files helps the support team identify drive order, array membership, array geometry, and cabling issues. Depending on the type of RAID controller that you are using, Adaptec or Broadcom, use the following commands to retrieve RAID log files.

Granting permission to restart or power down in the initial update or by asking for the drive to be hot-swapped, speeds up the support case process.
{: note}


## Adaptec RAID cards
{: #adaptec-raid-support-case}

Use the following command to obtain the log files for Adaptec RAID cards. Remember to include the full output of this log file in your support case.

```
arcconf getconfig 1/arcconf getlogs 1 device tabular
```
{: codeblock}


## Broadcom RAID cards
{: #broadcom-raid-support-case}

Use the following commands to obtain the log files for Broadcom RAID cards. Remember to include full output of these log files in your support case.

```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
{: codeblock}

Make sure that you back up any work before troubleshooting begins.
{: important}
