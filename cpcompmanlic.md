---

copyright:

  years: 1994, 2024
lastupdated: "2024-07-19"

keywords: active control panel software, control panel licenses window, download license files, devices, canceling license

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Managing control panel licenses
{: #cp_compacclisc}

You can manage the licenses for active control panel software, like cPanel and Parallels, from the {{site.data.keyword.cloud_notm}} console on the Control Panel Licenses window. You can view licenses and their associated IPs, download license files, and cancel individual licenses.
{: shortdesc}

## Before you begin
{: #byb-cp-compacclisc}

First, go to the device menu and make sure that you have the correct account permissions to complete the tasks.

* Go to your console's device menu.
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

## Downloading a control panel license to a device
{: #download-cp-compdllisc}

A license file is used to verify that the license is valid for software on a device, and any software features that are enabled. You can download license files from the {{site.data.keyword.cloud_notm}} console, but only on the device that runs the corresponding control panel software. Use the following steps to download a license file.

1. Select **Devices** > **Manage** > **Control panel licenses** from the menu to access the control panel licenses window.
2. Select **Actions > Download license file** for the license.
3. Save or download the file to the control panel software on the device by using the prompts provided by the device's operating system.

After you download the license file to the device, the control panel software's details about the license are updated. If issues occur or if the download wasn't successful, try the download process again by repeating the previous steps.

## Canceling a control panel license
{: #cancel-cp-compcanlisc}

Control panel licenses are invoiced monthly, based on the agreed-upon terms at the time the license was purchased. You can cancel licenses at any time and they're canceled on the next upcoming billing anniversary date. To make sure that a cancellation is applied to the current billing cycle, cancellations must be made no less than 24 hours before the billing anniversary date. Specific information on the billing anniversary for the account is displayed during the cancellation process. Use the following steps to cancel a control panel license.

1. Back up or transfer any data that is associated with the control panel license.
2. Select **Devices** > **Manage** > **Control panel licenses** from the menu to access the control panel licenses window.
3. Select **Actions** > **Cancel** for the control panel license that you want to cancel.
4. Enter any notes about the cancellation in the **Notes** text box.
5. Click **Continue** to proceed to the confirmation screen.
6. Select the **Data loss acknowledgment** checkbox. If you didn't back up any important data, return to the first step and back up all data before you cancel the license.
7. Click **Cancel the license**.

After you start the cancellation process, the control panel license is scheduled for cancellation for the upcoming billing anniversary date. If the cancellation was made in error, you can void the cancellation on the Cancellations screen in the {{site.data.keyword.cloud_notm}} console.

## Managing software passwords
{: #manage-software-passwords}

To manage the passwords for the software on each device, see [Managing software passwords](/docs/bare-metal?topic=bare-metal-cp_bpmanacctresp)
