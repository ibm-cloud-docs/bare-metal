---



copyright:
  years: 2017, 2018
lastupdated: "2018-03-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning an Intel Optane SSD DC P4800X
{: #ordering-ssd}

Intel® Optane™ SSD DC P4800X is a solid state drive that combines the attributes of storage and memory to create a new storage tier.

The Intel® Optane™ SSD DC P4800X 375 GB <!-- and 750 GB --> drives are available in some {{site.data.keyword.cloud}} bare metal servers.

For more information about Intel® Optane™ SSD DC P4800X, see https://www.intel.com/content/www/us/en/solid-state-drives/optane-ssd-dc-p4800x-brief.html.

## Intel Optane Drives and GPUs

You can either order an Intel® Optane™ SSD DC P4800X disk OR a GPU for your server. You cannot order both on the same server.

## Logging in and navigating to the advanced order form
Make sure that you are logged in, either through {{site.data.keyword.cloud_notm}} catalog or {{site.data.keyword.slportal}}:

  <table>
   <CAPTION>Table 1. Choose a log in location</CAPTION>
   <THEAD>
   <TR>
   <th>If you want to order with the...</th>
   <th>Then...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud catalog</td>
   <td>
   <ol>
   <li>Open a new browser window and enter  <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>.</li>
   <li>Click the <b>Log in</b> link. </li>
   <li>Enter your email or IBMid and click <b>Continue.</b></li>
   <li>Enter your Password and click <b>Log in.</b></li>
   <li>Select <b>Infrastructure</b> <b>Compute</b>.</li>
   <li>Click the <b>{{site.data.keyword.baremetal_short}}</b> tile.</li>
   <li>Click <b>Create</b>. The main page of the {{site.data.keyword.slportal}} opens.</li>
   <li>In the Order section, click <b>Devices</b>. The main page of the {{site.data.keyword.slportal}} opens.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Customer Portal</td>
   <td>
   <ol>
   <li>Open a new browser window and enter <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Type your user name and Password, and click <b>Log In</b>. Or, click <b>Log in with IBMid</b>. Then, enter your email or IBMid and click <b>Continue</b>. Enter your password and click <b>Log In</b>. The main page of the {{site.data.keyword.slportal}} opens.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Provisioning an Intel Optane-compatible bare metal server
Launch the order form and provision your server.
1.	From the {{site.data.keyword.slportal}}, locate the **Order** section and click **Devices**.
* On the catalog page, click **Bare Metal Server**.
* On the **Bare Metal Server** page, click **Create** to launch the order form.
* Below the **Popular Servers** section, click **Interested in other configuration options?** This opens the advanced bare metal provisioning form.
*  Select your **Data Center**. To use the Intel Optane drive, select one of the following data centers:
  * AMS03 - Amsterdam
  * DAL09 - Dallas
  * DAL10 - Dallas
  * DAL12 - Dallas
  * FRA02 - Frankfurt
  * LON02 - London
  * MEL01 - Melbourne
  * MON01 - Montreal
  * OSL01 - Oslo
  * SJC03 - San Jose
  * TOR01 - Toronto
  * WDC04 - Washington, DC
* Select your **server**, by clicking on the **Starting Price Per** link. The following servers are compatible with the Intel Optane drive:

  * Intel Xeon 4110  with up to 12 drives
  * Intel Xeon 5120  with up to 12 drives
  * Intel Xeon 6140  with up to 12 drives
  * Intel Xeon E5-2620 v4 with GPU Support
  * Intel Xeon E5-2650 v4 with GPU Support
  * Intel Xeon E5-2690 v4 with GPU Support

  **Note**: If you select E5-2620 v4, E5-2650 v4, or E5-2650 v4, the Intel Optane drive will replace your GPU, so you cannot have both a GPU and an Intel Optane drive.

* Select your requirements for **Server Security** and **RAM**.
* For the **First PCIe Component** and **Second PCIe Component**, you can select an Intel Optane drive.
* Select the **Operating System**.

  <!-- For Intel-provided Optane drivers the following operating systems are guaranteed:
  * Windows Server 2016 (all Editions)
  * Windows Server 2012 R2 (all Editions)

  For In-box, open-source, non-Intel drivers, compatibility and functionality is validated but not guaranteed:
  * Red Hat Enterprise Linux 7.x (64 bit)
  * Red Hat Enterprise Linux 6.x (64 bit) -->

* Specify the remaining items on the order form based on your needs.
* Click the **Add to Order** button to continue. See [Configuring your {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.html) for more information on how to configure your server. Once your order is verified, you'll be redirected to the **Checkout** page.
* Enter the **Advanced System Configuration** for the server. See [Configuring your {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.html) for more information on how to set this up.
* Click the **Cloud Service terms** and the **Third-Party Service Agreement** check boxes.
* Confirm or enter your payment information and click the **Submit Order** button. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

 A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page, after logging in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

## Next Steps
After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
