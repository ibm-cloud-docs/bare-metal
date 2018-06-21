---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-21"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Selecting from the most popular servers
The servers in the Most Popular Servers list are preconfigured to meet the needs of most client use cases, and they are ready to run in 30 - 40 minutes after you order them.
Prerequsites:
  * You must have an upgraded {{site.data.keyword.BluSoftlayer_full}} account.
  * You must be logged into one of the following sites:
    * [The IBM Cloud catalog](https://console.bluemix.net/catalog/)
    * [The SoftLayer control portal](https://control.softlayer.com/)


1. Open the bare-metal order form.    
  <!-- <a href="https://console.bluemix.net/gen1/infrastructure/provision/bm" target="_blank">https://console.bluemix.net/gen1/infrastructure/provision/bm</a> -->

2. Enter the following information:
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
    <td>Use the + and - icons to specify the number of identical servers to provision. <br>If you want to provision multiple servers with different specifications, you need to provision them separately.
    <tr>
    <td>Location</td>
    <td>Select the region and data center where you want the server to be located.</td>
    </tr>
    <tr>
    <tr>
    <td>Hostname and Domain</td>
    <td>These fields are populated with default. You can change them.</td>
    </tr>
    <tr>
    <td>Select your server</td>
    <td>Under **Popular Servers**, select the server that meets your needs. These servers are preconfigured and are ready to use in 30 - 40 minutes.
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
    <td>Select the operating system for the instance. **Note**: an error message is displayed if a conflict exists between the server and operating system. For example, selecting Linux on a Microsoft SQL server.</td>
    </tr>
    <td>Uplink Port Speeds</td>
    <td>Determines the speed of internal and external interfaces.</td>
    </tr>
    <tr>
    <td>Add-ons</td>
    <td> Select the appropriate options or use the default values.</td>
    </tr>
    </TBODY>
    </table>

3.  In the Order Summary section, select **Hourly** or **Monthly** billing.
4.  Review your order.
5.  Review any third-party service agreements that are listed and click the **Third-Party Service Agreement** check box.
6.  Click **Provision**. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

 A series of emails are sent to your administrator: Acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page so that you can log in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.


## Next Steps
After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
