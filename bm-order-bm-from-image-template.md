---

copyright:
  years: 2020
lastupdated: "2020-11-11"

keywords: custom image template, bare metal image, image template, order image template

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:tip: .tip}
{:note: .note}
{:beta: .beta}

# Ordering a bare metal server from an image template (Beta)
{: #ordering-bm-from-image-template}

The {{site.data.keyword.baremetal_long}} custom image templates feature is classified as beta and is available for evaluation and testing purposes. Which means that it might be unstable and can change frequently. Beta features also might not provide the same level of performance or compatibility that generally available features provide and are not intended for use in a production environment.
{: beta}

## Before you begin
{: #byb-bm-order-image-template}

Navigate to the device menu and ensure you have the correct account permissions to complete the tasks.

* Navigate to your console's device menu. For more information, see [Navigating to devices](/docs/image-templates?topic=virtual-servers-navigating-devices).
* Make sure that you have any necessary account permissions and device access. Only the account owner, or a user with the **Manage Users** classic infrastructure permission, can adjust the permissions.

For more information about permissions, see [Classic infrastructure permissions](/docs/iam?topic=iam-infrapermission#infrapermission) and [Managing device access](/docs/vsi?topic=virtual-servers-managing-device-access).

## Ordering a bare metal server from an image template
{: #ordering-bm-from-image-template_steps}

Use the following steps to order a bare metal server from an image template. 

1. Go to the Image templates page by going to **Devices > Manage > Images**.
2. Click the Action menu icon ![Actions menu icon](../icons/action-menu-icon.svg) for the image template that you want to use and select the type of bare metal server that you want to order.
3. Click **Order Bare Metal**.
4. Enter the **Quantity** of servers to provision. 
5. **Hostname** is a permanent or temporary name for your servers, for example, baremetal01. Click **Information** for formatting specifics.
6. **Domain** is the identification string that defines administrative control within the internet, for example, `Customer-123456.cloud`. Click **Information** for formatting specifics.
7. **Billing** is either **Hourly** or **Monthly**.
8. Locations are filtered based on where the image is available. You might see a subset of locations to choose from. 
9. Servers are filtered based on the supported hardware of your image. Select your server from the available options.
10. Select your **RAM**. For some servers, RAM defaults based on the CPU model and cannot be changed. 
11. Enter an optional public key for your **SSH key**, which you can use to log in to your server after it is provisioned.
12. Expand **Add-ons** to select options that are related to the image configuration.
13. Your storage selection defaults to the storage disks that were used during the image capture. <!--Keep the default selection.-->**Note:** You can't mix RAID and non-RAID storage disks.
14. Under **Network Interface**, select the Uplink Port Speeds and Private VLAN options. Expand **Add-ons** to select the appropriate options or use the default values.
15. Review your order in the Order summary.
16. Click the **Third-Party Service Agreement** checkbox.
17. Click **Create**. An email is sent when your bare metal server is provisioned.

