---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: custom server, {{site.data.keyword.baremetal_short}}, {{site.data.keyword.Bluemix_notm}}

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

## Provisioning through the {{site.data.keyword.cloud_notm}} catalog
{: #provision-through-the-catalog}

Use the following steps to provision your {{site.data.keyword.baremetal_short}} through the {{site.data.keyword.cloud_notm}}.

1. Open the [{{site.data.keyword.cloud_notm}} catalog](https://cloud.ibm.com/catalog/){: external}.   
2. Select {{site.data.keyword.baremetal_short}} under **Compute**.
3. Click Continue.  If you do not see a Continue button, you may need to log in.
4. Enter the **Quantity** of **identical** servers to provision. The default is 1. If you want to provision multiple servers with _different_ specifications, you need to provision the servers separately.
5. **Hostname** is a permanent or temporary name for your servers, for example, baremetal01. Click **Information** for formatting specifics.
6. **Domain** is the identification string that defines administrative control within the Internet, for example, Customer-123456.cloud. Click **Information** for formatting specifics.
7. **Billing** is either **Hourly** or **Monthly**.
8. Select the **Location**, region and data center, where your server is to be located.
9. Click **All servers** to see a list of processors (Single, Dual, and Quad) and certified servers (SAP and VMware). Select the server that best meets your worklaod.
10. Select your **RAM**. For some servers, RAM defaults based on the CPU Model and cannot be changed. 

For SAP certified servers, RAM and Operating System default based on your server selection. Your local storage option also defaults based on your server selection.
{ :note}

11. Enter an optional public key for your **SSH key**, which you can use to log in to yor server after it's provisioned.
12. Select an **Image** (operating system) for your server. Your options are based on the your selected server.
13. Expand **Add-ons** to select options related to the server's configuration.
14. The **Storage disks** are preconfigured based on your server selection. Expand **Add-ons** to add File or Block storage volumes after your {{site.data.keyword.baremetal_short}} have been provisioned. 
15. Under **Network Interface**, select the Uplink Port Speeds and Private VLAN options. Expand **Add-ons** to select the appropriate options or use the default values.
16. Review your order in the Order summary.
17. Enter any promo codes you have under **Apply Promo Code**.
18. Click the third-party service agreements for any listed agreements.
19. Click **Create** to provision your server. You are redirected to a screen with your provisioning order number, which you can print because it's also your receipt.

A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete.

The _provisioning complete_ email includes a link to your *Device Details* page so that you can log in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

You also have the option to save the order as a quote or to add it to an estimate. When you save a quote, a link is sent to the email address associated with your account. Open the link to see the saved quote information. Another option is to go to Manage > Billing and usage, and select Sales > Device quotes. If you have access, you can purchase the quoted offering by clicking the quote and confirming the order. Adding to estimate places the configurations proposed cost in the pricing calculator. Click **Information** for more details about the pricing calculator.

## Provisioning through the customer portal
Use the following steps to provision your {{site.data.keyword.baremetal_short}} through the {{site.data.keyword.slportal}}.

1. Log in to the [{{site.data.keyword.slportal}}](control.softlayer.com){: external} by using your unique credentials.
2. Go to **Account** > **Place an Order**.
3. Choose **Hourly** or **Monthly**.
3. Select your data center where your want your {{site.data.keyword.baremetal_short}} located from the list, and then select your certified server (SAP or VMware) or processor (Single, Dual, and Quad) by clicking the **STARTING PRICE**.
4. Enter the **Quantity** of _identical_ servers to provision. The default is 1. If you want to provision multiple servers with _different_ specifications, you need to provision the servers separately.
5. Select your **RAM**. For some servers, RAM defaults based on the CPU Model and cannot be changed. 

For SAP certified servers, RAM and Operating System default based on your server selection. Your local storage option also defaults based on your server selection.
{ :note}

6. Select your operating system.
7. Select your hard drives and additional system add ons.
8. Click **Add to Order** where you are redirected to confirm your order.
9. Confirm or edit the domain information for the server. **Hostname** is a permanent or temporary name for your servers, for example, baremetal01. 
10. Select **Cloud Service terms** and the **Third-Party Service Agreement**.
11. Enter any promo codes you have under **Promo code** and click **Apply**.
12. Confirm or enter your payment information and click **Submit Order**. You are redirected to a screen with your provisioning order number, which you can print because it's also your receipt. 

A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page, after logging in to {{site.data.keyword.Bluemix_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

## Next Steps
After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
