---

copyright:
  years: 2016, 2021
lastupdated: "2019-06-17"

keywords: manage bare metal servers, power off, replicate, reload os, delete server, manage server

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{: note .note}

# Managing bare metal servers
{: #bm-manage-servers}

You can cancel, stop, and restart servers.
{: shortdesc}

## Before you begin
{: #bm-managing-before-you-begin}

* Go to your console's device menu. For more information, see [Navigating to devices](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## Deleting the server instance
{: #bm-delete-server-instance}

At any time, you can delete the bare metal server instance if you no longer need the instance and do not want to be charged.

1. Go to the **Devices** menu and highlight the device to be deleted.
2. Click **Actions** and select **Cancel Server**.

## Powering off a server
{: #bm-power-off}

You can create a server in advance to prepare for usage. After you create the server, power it off to make sure that nothing gets changed and that no one can access it. When you're ready, you can power on the server and have it ready in minutes.

1. Go to the **Devices** menu and highlight the device to be powered off or on.
2. Click **Actions** and select **Power On/Off**.

You are billed for the server while it is powered off. If the server is powered off, it stays powered off and you need to be manually power it on.
{: note}
