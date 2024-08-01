---

copyright:
  years: 2019, 2024
lastupdated: "2024-08-01"

keywords:

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Reloading an OS by using an image template
{: #reloading-an-os-using-an-image-template}

During the standard OS Reload process, you select configuration options for the device individually. When you reload from an image template, the configuration loads exactly as it appears in the image template.
{: shortdesc}

## Differences between a standard OS reload and a reload from an image template
{: #differences-between-a-standard-os-reload-and-a-reload-from-an-image-template}

In an image template reload, you can still add features before you reload the OS.

Use the following steps to reload an OS from an image template by using the Load from Image feature.

If you want to retain your data, back up all data before reloading the OS. An OS reload clears all data from the device, so, if you did not back up the data before the reload, it is permanently deleted and cannot be retrieved.
{: important}

## Before you begin
{: #byb-os-reload}

* Go to your console's device menu.
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the `Manage users` classic infrastructure permission, can adjust the permissions.

## Reloading an OS
{: #reload-an-os-image}

1. From the **Device list**, click the server that needs an OS Reload to show the Device Details page.
2. From the **Actions** menu, select **Load from image**.
3. Select the image template checkbox to for the image template to load on to the device.

   Before the reload completes, the image template is copied to the data center that contains the device, if it is not already located in the same data center. If the image template must be copied to the data center, a fee might be charged if the template is not deleted from the location after the OS Reload occurs.
   {: note}

4. Determine whether you want to add any features. Any features that you select are added to the device as part of the reload process.

   | Optional features| Steps |
   | -------------- | -------------- |
   | Yes, I want to add optional features. | i. Click **Load the selected image**.  \n ii. Review the Image Configuration and proceed or cancel.  \n iii. Click Confirm OS Reload to confirm the action and begin the OS reload process. |
   | No, I do not want to add optional features. | Click **View optional features**. |
   {: caption="Table 1. Optional features" caption-side="top"}

5. Configure options, as relevant. Refer to the following information for more details.

   **A postinstallation script** adds an existing or new postinstallation script.

   **SSH key** adds an SSH key to the device upon the reload action.

   **Reset IPMI password** is available only for physical devices.

   **Apply system board BIOS upgrades** action is available only for physical devices.

   **Apply firmware updates for all hard disks** is available only for physical devices.

   **Add to spare spool after OS reload** is available on only physical devices and requires internal approval before its available on an account.

   **Erase all hard disks** action is available on only physical devices and requires special user permissions set by the account administrator.

   **OS reload with disk preservation** configures your current primary disk as a secondary disk (retains all data), and creates a new primary disk. The OS is installed on the new primary disk. Retains all data on the current primary disk during the OS Reload process. Retains all data on the current primary disk during the OS Reload process. Disk preservation converts the primary drive to a Portable Storage device. This option is available only on virtual devices and incurs charges based on the billing patterns (hourly or monthly) of the device. Charges might be canceled by canceling the Portable Storage device anytime after it was created.

6. Click **Load the selected image**.

7. Review the image configuration and click **Next** to proceed to the next screen or **Cancel** to cancel the action.

   After you click **Next**, all network ports for the device are systematically shut down and the device is not available for up to 15 minutes. During this time, the action can be canceled at any time by clicking **Cancel**. The next step must be completed within 15 minutes of clicking **Next** or the previous steps must be completed again. This process is in place as a safeguard to make sure that no additional data is added to a device between the configuration confirmation and the OS Reload initiation.
   {: note}

8. Click **Confirm OS Reload** to confirm the action and begin the OS reload process. Click **Cancel** to cancel the action.

## What's next?
{: #what-s-next-reloading-an-os-using-an-image-template}

After you initiate the OS Reload process, the device is taken offline and the OS Reload process begins.
The time period in which an OS reload takes place varies based on the current and new configuration of the device.
Throughout the configuration process, the minimum time for the OS Reload is displayed on each screen.
The time frame that is displayed is an estimate that is made by the system and is given as a courtesy. If the reload takes longer than 24 hours, contact [support](/docs/get-support?topic=get-support-using-avatar).

When the device returns online, it functions as specified in the new configuration for the OS Reload. All data that is previously saved to the device is lost, but can be restored if a backup was made of the device before its reload. If data was not backed up, it cannot be retrieved.

You need to reregister your device with [IBM Cloud Backup](/docs/Backup?topic=Backup-getting-started#getting-started).
