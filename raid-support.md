---

copyright:
  years: 1994, 2019
lastupdated: "2018-5-31"

keywords: raid support, raid help

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# RAID support ticket information
{:# bm-raid-support-ticket}

If you have a problem or question about using RAID on your bare metal server, you might find an answer in the [IBM developerWorks dW Answers](https://developer.ibm.com/answers/topics/ibm-cloud/){:new_window} forum.
You can also open a support ticket. For information about support tickets, see [Opening a support ticket.](https://test.cloud.ibm.com/docs/get-support?topic=get-support-getting-customer-support#open-ticket){:new_window}
{:shortdesc}

<!--During a drive or RAID failure, support tickets are automatically created. You can create a support ticket for other problems.--> When a support ticket is created, you need to provide RAID log files. The information in RAID log files is critical to the recovery of a lost RAID configuration. Providing your log files helps the support team identify drive order, array membership, array geometry, and cabling issues. Depending on the type of RAID controller that you are using, Adaptec or LSI, use the following commands to obtain RAID log files.

**Note:** Granting permission to restart/power down in the initial update or by asking for the drive to be hot swapped, speeds up the support ticket process.

<b>Adaptec RAID cards</b><br>
Use the following command to obtain the log files for Adaptec RAID cards. Make sure that you include the full output of this log file in your support ticket.

`arcconf getconfig 1/arcconf getlogs 1 device tabular`.

<b>LSI RAID cards</b><br>
Use the following commands to obtain the log files for LSI RAID cards. You need to include the full output of these log files in your support ticket.
```/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
**Important:** Make sure that you back up any work before troubleshooting begins.
