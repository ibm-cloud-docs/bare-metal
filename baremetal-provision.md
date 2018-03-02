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


# Advanced bare metal server provisioning
{: #ordering-baremetal-server}
After you log in, you can provision a {{site.data.keyword.baremetal_short}}.

1.	From the {{site.data.keyword.slportal}}, locate the **Order** section and click **Devices**.
2.	Enter the following information:

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
    <td>Select the data center where you want the server to be located.</td>
    </tr>
    <tr>
    <td>Select your server specifications</td>
    <td>Select one of the more common servers for faster provisioning or click <b>All Servers</b> for more options.</td>
    </tr>
    <tr>
    <td>SSH Keys</td>
    <td>Provide a public key of your SSH key, which enables you to log in to your server after it is provisioned.</td>
    </tr>
    <tr>
    <td>Operating System</td>
    <td>Select the operating system for the instance. **Note**: an error message is displayed if there is a conflict between the server and operating system. For example, selecting Linux on a Microsoft SQL server.</td>
    </tr>
    <tr>
    <td>Attached storage disk</td>
    <td>Indicates the type and size of the storage disks attached to the server you selected.</td>
    </tr>
    <!-- <tr>
    <td>Additional Disks</td>
    <td>You can provision up to four more boot disks, SAN, or Local, per dedicated instance.</td>
    </tr>-->
    <td>Network Interface</td>
    <td> Select the appropriate options or use the default values.</td>
    </tr>
    <tr>
    <td>Add-ons</td>
    <td> Select the appropriate options or use the default values.</td>
    </tr>
    <tr>
    </TBODY>
    </table>


After clicking for additional configuration options from the [bare metal provisioning](../bare-metal/baremetal-provision-popular.html) page, the advanced bare metal ordering form is displayed. Use this procedure to configure and order your server.

1.  Select your **Data Center**, scroll through the  page, and click on the **Starting Price Per** link to select your server.
4.  Fill in the information on the **Configure your {{site.data.keyword.baremetal_short}}** page and click the **Add to Order** button to continue. See [Configuring your {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.html) for more information on how to configure your server. Once your order is verified, you'll be redirected to the **Checkout** page.
5.  Enter the **Advanced System Configuration** for the server. See [Configuring your {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.html) for more information on how to set this up.
6.  Click the **Cloud Service terms** and the **Third-Party Service Agreement** check boxes.
7.  Confirm or enter your payment information and click the **Submit Order** button. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

 A series of emails are sent to your administrator: acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The provisioning complete email includes a link to your *Device Details* page, after logging in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.

### Next Steps
After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
