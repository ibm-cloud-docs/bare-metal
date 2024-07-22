---

copyright:
  years: 2014, 2024
lastupdated: "2024-07-19"

keywords: manage port control, managing port control, device port control

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Managing port control for a device
{: #bm-manage-port-control}

Each device that is associated with an account has two network ports that receive incoming traffic – one for public network traffic and one for private network traffic. You can enable or disable these ports at any time to control the network traffic that a device receives.
{: shortdesc}

## Before you begin
{: #bm-port-control-before}

* Go to your console's device menu.
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage users** classic infrastructure permission, can adjust the permissions.

## Manage the port control for a device
{: #bm-manage-port-control}

Complete the following steps to update the port control settings for a device.

1. Access the **Device list** and select the **Device name** to update.
2. Click **Actions** to select one of the following available actions.
   | Action | Description |
   | ------ | ----------- |
   | Enable | Sets port to **Active** on all available interfaces. |
   | Enable (Degraded) | Sets port to **Active** on only the primary interface. |
   | Upgrade port speed | Updates the port speed to the maximum available speed and sets port to **Active** on all available interfaces. |
   | Upgrade port speed (Degraded) | Updates the port speed to the maximum available speed and sets port to **Active** on only the primary interface. |
   | Disable | Sets device to **Off**. |
   {: caption="Table 1. Device port control options" caption-side="top"}

3. Click **Update** to confirm your selection.

## Next steps
{: #manage-portal-control-next-steps}

If you selected **Disabled**, network access for the disabled port ceases for the device interface. If you selected **Enabled**, network access is available for the enabled port. Port control remains in the selected setting until manually changed.
