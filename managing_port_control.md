---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-18"

keywords: manage bare metal port control

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Managing port control for a device
{: #bm-manage-port-control}

Each device that is associated with an account has two network ports that receive incoming traffic – one for public network traffic and one for private network traffic. You can enable or disable these ports at any time to control the network traffic that a device receives. Complete the following steps to update the port control settings for a device.

## Before you begin
* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/bare-metal?topic=virtual-servers-managing-device-access).

## Manage the port control for a device

1. Access the **Device List** and select the **Device Name** to update.  
2. Click the **Actions** drop-down list for the device.
3. Select **Port Control**.
4. Update the *Public Network* and/or *Private Network* drop-down boxes by completing one of the following actions:
   * Select desired speed to enable network access.
   * Select Disconnected to disable network access.
5. Click the Update button.
6. Click the Close button to close the window.

## Next Steps

If you selected **Disabled**, network access for the disabled port ceases for the device interface. If you selected **Enabled**, network access is available for the enabled port. Port control remains in the selected setting until manually changed.
