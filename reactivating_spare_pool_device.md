---



copyright:
  years: 2014, 2018
lastupdated: "2018-11-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Reactivating a device from the spare pool
{: #reactivating-spare-pools}

When a device is added to the spare pool, its status within the Device List changes from Active, indicating that the device is eligible for standard interactions, to Spare Pool. Devices that are part of the spare pool are dedicated to that functionality and may not be used for traditional, day-to-day actions like other devices. To remove a device from the spare pool so that it may return to its traditional functionality, it must be reactivated.
{:shortdesc}

## Reactivating a device from the spare pool

1. Access the [{{site.data.keyword.slportal_full}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
2. Select **Devices > Spare Pool** from the Navigation Bar to access the *Spare Pool* screen.
3. Select **Actions > Reactivate Device** for the desired device.
4. Click **Yes** to reactivate the server. Click **No** to cancel the action.

## Next Steps
After initiating the reactivation process, the device is taken offline, firmware is updated, and the device is available for regular use. The reactivation process takes approximately one hour. Devices that are removed from the spare pool are no longer eligible for use as a failover method. The device can return to the spare pool at any time by adding the device to the spare pool again. For more information, see [Adding a device to the spare pool](../vsi/adding_spare_pool.html).
