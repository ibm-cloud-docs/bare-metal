---

copyright:
  years: 2017, 2019
lastupdated: "2018-11-12"

keywords: custom server, build custom {{site.data.keyword.baremetal_short}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Building a custom {{site.data.keyword.baremetal_short}}
{: #ordering-baremetal-server}

Use the following steps to build a custom {{site.data.keyword.baremetal_short}}.

1. Open the [{{site.data.keyword.cloud_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/){: new_window}.   
2. Select {{site.data.keyword.baremetal_short}}.
3. Click Continue.  If you do not see a Continue button, you may need to log in.
2. In the {{site.data.keyword.baremetal_short}} section, select the following information:
    <table>
    <CAPTION>Table 1. Bare metal selections</CAPTION>
    <THEAD>
    <TR>
    <th>Field</th>
    <th>Value</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantity</td>
    <td>Use the + and - icons to specify the number of **identical** servers to provision. The default is 1.<br>If you want to provision multiple servers with **different** specifications, you need to provision them separately.
    <tr>
    <tr>
    <td>Billing type</td>
    <td>Select Hourly or Monthly
    <tr>
    <td>Hostname and Domain</td>
    <td>These fields are populated with default. You can change them.</td>
    </tr>
    <td>Location</td>
    <td>Select the region and data center where you want the server to be located.</td>
    </tr>
    <tr>
    <tr>
    <td>Select your server</td>
    <td>1. Select **All Servers**. <br>2. Select the processor type (Single, Dual, Quad, SAP Certified, or GPU) that you need.<br>3. Select the CPU model that you need.
    </td>
    </tr>
    <tr>
    <td>RAM</td>
    <td>Select the amount of RAM you need on your machine. Your choices may be limited by the server that you selected.</td>
    </tr>
    <tr>
    <td>SSH Keys</td>
    <td>Provide a public key of your SSH key, which you use to log in to your server after it is provisioned.</td>
    </tr>
    <tr>
    <td>Image <br>(Operating System)</td>
    <td>Select the operating system for the server. Your Image options may be limited based on the server you selected.</td>
    </tr>
    <td>Add-ons</td>
    <td>Expand the Add-ons section to select the appropriate options or use the default values.</td>
    </tr>
    </TBODY>
    </table>
5. In the Storage Disks section, select your disk specifications. Click Add new to add more storage disks.
Expand the Add-ons section for more storage options.
4. In the Network Interface section, select the Uplink Port Speeds and Private VLAN options. Expand the Add-ons section to select the appropriate options or use the default values.
4.  Review your order.
4. If you have a promo code to apply to your order, expand Apply Promo Code.
5.  Review any third-party service agreements that are listed and click the **Third-Party Service Agreement** check box.
6.  Click **Provision**. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.  

A series of emails are sent to your administrator: Acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete.

The _provisioning complete_ email includes a link to your *Device Details* page so that you can log in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

## Provisioning through the customer portal
To provision your bare metal server instance through the {{site.data.keyword.slportal}}, complete the following steps:

  1. Log in to the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} by using your unique credentials.
  2. Go to **Order** > **Devices**.
  3. Click **Hourly SAN**, **Hourly local**, **Monthly**, or **Transient** for one of the bare metal offerings.
  4. From **Configure your Cloud Server**, complete all the relevant information.
  5. Click **Add to Order**.
  6. Confirm or edit the domain information for the server.
  7. Select **Cloud Service terms** and the **Third-Party Service Agreement**.
  8. Confirm or enter your payment information and click **Submit Order**. You are redirected to a screen with your provisioning order number. You can print the screen because if you need a provisioning order receipt.

A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page, after logging in to {{site.data.keyword.Bluemix_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

## Next Steps
After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
