---

copyright:
  years: 2014, 2026
lastupdated: "2026-10-02"

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Enabling drive security by using Avago SafeStore Encryption Services
{: #enabling-drive-security-by-using-avago-safestore-encryption-services}

Setting up drive security helps prevent access to stored data on removed disks without a security key. The drive data can't be recovered without this key. {{site.data.keyword.cloud}} provides self-encrypting drives at select data centers for the drives that can be bought on a bare metal server. 10 TB SATA drives are available in our US data centers.
{: shortdesc}

## Prerequisites
{: #prerequisites-enabling-drive-security-by-using-avago-safestore-encryption-services}

* Bare metal server with self-encrypting drives – 10 TB SATA
* AVAGO MegaRAID SAS 9361 -8i or Similar AVAGO RAID cards
* Installed Mega RAID Storage Manager Software

## Enabling drive security by using MegaRAID Storage Manager (MSM)
{: #enabling-drive-security-by-using-megaraid-storage-manager-msm-}

Use can set the security key and safe guard data in a removed disk by using the MegaRAID Storage Manager. You can also use the WebBIOS interface that requires a security key at server start time to enter the MegaRAID card BIOS to configure the drive security setting.

For more information, see [SafeStore Disk Encryption](https://techdocs.broadcom.com/us/en/storage-and-ethernet-connectivity/enterprise-storage-solutions/megaraid8-tri-mode-software/1-0/v11668478.html){: external}.

### Identifying preinstalled self-encrypting drives
{: #identifying-preinstalled-sed-drives}

MegaRAID Storage Manager comes preinstalled on most supported operating systems. If they are not present, you can manually install it from the Broadcom site.

You can open MegaRAID Storage Manager by using the system credentials. In the example, a Windows environment is used to and MSM is preinstalled.

When you start MSM, you must enter your **username** and password that is the privileged user (administrator) and password.

Click the **Physical** tab and click the drives that are available on the system. The **Properties** page has the **Drive security properties** section that includes the **Full disk encryption capable** field, which shows **Yes**. In the example used, two non-self-encrypting drives and four self-encrypting drives are used.

### Enabling drive security on the controller
{: #enabling-drive-security-at-the-controller}

1. To enable drive security, right-click the `Controller 0 :AVAGO MegaRAID SAS 9361-8i` from the **Physical** tab and select **Enable drive security**.
   - You can now enter the **Security key identifier** and the **Security key**. If you have multiple security keys, a security key identifier can help you identify which security key that you need to use. You must record the security key in a safe location. The security key is required when you reconfigure drives such as removing or reinserting a drive. Without the security key, it is not possible to retrieve any data that is stored in a volume that is created out of the self-encrypting drives. It is not possible to retrieve a forgotten security key. A start time password can also be set, which holds the system pause for a password set here to be entered. The start time password is optional and if it is set you must log in into IPMI and type the start password whenever the system is restarted. Scroll down and check the box that says **I recorded the security settings for future reference** and click **Yes** to enable drive security.
   - When drive security is enabled, a yellow key image appears for **Controller 0 AVAGO MegaRAID SAS 9361-8i**.

1. Now create a secure volume by using the self-encrypting drives. Right-click **Controller0** from the **Logical** tab and select **Create Virtual Drive**.
1. Choose the **Advanced** option. The screen needs to specify the **RAID level** and the **Drive security method** as **full disk encryption (FDE)**.
1. Select the FDE Drives that are required and click **Add** > **Create a drive group** > **Next**.
1. Review the virtual drive settings and make any necessary changes.
   - The suggested setting for the **Read policy** is **always read ahead**.
   - The suggested setting for the **Write policy** is **Write-back**.

1. Click **Create a virtual drive**.
1. Accept the write-back policy impact due to BBU by clicking **Yes**. Then, click **Next** and review the summary screen.
1. Click **Finish**.
1. To confirm that the virtual disk is secured, click the **Logical** tab and the virtual drive that was created. You see in the **Drive security properties** that the **Secured** field is marked **Yes**.

### Securing RAID volumes
{: #secure-raid-volumes}

If the server came with RAID volumes that were already created by using self-encrypting drives drives, you can make the volume secure by completing the following step.

1. In the **Logical** tab, right-click **Drive group** and select **Secure with FDE**.

   If you mixed FDE and Non-FDE drives for a volume, then this option is not visible.
   {: note}

You can also set up drive security by using webBIOS and logging in through the IPMI at the start time and entering the RAID BIOS.

### Removing drive security
{: #remove-drive-security}

1. To remove drive security, you must first delete secured virtual disks and right-click **Controller 0** to **Disable Drive Security**. This function securely erases the data in it and removes drive security.
