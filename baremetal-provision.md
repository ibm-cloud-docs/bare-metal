---

copyright:
  years: 2017, 2022
lastupdated: "2022-04-13"

keywords:

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}


# Building a custom bare metal server
{: #ordering-baremetal-server}

Use the following steps to build a custom {{site.data.keyword.baremetal_long}}.
{: shortdesc}

## Before you begin
{: #byb-custom-baremetal-server}

Make sure that you review the [Getting started tutorial](https://test.cloud.ibm.com/docs/bare-metal?topic=bare-metal-getting-started) before you begin the provisioning process.

## Provisioning through the {{site.data.keyword.cloud_notm}} catalog
{: #provision-through-the-catalog}

Use the following steps to provision your {{site.data.keyword.baremetal_short}} through the {{site.data.keyword.cloud_notm}}.

1. Open the [{{site.data.keyword.cloud_notm}} catalog](https://cloud.ibm.com/catalog/){: external}.   
1. Select {{site.data.keyword.baremetal_short}} under **Compute**.
1. Click **Continue**. If you do not see a **Continue** button, you might need to log in.
1. In the Bare Metal Servers section, select the following information:

   | Field | Value |
   | ----- | ----- |
   | Quantity | Enter the **Quantity** of **identical** servers to provision. The default quantity is _1_. If you want to provision multiple servers with _different_ specifications, you need to provision the servers separately. |
   | Hostname | Permanent or temporary name for your servers, for example, baremetal01. Click **Information** for formatting specifics. |
   | Domain | Identification string that defines administrative control within the internet, for example, Customer-123456.cloud. Click **Information** for formatting specifics. |
   | Billing | Select either **Hourly**, **Monthly**, **1-year term**, or a **3-year term**. |
   | Location |  Region and data center where your server is to be located. |
   | Select your server | Select the server that best meets your workload. |
   | RAM |  For some servers, RAM defaults are based on the CPU model and can't be changed. Keep in mind that for SAP certified servers, RAM, and operating system default is based on your server selection. Your local storage option also defaults based on your server selection. |
   | SSH keys | Enter an optional public key of your SSH key that you can use to log in to your server after it is provisioned. |
   | Image (operating system) | Select an image for your server. Your options are based on your selected server. |
   | Add-ons | Expand the **Add-ons** section to select the appropriate options or use the default values. |
   | Storage disks | Storage disks are preconfigured based on your server selection. You can expand **Add-ons** to add file or block storage volumes after your {{site.data.keyword.baremetal_short}} are provisioned.  \n Because of compatibility issues, you can’t select NMVe drives if you’re going to install Windows&reg;. |
   | Network interface | Select the uplink port speeds and private VLAN options. Expand **Add-ons** to select the appropriate options or use the default values. |
   {: caption="Table 1: Custom bare metal server selections" caption-side="top"}

1. Review your order in the Order summary.
1. Enter any promo codes that you have under **Apply Promo Code**.
1. Click the third-party service agreements for any listed agreements.
1. Click **Create** to provision your server. You are redirected to a screen with your provisioning order number, which you can print because it's also your receipt.

A series of emails is sent to your administrator: Acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The _provisioning complete_ email includes a link to your *Device Details* page so that you can log in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.cloud}} console.
{: note}

### Provisioning by using a quote 
{: #provision-by-using-quote}

You can also provision a {{site.data.keyword.baremetal_short}} with a quote or add it to an estimate. When you save a quote, a link is sent to the email address associated with your account. Open the link to see the saved quote information. 

Another option is to go to **Manage** > **Billing and usage** > **Sales** > **Device quotes**. If you have access, you can purchase the quoted offering by clicking the quote and confirming the order. Adding to estimate places the configurations proposed cost in the pricing calculator. Click **Information** for more details about the pricing calculator.

## Next Steps
{: #provision-next-steps}

After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers).
