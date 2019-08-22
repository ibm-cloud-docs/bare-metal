---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

keywords: spare pools, cancel, bare metal

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Canceling spare pools
{: #cancel-spare-pools}

Devices that have been added to the spare pool may only be canceled from the Spare Pool screen within the {{site.data.keyword.cloud}} console. The cancellation of a device in the spare pool is identical to that of a device within the Device List. Follow the steps below to cancel a device in the spare pool.
{:shortdesc}

## Canceling spare pools

1. Back up any data that you want to keep from the device being canceled.

   Canceling a device results in all data being removed from the canceled device. All information that is stored on the device cannot be retrieved after the device is canceled.
   {:tip}

2. Access the [{{site.data.keyword.cloud}} console ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/){: new_window} by using your unique credentials.
3. Select **Devices > Spare Pool** from the Navigation Bar to access the *Spare Pool* screen.
4. Select **Actions > Cancel Device** for the specific device.
5. Select the cancellation reason from the **Reason** drop-down list.
6. Enter a brief cancellation explanation in the text box provided.
7. Click **Continue** to proceed to the next screen. Click **Cancel** to stop the cancellation process and return to the Spare Pool screen.
8. Select **Data Loss Acknowledgement** to acknowledge that data loss can occur as part of the cancellation process.
9. Click **Cancel Device** to cancel the device. Click **Close** to stop the cancellation process and return to the Spare Pool screen.

## Next Steps
{: #cancel-spare-next}
After requesting cancellation of a device in the spare pool, the device is scheduled for cancellation. The device is then immediately reclaimed and removed from the account.
