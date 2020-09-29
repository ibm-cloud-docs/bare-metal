---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-08"

keywords: R1Soft, restoring OS, restoring bare metal

subcollection: software

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Restoring your server from an R1Soft image
{: #restoring-your-server-from-an-r1soft-image}

Use this procedure to complete a restore to public or private {{site.data.keyword.BluVirtServers_full}} or {{site.data.keyword.BluBareMetServers_full}}. Use this process if a server failure causes data or OS loss. This process restores all file system blocks that are backed up (including the OS and any files that were not excluded from backups).
{:shortdesc}

Do not use this process if the restoration of a subset of files is the objective. To restore only the files, see [R1Soft Wiki](http://wiki.r1soft.com/display/CDP/Restoring+Files){:new_window}.

## Before you begin
* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## Restoring your virtual device
{: #restoring-your-virtual-device}

1. From the **Device List**, click into the device you want you restore.
2. Click the **Actions** menu and choose **Boot from image** you get a list of private images.
3. Choose **Public Images** from the menu.
4. Choose the appropriate R1Soft agent boot image for your version of R1Soft server (serverbackup-centos-bootcd-agent.iso) and click **Boot From This Image** link on the right.
5. From the **Device Details** page for the server that you are restoring, click **Actions** > **KVM Console**.
6. After the console is up and the image boots, you will see a Debian bootloader screen with some options. Press the Enter key to boot from the default option.
7. After the OS is booted, type `netconfig` and press **Enter**.
8. Choose **Yes** to configure the networking.
9. Enter networking configuration details from device details in the Control portal.
10. Choose **Yes** when prompted to restart networking.
11. Optionally, type `passed root` to set a root password for SSH logins and type service ssh start to allow SSH login. This step might be useful if your KVM console is slow.
12. Type `service cdp-agent restart` (This command starts the Continuous Data Protection for Files agent if it isn't already running).

## Restoring your bare metal device
{: #restoring-your-bare-metal-device}

1. Open a ticket in the [{{site.data.keyword.cloud_notm}} Console](https://cloud.ibm.com/){:new_window} and request that we boot your bare metal server in **R1Soft Bare Metal Restore mode**.
2. Using the **Device Details** page for the server that you are restoring, log in to the **IPMI KVM console**.
3. After the console is up and the image boots, you will see a Debian bootloader screen with some options. Press the Enter key to boot from the default option.
4. _R1Soft Bare Metal Restore_ boots into CentOS with the network IP preconfigured. Start the agent by using this command: `/etc/init.d/cdp-agent start` (or `/etc/init.d/cdp-agent restart`)
5. Choose **Yes** to configure the networking.
6. Enter networking configuration details from device details in the Control portal.
7. Choose **Yes** when prompted to restart networking.
8. Optionally, type `passed root` to set a root password for SSH logins and type service ssh start to allow SSH login. This step might be useful if your KVM console is slow.
9. Type `service cdp-agent restart` (This command starts the Tivoli Continuous Data Protection for Files agent if it isn't already running).

## Selecting the R1Soft server and other restore parameters and options
{: #selecting-the-r1soft-server-and-other-restore-parameters-and-options}

Refer to the R1Soft documentation for [Performing a Bare Metal Restore](http://wiki.r1soft.com/display/ServerBackup/Perform+a+bare-metal+restore)
You need to select the server to restore and select the file system, portion tables, and other restore options.
