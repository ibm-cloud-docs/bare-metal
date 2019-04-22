---
copyright:
  years: 2014, 2018
lastupdated: "2019-04-22"

subcollection: bare-metal

keywords: Avago SafeStore, encryption
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Enabling drive security by using Avago SafeStore Encryption Services
{: #enabling-drive-security-by-using-avago-safestore-encryption-services}

Setting up drive security helps prevent access to stored data on removed disks without a security key. The drive data can't be recovered without this key. {{site.data.keyword.BluSoftlayer_full}} provides Self-Encrypting Drives (SED) at select data centers for the drives that can be bought on a Bare metal server. 10 TB SATA drives are available in our US data centers.

## Prerequisites
{: #prerequisites-enabling-drive-security-by-using-avago-safestore-encryption-services}

* Bare metal server with SED Drives – 10 TB SATA
* LSI/AVAGO MegaRAID SAS 9361 -8i or Similar LSI/AVAGO RAID cards
* Installed Mega RAID Storage Manager Software

## Enabling drive security by using MegaRAID Storage Manager (MSM)
{: #enabling-drive-security-by-using-megaraid-storage-manager-msm-}

Use can set the security key and safe guard data in a removed disk by using the MegaRAID Storage Manager. You can also use the WebBIOS interface that requires a security key at server start time to enter the MegaRAID card BIOS to configure the drive security setting. For more information about MegaRAID Controller Card SAS 9361-8i, see the Broadcom site, [MegaRAID SAS 9361-8i ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#documentation).

### Identifying preinstalled SED drives
{: #identifying-preinstalled-sed-drives}

MegaRAID Storage Manager comes preinstalled on most supported operating systems. If they are not present, you can manually install it from theBroadcom site. For more information, see [MegaRAID SAS 9361-8i downloads](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#downloads).

You can open MegaRAID Storage Manager by using the system credentials. In the example, a Windows environment is used and MSM is preinstalled.

When you start MSM, you must enter **User name** and **Password** which is the privileged user (Administrator) and password.

Click the **Physical** tab and click the drives that are available on the system. The **Properties** pane has the
**Drive Security Properties** section that includes **Full Disk Encryption capable** field, which shows **Yes**. In the example used, two non-SED disks and four SED disks are used.

### Enabling drive security on the controller
{: #enabling-drive-security-at-the-controller}

1. To enable Drive security, right-click the **Controller 0 :AVAGO MegaRAID SAS 9361-8i** from the **Physical** tab and select
**Enable Drive Security**.
  * You can now enter the **Security key identifier** and the **Security key**. If you have multiple security keys, a security key identifier can help you identify which security key that you need to use. You must record the security key in a safe location. The security key is required when you reconfigure drives such as removing or reinserting a drive. Without the security key, it is not possible to retrieve any data that is stored in a volume that is created out of the SEDs. It is not possible to retrieve a forgotten security key. A start time password can also be set, which holds the system pause for a password set here to be entered. The start time password is optional and if it is set you must log in into IPMI and type the start password whenever the system is rebooted. Scroll down and check the box that says **I recorded the security settings for future reference** and click **Yes** to enable drive security.
  * When drive security is enabled, a yellow key image appears for **Controller 0 AVAGO MegaRAID SAS 9361-8i**.
2. Now create a secure volume by using the SEDs. Right-click **Controller0** from the **Logical** tab and select  
**Create Virtual Drive**.
3. Choose the **Advanced** option. The screen needs to specify the **RAID level** and the **Drive security method** as
**Full Disk encryption (FDE)**. Select the FDE Drives that are required and click **Add** > **Create Drive Group** > **Next**.
4. Review the virtual drive settings and make any necessary changes. The suggested setting for the **Read Policy** is **Always Read Ahead**. The suggested setting for the **Write policy** is **Write Back**. Click **Create Virtual Drive**. Accept the Write Back policy impact due to BBU by clicking **Yes**. Click **Next** and review the summary screen. Click **Finish**.
5. To confirm that the virtual disk is secured, click the **Logical** tab and the virtual drive that was created. You see in the **Drive Security Properties** that the **Secured** field is marked **Yes**.

If the server came with RAID volumes that are already created by using SED drives, you can make the volume secure by following these steps.

In the **Logical** tab, right-click **Drive Group** and select **Secure Using FDE**. If you mixed FDE and Non-FDE
drives for a volume, then this option is not visible.

To remove drive security, you must first delete secured virtual disks and right-click on Controller 0 to **Disable Drive Security**. This function securely erases the data in it and removes drive security.

You can also set up drive security by using webBIOS and logging in through the IPMI at the start time and entering the RAID BIOS. For more information, see **Avago SafeStore Encryption Services** in the **12 Gb/s MegaRAID SAS Software User Guide**.
