---

copyright:
  years: 2014, 2021
lastupdated: "2019-07-30"

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
{: shortdesc}

## Before you begin
{: #bm-port-control-before}

* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Ensure you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/account?topic=account-infrapermission) and [Managing device access](/docs/virtual-servers?topic=virtual-servers-managing-device-access).

## Manage the port control for a device
{: #bm-manage-port-control}

1. Access the **Device List** and select the **Device Name** to update.  
2. Click the **Speed** drop-down and select a network port speed.
3. Confirm your selected speed and click **Update**.

## Next Steps
{: #manage-portal-control-next-steps}

If you selected **Disabled**, network access for the disabled port ceases for the device interface. If you selected **Enabled**, network access is available for the enabled port. Port control remains in the selected setting until manually changed.
