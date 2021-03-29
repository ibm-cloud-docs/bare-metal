---

copyright:
  years: 2020, 2021
lastupdated: "2021-03-29"

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

# Ordering a bare metal server from an image template
{: #ordering-bm-from-image-template}

After you create an image template, you are ready to create more bare metal servers by using the template.{: shortdesc}

## Ordering a bare metal server from an image template
{: #ordering-bm-from-image-template_steps}

Use the following steps to order a bare metal server from an image template. 

1. Go to the Image templates page by going to **Devices > Manage > Images**.
2. Click the **Action menu** icon  ![Actions menu icon](../icons/action-menu-icon.svg)  for the image template that you want to use and select the type of bare metal server that you want to order.
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
