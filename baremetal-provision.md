---

copyright:
  years: 2017, 2021
lastupdated: "2021-08-26"

keywords: custom server, {{site.data.keyword.baremetal_short}}, {{site.data.keyword.cloud_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# Building a custom Bare Metal Server
{: #ordering-baremetal-server}

Use the following steps to build a custom {{site.data.keyword.baremetal_long}}.

## Before you begin

Make sure that you review the [Getting started tutorial](https://test.cloud.ibm.com/docs/bare-metal?topic=bare-metal-getting-started) before you begin the provisioning process.

## Provisioning through the {{site.data.keyword.cloud_notm}} catalog
{: #provision-through-the-catalog}

Use the following steps to provision your {{site.data.keyword.baremetal_short}} through the {{site.data.keyword.cloud_notm}}.

1. Open the [{{site.data.keyword.cloud_notm}} catalog](https://cloud.ibm.com/catalog/){: external}.   
2. Select {{site.data.keyword.baremetal_short}} under **Compute**.
3. Click Continue. If you do not see a Continue button, you might need to log in.
4. Enter the **Quantity** of **identical** servers to provision. The default is 1. If you want to provision multiple servers with _different_ specifications, you need to provision the servers separately.
5. **Hostname** is a permanent or temporary name for your servers, for example, baremetal01. Click **Information** for formatting specifics.
6. **Domain** is the identification string that defines administrative control within the internet, for example, Customer-123456.cloud. Click **Information** for formatting specifics.
7. **Billing**, select either **Hourly**, **Monthly**, **1-year term**, or a **3-year term**.
8. Select the **Location**, region and data center, where your server is to be located.
9. Click **All servers** to see a list of processors (Single, Dual, and Quad) and certified servers (SAP and VMware). Select the server that best meets your workload.
10. Select your **RAM**. For some servers, RAM defaults based on the CPU Model and cannot be changed. **Note:** For SAP certified servers, RAM and Operating System default based on your server selection. Your local storage option also defaults based on your server selection.
11. Enter an optional public key for your **SSH key**, which you can use to log in to your server after it is provisioned.
12. Select an **Image** (operating system) for your server. Your options are based on your selected server.
13. Expand **Add-ons** to select options related to the server's configuration.
14. The **Storage disks** are preconfigured based on your server selection. Expand **Add-ons** to add File or Block storage volumes after your {{site.data.keyword.baremetal_short}} are provisioned.
15. Under **Network Interface**, select the Uplink Port Speeds and Private VLAN options. Expand **Add-ons** to select the appropriate options or use the default values.
16. Review your order in the Order summary.
17. Enter any promo codes that you have under **Apply Promo Code**.
18. Click the third-party service agreements for any listed agreements.
19. Click **Create** to provision your server. You are redirected to a screen with your provisioning order number, which you can print because it's also your receipt.

A series of emails is sent to your administrator: Acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete.

The _provisioning complete_ email includes a link to your *Device Details* page so that you can log in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.cloud}} console.

You can also order as a quote or to add it to an estimate. When you save a quote, a link is sent to the email address associated with your account. Open the link to see the saved quote information. Another option is to go to Manage > Billing and usage, and select Sales > Device quotes. If you have access, you can purchase the quoted offering by clicking the quote and confirming the order. Adding to estimate places the configurations proposed cost in the pricing calculator. Click **Information** for more details about the pricing calculator.

## Next Steps
{: #provision-next-steps}

After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers).
