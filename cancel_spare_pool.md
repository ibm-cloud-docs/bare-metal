---

copyright:
  years: 2014, 2022
lastupdated: "2021-09-20"

keywords: spare pools, cancel, bare metal

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Canceling spare pools
{: #cancel-spare-pools}

Devices that are added to the spare pool can be canceled only from anywhere within the {{site.data.keyword.cloud}} console. The cancellation of a device in the spare pool is identical to that of a device within the **Device List**. 
{: shortdesc}

## Canceling a spare pool
{: #how-to-cancel-spare-pool}

Use the following steps to remove a device from the spare pool.

Canceling a device results in removing all data from the canceled device. All information that is stored on the device cannot be retrieved after the device is canceled.
{: important}

1. Back up any data that you want to keep from the device that you are canceling.
2. Access your [{{site.data.keyword.cloud}} console](https://cloud.ibm.com/){: external} by using your unique credentials.
3. Select **Devices > Spare Pool** from the Navigation Bar to access the *Spare Pool* screen.
4. Select the Actions icon ![Actions icon](../icons/action-menu-icon.svg). Then, select **Cancel Device** for the specific device.
5. Select the cancellation reason from the **Reason** drop-down list.
6. Enter a brief cancellation explanation in the text box.
7. Click **Continue** to proceed to the next screen. Click **Cancel** to stop the cancellation process and return to the *Spare Pool* screen.
8. Select **Data Loss Acknowledgement** to acknowledge that data loss can occur as part of the cancellation process.
9. Click **Cancel Device** to cancel the device. Click **Close** to stop the cancellation process and return to the Spare Pool screen.

## What's next
{: #cancel-spare-next}

After you request the cancellation of a spare pool device, the device is scheduled for cancellation. The device is then immediately reclaimed and removed from the account.
