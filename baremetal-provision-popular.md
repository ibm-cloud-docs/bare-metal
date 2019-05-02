---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-02"

keywords: provision bare metal, popular servers, {{site.data.keyword.baremetal_short}}, provision

subcollection: bare-metal


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Selecting from the most popular servers
{: #bm-select-popular-servers}

The servers in the Most Popular Servers list are preconfigured to meet the needs of most client use cases, and they are ready to run in 30 - 40 minutes after you order them.
1. Open the [{{site.data.keyword.cloud_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/){: new_window}.   
2. Select Bare Metal Server.
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
    <tr>
    <td>Location</td>
    <td>Select the region where you want the server to be located. Using the drop down list, select and data center in the region. </td>
    </tr>
    <tr>
    <tr>
    <td>Select your server</td>
    <td>Select **Popular Servers** and select the server that meets your needs. These servers are preconfigured and are ready to use in 30 - 40 minutes.
    </tr>
    <tr>
    <td>RAM</td>
    <td>Default based on the server you selected.</td>
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
    <td>Expand the Add-ons section to select the appropriate options or use the default values./td>
    </tr>
    </TBODY>
    </table>
3. In the Storage Disks section, the Storage Disk is already selected for your Popular servers selection. Expand the Add-ons section if you want to add IBM Cloud Backup to your server.
4. In the Network Interface section, select the Uplink Port Speeds. Expand the Add-ons section to select the appropriate options or use the default values.
4.  Review your order.
4. If you have a promo code to apply to your order, expand Apply Promo Code.  
5.  Review any third-party service agreements that are listed and click the **Third-Party Service Agreement** check box.
6.  Click **Provision**. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

 A series of emails are sent to your administrator: Acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete.

 The _provisioning complete email_ includes a link to your *Device Details* page so that you can log in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.


## Next Steps

After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
