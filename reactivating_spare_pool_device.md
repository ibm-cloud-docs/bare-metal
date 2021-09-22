---

copyright:
  years: 2014, 2021
lastupdated: "2021-04-20"

keywords: reactivate spare pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Reactivating a device from the spare pool
{: #bm-reactivating-spare-pools}

When you add a device to the spare pool, the device status within the **Device List** changes from *Active*, indicating that the device is eligible for standard interactions, to *Spare Pool*. Devices that are part of the spare pool are dedicated to the spare pool and can't be used for traditional, day-to-day actions like other devices. To remove a device from the spare pool so that it can return to its traditional function, the device must be reactivated.
{: shortdesc}

## Reactivating a device from the spare pool

1. Access the [{{site.data.keyword.cloud}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/){: new_window} by using your unique credentials.
2. Select **Devices > Spare Pool** from the Navigation Bar to access the *Spare Pool* screen.
3. Select the Actions icon ![Actions icon](../icons/action-menu-icon.svg). Then select **Reactivate Device** for the device.
4. Click **Yes** to reactivate the server. Click **No** to cancel the action.

## Next Steps
{: #reactivate-device-spare-pool-next}

When the reactivation process begins, the device is taken offline, device firmware is updated, and the device is available for regular use. The reactivation process takes approximately 1 hour. The device can return to the spare pool at any time by adding the device to the spare pool again. For more information, see [Adding a device to the spare pool](/docs/bare-metal?topic=bare-metal-adding-spare-pools#adding-spare-pools).
