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

# Provisioning bare metal servers

## Before you begin

Before you provision a server, review the options and considerations described in [Understanding your bare metal configuration options](../bare-metal/configuring.html)

After reviewing your options, choose one of two ways to provision your your public {{site.data.keyword.baremetal_long}}. One option is through the {{site.data.keyword.cloud}} catalog and the second is through the {{site.data.keyword.slportal_full}}. The catalog and {{site.data.keyword.slportal}} use different log-in IDs, so be sure have you have log in credentials for either the {{site.data.keyword.cloud_notm}} catalog or {{site.data.keyword.slportal}}.
{:shortdesc}

**Note:** For the {{site.data.keyword.cloud_notm}} catalog, you must have an upgraded account to order {{site.data.keyword.baremetal_short}}. For more information about upgrading your account, see [Switching to IBMid](https://console.ng.bluemix.net/docs/admin/softlayerlink.html).

## Logging in and navigating to the provisioning page
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
{: #ordering-baremetal-server}
After you log in, you can provision a {{site.data.keyword.baremetal_short}}.

1.	From the {{site.data.keyword.slportal}}, locate the **Order** section and click **Devices**.
2. On the catalog page, click **Bare Metal Server**.
3. On the **Bare Metal Server** page, click **Create** to launch the order form.
4.	Enter the following information:

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
    <td>Select your server</td>
    <td>Under **Popular Servers**, you see a list of the most commonly ordered servers. If you select one of these options, the provisioning time is faster.

    <br><br>If the servers in the **Popular Servers** list do not meet your needs, click the link that is labeled **Interested in other configuration options?** to open the advanced ordering form. You can find instructions for using the advanced order form [here](../bare-metal/baremetal-provision.html).</td>
    </tr>
    <tr>
    <td>RAM</td>
    <td>Default based on the server you selected.</td>
    </tr>
    <tr>
    <td>SSH Keys</td>
    <td>Provide a public key of your SSH key, which enables you to log in to your server after it is provisioned.</td>
    </tr>
    <tr>
    <td>Operating System</td>
    <td>Select the operating system for the instance. **Note**: an error message is displayed if there is a conflict between the server and operating system. For example, selecting Linux on a Microsoft SQL server.</td>
    </tr>
    <!-- <tr>
    <td>Attached storage disk</td>
    <td>Select the type and size of your attached storage disks.</td>
    </tr> -->
    <!-- <tr>
    <td>Additional Disks</td>
    <td>You can provision up to four more boot disks, SAN, or Local, per dedicated instance.</td>
    </tr>-->
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
5. Review any third-party service agreements listed and click <!-- the **Cloud Service terms** and --> the **Third-Party Service Agreement** check box.
5.  Click **Provision**. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

 A series of emails are sent to your administrator: Acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page so that you can log in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.


### Next Steps
After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
