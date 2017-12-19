---



copyright:
  years: 2017
lastupdated: "2017-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning bare metal server

## Before you begin
You have two options to provision your public {{site.data.keyword.baremetal_long}}. The first is through the {{site.data.keyword.cloud}} catalog and the second is through the {{site.data.keyword.slportal_full}}. The catalog and {{site.data.keyword.slportal}} require unique log-in IDs. Your catalog user name and password won’t work for logging in to the portal and vice versa.
{:shortdesc}

Before you begin, ensure that you have either your {{site.data.keyword.cloud_notm}} catalog or {{site.data.keyword.slportal}} credentials set-up. 
  
     **Note:** For the {{site.data.keyword.cloud_notm}} catalog, you must have an upgraded account to order {{site.data.keyword.baremetal_short}}. For more information about upgrading your account, see [Switching to IBMid](https://console.ng.bluemix.net/docs/admin/softlayerlink.html).
  
## Logging in 
Make sure that you are logged in, either through {{site.data.keyword.cloud_notm}} catalog or {{site.data.keyword.slportal}}: 

  <table>
   <CAPTION>Table 1. Choose a log in location</CAPTION>
   <THEAD>
   <TR>
   <th>If you want to log in with...</th>
   <th>Then...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud Catalog</td>
   <td>
   <ol>
   <li>Open a new browser window and enter  <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>.</li>
   <li>Click the <b>Log in</b> link. </li>
   <li>Enter your email or IBMid and click <b>Continue.</b></li>
   <li>Enter your Password and click <b>Log in.</b></li>
   <li>Select <b>Infrastructure</b> > <b>Compute</b>.</li>
   <li>Click the <b>{{site.data.keyword.baremetal_short}}</b> tile.</li>
   <li>Click <b>Create</b>. The main page of the {{site.data.keyword.slportal}} opens.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Customer Portal</td>
   <td>
   <ol>
   <li>Open a new browser window and enter <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Enter your User name and Password, and click <b>Log In</b>. Or, click <b>Log in with IBMid</b>. Then, enter your email or IBMid and click <b>Continue</b>. Enter your password and click <b>Log In</b>. The main page of the {{site.data.keyword.slportal}} opens.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Provisioning a bare metal server
{: #ordering-baremetal-server}
After you have logged in,  you can begin to provision a {{site.data.keyword.baremetal_short}}. You can provision your {{site.data.keyword.baremetal_short}} through the **Devices** menu or the **Devices** icon.

### Provisioning a bare metal server through the devices icon
To provision your {{site.data.keyword.baremetal_short}} through the *Devices* icon, complete the following steps:

1.  From the {{site.data.keyword.slportal}}, locate the **Order** section and click **Devices**.
2.  On the Devices page, click **Hourly** or **Monthly** under {{site.data.keyword.baremetal_short}}.
3.  Select your **Data Center**, scroll through the  page, and click on the **Starting Price Per** link to select your server. 
4.  Fill in the information on the **Configure your {{site.data.keyword.baremetal_short}}** page and click the **Add to Order** button to continue. See [Configuring your {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) for more information on how to configure your server. Once your order is verified, you'll be redirected to the **Checkout** page.
5.  Enter the **Advanced System Configuration** for the server. See [Configuring your {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) for more information on how to set this up.
6.  Click the **Cloud Service terms** and the **Third-Party Service Agreement** check boxes.
7.  Confirm or enter your payment information and click the **Submit Order** button. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

 A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page, after logging in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

### Provisioning bare metal server through the Devices menu
{: #ordering-baremetal-devices-menu}

You can also provision your {{site.data.keyword.baremetal_short}} through the *Devices* menu on the main {{site.data.keyword.slportal}} page. 

1. Click **Devices > Device List**. The Devices page displays all device types—dedicated hosts, virtual servers, bare metal servers, and NetScaler application delivery controllers—within your account.
2. Click the **Order Devices** link in the upper right-hand corner.
3. On the Order SoftLayer Products and Services page, click **Hourly** or **Monthly** under {{site.data.keyword.baremetal_short}}.
4. Select your **Data Center**, scroll through the page, and click on the **Starting Price Per** link to select your server. 
5.  Fill in the information on the **Configure your {{site.data.keyword.baremetal_short}}** page and click the **Add to Order** button to continue. See [Configuring your {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) for more information on how to configure your server. Once your order is verified, you'll be redirected to the **Checkout** page.
6.  Enter the **Advanced System Configuration** for the server. See [Configuring your {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) for more information on how to set this up.
7. Click the **Cloud Service terms** and the **Third-Party Service Agreement** check boxes.
8. Confirm or enter your payment information and click the **Submit Order** button. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page, after logging in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

### Next Steps
After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](../bare-metal/vsi_managing.html).
