---


copyright:
  years: 2019, 2022
lastupdated: "2022-04-20"

keywords: OS Reload, operating system

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Reloading the OS
{: #reloading-the-os}

You can reload the operating system (OS) on a device at any time to restore a device to its original working order. Or you can reconfigure a device with a different operating system or software. An OS reload removes all data from the device and applies a "like new" configuration, as specified during the configuration process of the OS reload setup. Because OS reloads clear all data from the device, if the data is not backed up before the reload, the data is permanently deleted and can't be retrieved.
{: shortdesc}

If you want to retain your data, back up all data before you perform an OS reload.
{: important}

## Before you begin
{: #byb-reloading-os}

* Go to the console device menu. For more information, see [Navigating to devices](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage users** Classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Reloading the OS and software
{: #reload-the-os}

1. From the **Device list**, click the server that needs an OS reload to show the _Device details_ page.
2. From the **Actions** menu, select **OS reload**.
3. Determine whether you want to reload the existing configuration or reload the device with a new configuration.

   | Reload type | Steps |
   |-------------|-------|
   | If you want to reload a new configuration... | 1. Click **Edit** for the category that requires an update.  \n 2. Select the new software from the **Select software** drop-down list. |  
   | If you want to reload the existing configuration... | Proceed to the next step. |
   | If you want to change the operating system... | 1. Click **Edit OS** > **Change version or manufacturer**. |
   {: caption="Table 1. OS and software reload options" caption-side="top"}

4. Determine whether to apply a postinstallation script after the device is provisioned.

   If you want to apply a postinstallation script, select the script from the **Existing script** drop-down list or enter the qualified URL for the new script.  Otherwise, proceed to the next step.

5. For physical devices, determine whether to add or remove installed partitions or if they need to remain unchanged.

   | Partition action | Steps |
   |------------------|-------|
   | To add installed partitions... | 1. Click **Add another partition**.  \n 2. Enter the exact name of the partition.  \n 3. Enter the partition size (in GB).  \n Optionally, you can select **Grow** to grow the partition to fill the remaining disk space. Keep in mind that you can only one partition can be selected to grow at any time. This partition is larger than the specified size, and fills all available capacity. The capacity of the grow partition is calculated by subtracting the combined size of all other partitions from the total capacity number that is provided in the Installed Partitions section. |
   | To delete installed partitions... | Click **Delete** to delete the partition. |
   | To remain unchanged... | Proceed to the next step. |
   {: caption="Table 2. Partition action options" caption-side="top"}

6. Determine whether to apply one or more SSH keys to the device.

7. Select the applicable checkboxes for the options that you want to apply to the device during or after the OS reload.

   Options vary based on device. Not all options are available for every device.
   {: note}
   
   **Post installation script** Adds an existing or new postinstallation script.
   
   **SSH key** Adds an SSH key to the device upon the reload action.
   
   **Reset IPMI password** This option is available only for physical devices.
   
   **Apply system board BIOS upgrades** This option is available only for physical devices.
   
   **Apply firmware updates for all hard disks** This option is available only for physical devices.
   
   **Add to spare pool after OS reload** This option is available only on physical devices and requires internal approval before it's available on an account.
   
   **Erase all hard disks** This option is available only on physical devices and requires special user permissions set by the account administrator.
   
   **OS reload with disk preservation** This option configures your current primary disk as a secondary disk (retaining all data), and creates a new primary disk. The OS is installed on the new primary disk. Retains all data on the current primary disk during the OS reload process. Retains all data on the current primary disk during the OS reload process. Disk preservation converts the primary drive to a portable storage device. This option is available only on virtual devices and incurs charges based on the billing patterns (hourly or monthly) of the device. Charges might be canceled by canceling the portable storage device anytime after it was created.

8. Click **Reload with configuration** to proceed to review. Click **Cancel** to cancel the changes to the device and exit the screen.

9. Verify that all details in the _New configuration_ section are correct.  

10. Click **Confirm OS reload** to confirm and initiate the OS reload. Click **Cancel** to cancel the action.

## What's next?
{: #what-s-next-reloading-the-os}

After you initiate the OS reload process, the device is taken offline and the OS reload process begins.
The time period in which an OS reload takes place varies based on the current and new configuration of the device.
Throughout the configuration process, the minimum time for the OS reload is displayed on each screen.
The timeframe that is displayed is an estimate that is generated by the system. If the reload takes longer than 24 hours, contact {{site.data.keyword.cloud}} Support.

When the device returns online, it functions as specified in the new configuration for the OS reload. All data that was saved to the device is lost, but can be restored if you created a backup of the device before the OS reload. If data wasn't backed up, it cannot be retrieved.

You need to reregister your device with [IBM Cloud Backup](/docs/Backup?topic=Backup-getting-started).
