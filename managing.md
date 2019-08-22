---

copyright:
  years: 2016, 2019
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
{:note .note}

# Managing bare metal servers
{: #bm-manage-servers}

You can cancel, stop, and restart servers.
{:shortdesc}

## Before you begin
{: #bm-managing-before-you-begin}

* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).


<!-- ## Replicating a server instance
{: #bm-replicate-server-instance}

You can copy or clone a bare metal server instance to replicate the server configuration and quickly get a new server up and running.
{:shortdesc}

To clone the instance:
 1. Go to the **Device** menu and highlight the device to be copied.
 2. Click **Actions** and select **Configure Replica**. All configurations are copied. No data or content is not copied.
 3. Enter a unique server name.
 4. Specify the domain name. -->

<!-- ## Reloading the operating system
{: #bm-reload-os}

Occasionally, you might want to reload the operating system on your server.
{:shortdesc}

To reload the operating system, follow these steps.
 1. Back up all data before you start. If you don't back up your data, all data that is on the primary disk is lost. But, secondary disk data stays intact.
 2. Go to the **Devices** menu and highlight the device to be reloaded.
 3. Click **Actions** and select **OS Reload**. You can select one of these options:
  * Change the operating system to a different one and start over with new configurations.
  * Keep the existing operating system with the current configurations, but wipe out the server to start over.

During the OS reload, the server is offline and unavailable for use. Reload time varies based on server capacity and operating system. If you defined a provision script, all configurations are restored after the reload completes. Data was backed up before the OS reload can be uploaded the server when the server is available. -->

## Deleting the server instance
{: #bm-delete-server-instance}

At any time, you can delete the bare metal server instance if you no longer need the instance and do not want to be charged.
{:shortdesc}

1. Go to the **Devices** menu and highlight the device to be deleted.
2. Click **Actions** and select **Cancel Server**.

## Powering off a server
{: #bm-power-off}

You can create a server in advance to prepare for usage. After you create the server, power it off to make sure that nothing gets changed and that no one can access it. When you're ready, you can power on the server and have it ready in minutes.
{:shortdesc}

1. Go to the **Devices** menu and highlight the device to be powered off or on.
2. Click **Actions** and select **Power On/Off**.

You are billed for the server while it is powered off. If the server is powered off, it stays powered off and you need to be manually power it on.
{: note}
