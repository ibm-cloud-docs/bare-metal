---

copyright:
  years: 2017, 2023
lastupdated: "2021-09-20"

keywords: popular servers, fast provisioning

subcollection: bare-metal


---

{{site.data.keyword.attribute-definition-list}}


# Selecting from the most popular servers
{: #bm-select-popular-servers}

The servers in the fast provisioning list are preconfigured to meet the needs of most client use cases, and they are ready to run in 30 - 40 minutes after you order them.
1. Open the [{{site.data.keyword.cloud}} catalog](https://cloud.ibm.com/catalog/){: external}.   
2. Select **Bare Metal Server**.
3. Click **Continue**. If you do not see **Continue**, you might need to log in.
4. In the {{site.data.keyword.baremetal_short}} section, select the following information:

   | Field | Value |
   | ------ | ------ |
   | Quantity | Use the + and - icons to specify the number of identical servers to provision. The default is 1. If you want to provision multiple servers with different specifications, you need to provision them separately. |
   | Billing type | Select **Hourly**, **Monthly**, **1-year term**, or **3-year term**. |
   | Hostname and domain | These fields are populated with default values. You can change them. |
   | Location | Select the region where you want the server to be located. Using the drop-down list, select and data center in the region. |
   | Select your server | Select **Fast provisioning servers** and select the server that meets your needs. These servers are preconfigured and are ready to use in 30 - 40 minutes. |
   | RAM | Default based on the server you selected. |
   | SSH keys | Provide a public key of your SSH key, which you use to log in to your server after it is provisioned. |
   | Image (operating system) | Select the operating system for the server. Your image options might be limited based on the server that you selected. |
   | Add-ons | Expand the Add-ons section to select the appropriate options or use the default values. |
   {: caption="Table 1: Bare metal server selections" caption-side="top"}
    
5. In the Storage Disks section, the Storage Disk is already selected for your fast provisioning servers selection. Expand the Add-ons section if you want to add [IBM Cloud Backup](/docs/Backup?topic=Backup-getting-started) to your server. 
6. In the Network Interface section, select the Uplink Port Speeds. Expand the Add-ons section to select the appropriate options or use the default values. For more information about network options, see [Network options](/docs/bare-metal?topic=bare-metal-network-options).
7. Review your order.
8. If you have a promo code to apply to your order, expand **Apply Promo Code**.  
9. Review any third-party service agreements that are listed and click the **Third-Party Service Agreement** checkbox.
10. Click **Provision**. You are redirected to a screen with your provisioning order number. You can print the screen because it's also your provisioning order receipt.

A series of emails is sent to your administrator: Acknowledgment of the provisioning order, provisioning order approval and processing, and provisioning complete. The _provisioning complete email_ includes a link to your *Device Details* page so that you can log in to {{site.data.keyword.cloud_notm}}. You can also log directly in to the {{site.data.keyword.cloud}} console.

## Next Steps
{: #prov-popular-next}

After your {{site.data.keyword.baremetal_short}} is provisioned, you can start managing it. For more information, see [Managing {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers).
