---



copyright:
  years: 2017, 2018
lastupdated: "2018-03-06"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Advanced bare metal server provisioning
{: #ordering-baremetal-server}
Use this procedure to customize your {{site.data.keyword.baremetal_short}}.

## Logging in and navigating to the customer portal
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

## Provisioning a bare metal server
Launch the order form and provision your server.
1.	From the {{site.data.keyword.slportal}}, locate the **Order** section and click **Devices**.
* On the catalog page, click **Bare Metal Server**.
* On the **Bare Metal Server** page, click **Create** to launch the order form.
* Below the **Popular Servers** section, click **Interested in other configuration options?** This opens the advanced bare metal provisioning form.

1. Select a data center location for your server.
* There are three categories of servers:
  * SAP Certified servers
  * Single Processor Multi-Core Servers
  * Dual Processor Multi-Core Servers

  Select your server, by clicking on the **Starting Price Per** link.
* Select all of your configuration options. **Data Center**, **RAM**, and **Operating System** are required fields. All other fields are optional.

  **Note**: an error message is displayed if there is a conflict between the server and operating system. For example, selecting Linux on a Microsoft SQL server.
* Click Add to Order. The Checkout page is displayed.

  From the Checkout page, you can return to the configuration page by clicking one of the Reconfigure options.
* In the Advanced System Configuration section, specify additional configuration options. See [Understanding your  {{site.data.keyword.baremetal_short}} options](../bare-metal/configuring.html){:target="_blank"} for more information on these options.

*   Click the **Cloud Service terms** and the **Third-Party Service Agreement** check boxes.
*   Confirm or enter your payment information and click the **Submit Order** button. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

  You can also save this order without purchasing by clicking **Save as Quote**.

 A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page, after logging in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

### Next Steps
After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
