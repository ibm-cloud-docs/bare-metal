---

copyright:
  years: 2023, 2024
lastupdated: "2024-06-18"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Disks are not displayed in the operating system
{: #bm-disk-not-displaying-OS}
{: troubleshoot}
{: support}

You purchased an extra disk, but you can't access it in the OS.
{: tsSymptoms}

The disk might not be authorized or mounted.
{: tsCauses}

Use the following information to authorize and or attach storage and how to mount it for both Windows and Linux servers.

Windows

   * Portable storage

   Verify that you attached the disk to the virtual server in the {{site.data.keyword.cloud}} Portal. For more information, see [Managing portable storage](/docs/virtual-servers?topic=virtual-servers-accessing-portable-storage).

   After you attach the storage to the virtual server, log on to your Windows server and open the disk management window by using the following steps.

      1. Click the Start button, select “Windows Administrative Tools” and double-click “Computer Management”.
      1. Select “Storage” > “Disk Management”. If your disk is larger than 2 TB, then select GPT, if not, you can select either MBR or GPT.
      1. Click OK.
      1. The new disk shows up in the list as “Unallocated”. If it doesn’t, then right-click “Disk Management” and select “Rescan Disks”.
      1. Right-click the disk and select “New Simple Volume”. Follow the steps in the Wizard.

      The disk is now be visible with status “Healthy” and you can see it in the file explorer.

   * Block Storage

   To connect to iSCSI LUNS from a Windows server, see [Connecting to iSCSI LUNS on Microsoft Windows](/docs/BlockStorage?topic=BlockStorage-mountingWindows&interface=ui).

Linux

If you ordered a new disk for your server but cannot see it in Linux, it might be because of one or more of the following reasons.

   * Portable Storage

   Verify that you attached the disk to the virtual server in the {{site.data.keyword.cloud}} Portal. For more information, see [Managing portable storage](/docs/virtual-servers?topic=virtual-servers-accessing-portable-storage).

   You can see the new disk by logging on to your Linux virtual server and running the `lsblk` command.

   The command returns something similar to the following example. In the example, the new disk is _xvdc_.

      # lsblk

      NAME    MAJ:MIN RM SIZE RO TYPE MOUNTPOINT

      xvda    202:0    0  25G  0 disk

      ├─xvda1 202:1    0   1G  0 part /boot

      └─xvda2 202:2    0  24G  0 part /

      xvdb    202:16   0   2G  0 disk

      └─xvdb1 202:17   0   2G  0 part [SWAP]

      xvdc    202:32   0  10G  0 disk

      xvdh    202:112  0  64M  0 disk

   You need to partition the disk before you can use it. For more information, see [Red Hat Storage Admin Guide](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/s2-disk-storage-parted-create-part){: external}.

   After you partition the disk, it looks similar to the following example.

      # lsblk

      NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT

      xvda    202:0    0   25G  0 disk

      ├─xvda1 202:1    0    1G  0 part /boot

      └─xvda2 202:2    0   24G  0 part /

      xvdb    202:16   0    2G  0 disk

      └─xvdb1 202:17   0    2G  0 part [SWAP]

      xvdc    202:32   0   10G  0 disk

      └─xvdc1 202:33   0  9.3G  0 part

      xvdh    202:112  0   64M  0 disk

   After the disk is partitioned, you need to mount the disk.

   If you want the disk to remain mounted after each restart, you need to update `/etc/fstab`.
   {: tip}

   * Block Storage

   To authorize and mount block storage LUN to a Linux server, see [Mount iSCSI LUN on Red Hat Enterprise Linux 8](/docs/BlockStorage?topic=BlockStorage-mountingRHEL8&interface=ui).

   * File Storage

   To authorize and mount file storage on a Linux server, see [Mounting File Storage for Classic on Red Hat Linux](/docs/FileStorage?topic=FileStorage-mountingLinux&interface=ui).

   If you can't see the new disk in your operating system, [contact {{site.data.keyword.cloud}} Support](/docs/bare-metal?topic=bare-metal-gettinghelp).
{: tsResolve}
