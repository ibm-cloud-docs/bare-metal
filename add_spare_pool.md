---



copyright:
  years: 2014, 2018
lastupdated: "2018-11-27"

subcollection: bare-metal


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Adding spare pools
{: #adding-spare-pools}

Spare pooling is a form of holding certain devices that are designated as spares and have the ability to take over the workflow of a primary device or act as a new device in the customer fleet. For a device to be designated as a spare, it must be added to the spare pool and associated to a primary device. Follow the steps below to add a device to the spare pool.
{:shortdesc}

1. Access the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
2. Select **Devices > Spare Pool** from the Navigation Bar to access the *Spare Pool* screen.
3. Click the **Add to Spare Pool** link.

   A list of devices eligible to be added to the spare pool will be populated.
   {:tip}

4. Select the devices to be added to the spare pool.
5. Click **Add Selected Devices**.
6. Click **Confirm** to add the devices to the spare pool.

## Next Steps
After initiating a device's transfer to the spare pool, the device is transitioned to the spare pool within one hour. After the device is active in the spare pool, it is displayed on the Spare Pool screen and can be designated as a hot spare for a primary device.
