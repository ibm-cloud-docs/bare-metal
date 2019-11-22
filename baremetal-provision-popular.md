---

copyright:
  years: 2017, 2019
lastupdated: "2019-10-23"

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
1. Open the [{{site.data.keyword.cloud_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/catalog/){: new_window}.   
2. Select Bare Metal Server.
3. Click Continue.  If you do not see a Continue button, you may need to log in.
2. In the {{site.data.keyword.baremetal_short}} section, select the following information:

| Field | Value |
|------|------|
| Quantity | Use the + and - icons to specify the number of identical servers to provision. The default is 1. If you want to provision multiple servers with different specifications, you need to provision them separately. |
| Billing type | Select Hourly or Monthly |
| Hostname and Domain | These fields are populated with default values. You can change them. |
| Location | Select the region where you want the server to be located. Using the drop down list, select and data center in the region. |
| Select your server | Select **Popular Servers** and select the server that meets your needs. These servers are preconfigured and are ready to use in 30 - 40 minutes. |
| RAM | Default based on the server you selected. |
| SSH keys | Provide a public key of your SSH key, which you use to log in to your server after it is provisioned. |
| Image (operating system) | Select the operating system for the server. Your Image options may be limited based on the server you selected. |
| Add-ons | Expand the Add-ons section to select the appropriate options or use the default values. |

<caption>Table 1: Bare metal server selections</caption>

3. In the Storage Disks section, the Storage Disk is already selected for your Popular servers selection. Expand the Add-ons section if you want to add IBM Cloud Backup to your server.
4. In the Network Interface section, select the Uplink Port Speeds. Expand the Add-ons section to select the appropriate options or use the default values. For more information about network options, see [Network options](https://test.cloud.ibm.com/docs/bare-metal?topic=bare-metal-network-options).
4.  Review your order.
4. If you have a promo code to apply to your order, expand Apply Promo Code.  
5.  Review any third-party service agreements that are listed and click the **Third-Party Service Agreement** check box.
6.  Click **Provision**. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

 A series of emails are sent to your administrator: Acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete.

 The _provisioning complete email_ includes a link to your *Device Details* page so that you can log in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.slportal}}.


## Next Steps
{: #prov-popular-next}
After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](/docs/vsi?topic=virtual-servers-managing-virtual-servers).
