---

copyright:
  years: 2019, 2021
lastupdated: "2021-09-15"

keywords: image template, OS Reload, operating system

subcollection: bare-metal
---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# Reloading an OS using an image template
{: #reloading-an-os-using-an-image-template}

## Differences between a standard OS reload and a reload from an image template
{: #differences-between-a-standard-os-reload-and-a-reload-from-an-image-template}

During the standard OS Reload process, you select configuration options for the device individually. When you reload from an image template, the configuration loads exactly as it appears in the image template.

In an image template reload, you can still add features before reloading the OS.

Use the following steps to reload an OS from an image template by using the Load from Image feature in the Customer Portal.

**Important:** If you want to retain your data, back up all data before reloading the OS. An OS reload clears all data from the device, so, if you did not back up the data before the reload, it is permanently deleted and cannot be retrieved.
{:shortdesc}

## Before you begin
* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

##Reload an OS
{: #reload-an-os-image}

1. From the **Device List**, click the server that needs an OS Reload to show the Device Details page.
2. From the **Actions** menu, select **Load from Image**.
3. Select the image template check box to for the image template to load on to the device.

   Before completing the reload, the image template is copied to the data center that contains the device, if it is not already located in the same data center. If the image template must be copied to the data center, an fee might be charged if the template is not deleted from the location after the OS Reload occurs.
   {:note: .note}

4. Determine whether you want to add any features. Any features that you select are added to the device as part of the reload process.

   <table>
   <CAPTION>Table 1. Optional features</CAPTION>
   <THEAD>
   <TR>
   <th>Optional Features</th>
   <th>Steps</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   </tr>
   <tr>
   <td>Yes, I want to add optional features.</td>
   <td>
   <ol>
   <li>Click <b>Load Selected Image</b>.</li>
   <li>Review the Image Configuration and proceed or cancel.</li>
   <li>Click <b>Confirm OS Reload</b> to confirm the action and begin the OS reload process.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>No, I do not want to add optional features.</td>
   <td>Click <b>View Optional Features</b>.</td>
   </tr>
   </TBODY>
   </table>

5. Configure options, as relevant. Refer to the following information for more details.

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

6. Click **Load Selected Image**.

7. Review the image configuration and click **Next** to proceed to the next screen or **Cancel** to cancel the action.

   After you click **Next**, all network ports for the device are systematically shut down and the device is unavailable for up to 15 minutes. During this time, the action can be canceled at any time by clicking **Cancel**. The next step must be completed within 15 minutes of clicking **Next** or the previous steps must be completed again. This process is in place as a safeguard to ensure that no additional data is added to a device between the configuration confirmation and the OS Reload initiation.
   {:note: .note}

8. Click **Confirm OS Reload** to confirm the action and begin the OS reload process. Click **Cancel** to cancel the action.

## What's Next?
{: #what-s-next-reloading-an-os-using-an-image-template}

After you initiate the OS Reload process, the device is taken offline and the OS Reload process begins.
The time period in which an OS reload takes place varies based on the current and new configuration of the device.
Throughout the configuration process, the minimum time for the OS Reload is displayed on each screen.
The time frame timeframe that is displayed is an estimate made by the system and is given as a courtesy. If the reload takes longer than 24 hours, contact IBM Support.

When the device returns online, it functions as specified in the new configuration for the OS Reload. All data that is previously saved to the device is lost, but can be restored if a backup was made of the device before its reload. If data was not backed up, it cannot be retrieved.

You will need to re-register your device with IBM Cloud Backup.
