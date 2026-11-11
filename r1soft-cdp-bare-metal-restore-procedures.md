---

copyright:
  years: 2017, 2026
lastupdated: "2026-11-11"

keywords:

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Restoring your server from an R1Soft&reg; image
{: #restoring-your-server-from-an-r1soft-image}

Use this procedure to complete a restore to public or private {{site.data.keyword.BluVirtServers_full}} or {{site.data.keyword.BluBareMetServers_full}}. Use this process if a server failure causes data or OS loss. This process restores all file system blocks that are backed up (including the OS and any files that were not excluded from backups).
{: shortdesc}

Do not use this process if you need to restore a subset of files. To restore only the files, see [R1Soft&reg; Wiki](http://wiki.r1soft.com/display/CDP/Restoring+Files){: external}.
{: important}

## Before you begin
{: #byb-restore-r1soft}

* Go to your console device menu.
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage users** Classic infrastructure permission, can adjust the permissions.

## Restoring your virtual server
{: #restoring-your-virtual-device}

1. From the **Device list**, click the device that you want you restore.
1. Click **Actions** menu and choose **Boot from image** > **Public images**.
1. Select the appropriate R1Soft agent boot image that matches your version of R1Soft server (example: serverbackup-bootcd-agent-6.18.5.iso) and click **Boot from this image**.
1. From the **Device details** page for the server that you are restoring, click **Actions** > **KVM Console**.
1. After the console is up and the image boots, the Debian bootloader options screen appears. Press Enter to boot from the default option.
1. After the operating system starts, type `sudo Ceni` and press Enter to set up networking for the ISO.
1. Choose **Yes** to configure the networking and enter the network configuration information (use your virtual server networking information).
1. Choose **Yes** to restart networking.
1. Optionally, enter `passed root` to set a root password for SSH logins and enter `service ssh start` to allow SSH login. This step might be useful if your KVM console is slow.
1. Enter `service cdp-agent restart`. This command starts the Continuous Data Protection for the files agent if it isn't running.

## Restoring your bare metal server
{: #restoring-your-bare-metal-device}

Use the following steps to restore your bare metal server.

1. From the Device list, click the bare metal server that you want you restore.
2. Click the Actions menu and select **Bare metal restore**.

   Configuring the Tivoli Continuous Data Protection for Files agent and networking takes about 10 minutes after the ISO boots. You don't need to log in to or adjust the ISO after it boots.
   {: note}

3. After 10 minutes, confirm that the Tivoli Continuous Data Protection for Files and networking started successfully by testing the agent with the [R1soft&reg; SBM](http://wiki.r1soft.com/display/ServerBackupManager/Test+Agent+Connection){: external}.

## Using Bare Metal Restore for Windows-based servers
{: #using-bare-metal-restore-for-windows-based-devices}

When you use Bare Metal Restore for a Windows server, the restore process generally takes longer when compared to Linux-based devices. So, keep the following information in mind.

* The estimated time to mount a Windows ISO can take 4 or more hours.
* This extended time can affect your overall Recovery Time Objective (RTO). Make sure that your recovery plan minimizes disruption.

If the estimated wait time of 4 or more hours does not align with your recovery needs, you can manually mount the R1Soft ISO. Then, you can proceed with the restore without waiting for manual intervention.

To help reduce the time that it takes to recover your Windows server, use the following steps to manually mount the R1Soft ISO.

1. Refer to the [manual ISO mounting instructions](/docs/bare-metal?topic=bare-metal-bm-mount-iso#bm-mount-iso-opt-3).
2. Download the R1Soft Live ISO from [R1Soft live ISO download](https://repo.r1soft.com/bm/serverbackup-bootcd-agent-6.14.2.iso){: external}.
