---

copyright:
  years: 1994, 2019
lastupdated: "2019-11-05"

keywords: raid support, raid help

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:note: .note}

# RAID support ticket information
{:# bm-raid-support-ticket}

If you have a question about using RAID on your bare metal server, you might find an answer in the [IBM Developer Answers](https://developer.ibm.com/answers/topics/ibm-cloud/){:new_window} forum.
You can also open a support ticket. For more information about support tickets, see [Opening a support ticket.](/docs/get-support?topic=get-support-using-avatar#open-ticket)
{:shortdesc}

When a support ticket is created, you need to provide RAID log files. The information in RAID log files is critical to the recovery of a lost RAID configuration. Providing your log files helps the support team identify drive order, array membership, array geometry, and cabling issues. Depending on the type of RAID controller that you are using, Adaptec or LSI, use the following commands to retrieve RAID log files.

Granting permission to restart or power down in the initial update or by asking for the drive to be hot-swapped, speeds up the support ticket process.
{:note}
 
 
### Adaptec RAID cards
 
Use the following command to obtain the log files for Adaptec RAID cards. Remember to include the full output of this log file in your support ticket.

```
arcconf getconfig 1/arcconf getlogs 1 device tabular
```
  
  
### LSI RAID cards

Use the following commands to obtain the log files for LSI RAID cards. Remember to include full output of these log files in your support ticket.

```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
 
Make sure that you back up any work before troubleshooting begins.
{:important}
