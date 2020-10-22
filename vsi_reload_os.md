---



copyright:
  years: 2019, 2020
lastupdated: "2020-01-30"

keywords: OS Reload, operating system

subcollection: bare-metal
---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

#  Reloading the OS
{: #reloading-the-os}

You can reload the operating system (OS) on a device at any time to restore a device to its original working order, or to reconfigure a device with different software. An OS reload removes all data from the device and applies a "like new" configuration, as specified during the configuration process of the OS Reload setup. Because OS reloads clear all data from the device, if the data is not backed up before the reload, it's permanently deleted and cannot be retrieved.
{:shortdesc}

**Important:** If you want to retain your data, back up all data before you perform an OS reload.

## Before you begin
* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Reload the OS
{: #reload-the-os}

1. From the **Device List**, click the server that needs an OS Reload to show the Device Details page.
2. From the **Actions** menu, select **OS Reload**.
3. Determine whether you want to reload the existing configuration or reload the device with a new configuration.

| Reload type | Steps |
|-------------|-------|
| If you want to reload a new configuration... | 1. Click <b>Edit</b> for the Category that requires an update.<br>2. Select the new software to apply to the device from the **Select Software** drop down list. |  
| If you want to reload the existing configuration... | Proceed to the next step. |
{: caption="Table 1. OS reload options" caption-side="top"}

4. Determine whether to apply a post-installation script after the device is provisioned.

   If you want to apply a post-installation script, select the script from the Existing Script drop down list or enter the qualified URL for the new script.  Otherwise, proceed to the next step.

5. For physical devices, determine whether to add or remove installed partitions or if they should remain unchanged.

| Partition action | Steps |
|------------------|-------|
| To add installed partitions... | 1. Click **Add Another Partition**.<br> 2. Enter the exact name of the partition.<br> 3. Enter the partition size (in GBs). If you want, you can select Grow to grow the partition to fill the remaining disk space.<br><br> **Note**: Only one partition can be selected to grow at any time. This partition is larger than the specified size, and fills all available capacity. The capacity of the Grow partition is calculated by subtracting the combined size of all other partitions from the Total Capacity number that is provided in the Installed Partitions section. |
| To delete installed partitions... | Click **Delete** to delete the partition. |
| To remain unchanged... | Proceed to the next step. |
{: caption="2. Partition action options" caption-side="top"}

6. Determine whether to apply one or more SSH Keys to the device.

7. Select the applicable checkboxes for the options that you want to apply to the device during or after the OS reload.

   **Note:** Options vary based on device. Not all options are available for every device.
      <dl>
   <dt>Post Install script</dt>
   <dd>Adds an existing or new post-installation script.</dd>
   <dt>SSH key</dt>
   <dd>Adds an SSH key to the device upon the reload action. </dd>
   <dt>Reset IPMI Password</dt>
   <dd> This option is only available for physical devices. </dd>
   <dt>Apply system board BIOS upgrades</dt>
   <dd>This option is only available for physical devices. </dd>
   <dt>Apply firmware updates for all hard disks</dt>
   <dd>This option is only available for physical devices.</dd>
   <dt>Add to Spare Pool after OS Reload</dt>
   <dd>This option is available only on physical devices and requires internal approval before being available on an account.</dd>
   <dt>Erase all hard disks</dt>
   <dd> This option is available only on physical devices and requires special user permissions set by the Account's administrator.</dd>
   <dt>OS Reload with Disk Preservation</dt>
   <dd>This option configures your current primary disk as a secondary disk (retaining all data), and creates a new primary disk. The OS is installed on the new primary disk. Retains all data on the current primary disk during the OS Reload process. Retains all data on the current primary disk during the OS Reload process. Disk preservation converts the primary drive to a Portable Storage device. This option is available only on virtual devices and incurs charges based on the billing patterns (hourly or monthly) of the device. Charges might be canceled by canceling the Portable Storage device any time after it was created.</dd>
   </dl>

8. Click **Reload Above Configuration** to proceed to review. Click **Cancel** to cancel the changes to the device and exit the screen.

9. Verify that all details in the New Configuration section are correct.  

10. Click **Confirm OS Reload** to confirm and initiate the OS Reload. Click **Cancel** to cancel the action.

## What's Next?
{: #what-s-next-reloading-the-os}

After you initiate the OS reload process, the device is taken offline and the OS Reload process begins.
The time period in which an OS reload takes place varies based on the current and new configuration of the device.
Throughout the configuration process, the minimum time for the OS Reload is displayed on each screen.
The timeframe that is displayed is an estimate that is generated by the system. If the reload takes longer than 24 hours, contact IBM Support.

When the device returns online, it functions as specified in the new configuration for the OS Reload. All data that is previously saved to the device is lost, but can be restored if you created a backup of the device before the OS reload. If data was not backed up, it cannot be retrieved.

You need to reregister your device with IBM Cloud Backup.
