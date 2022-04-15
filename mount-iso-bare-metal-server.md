---

copyright:
  years: 2017, 2022
lastupdated: "2022-03-09"

keywords: 

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}


# Mounting an ISO on a bare metal server
{: #bm-mount-iso}

Although most {{site.data.keyword.cloud}} customers use one of the standard operating systems that come with our servers, you can mount custom ISOs (disk images) on servers. You have two options for mounting custom ISOs.
{: shortdesc}

## Overview
{: #bm-mounting-iso-overview}

For the two mounting methods to work, you need to connect to the private network through the SL VPN service, such as `IBM Cloud SSL VPN - AMS01` or through another server that is connected to the network.

Lenovo hardware disk images larger than 50 MB must be mounted by using the IMM console and clicking **Interface > Media tab**.
{: note}

## Option 1 (preferred): using IPMI (ISO on a CIFS share)
{: #bm-mount-iso-opt-1}

If your infrastructure is already deployed on {{site.data.keyword.cloud_notm}}, you can configure an existing server to offer a CIFS share to the internal network. You can then mount any ISO on the internal network to a bare metal server.

This option is the preferred method for installing a custom OS on a bare metal server. IPMI installs over the local network, which is fast and can keep an ISO mounted even if you log out or get disconnected from the management interface.

Follow these steps to install a custom OS from a CIFS Share:

1. Make sure that the ISO is on the CIFS Share.
1. Log in to the IPMI management console by pointing your web browser to the IP specified in cloud.ibm.com. 
1. From the {{site.data.keyword.cloud_notm}} console, go to **Devices** > **Your server (device details)** > **Remote Mgmt**. The username and password are also specified in the details.
1. Hover over **Virtual Media** and click **CD-ROM image**
1. Complete the appropriate details and click **Save and Mount**.

Not all users have permission to change the BIOS of the server. If necessary, you can open a support case and request the following items:

* Root user administrator privileges on IPMI (to be able to change the Virtual Media Attach mode).
* Change the boot sequence to ‘IPMI Virtual Disk’ as first boot option.
  
### What next
{: #bm-what-next-mount-iso}

After you make these changes, go back to the **IPMI management console** and go to **Configuration > Remote session**. Change the attach mode to **Attach**. Then, restart the server and boot from the virtual media.

In some older IPMI consoles, you can skip this option. 
{: note}

## Option 2: Mounting an ISO from your local computer
{: #bm-mount-iso-opt-3}

You can mount an ISO from your local computer by using the Java&reg; iKVM viewer (console). By using the Java iKVM viewer, you can mount an ISO while it is connected to the console. The speed at which the installation progresses can vary depending on the upload speed and latency of your internet connection, performance of Java and your computer.

If you do not have permission to change the BIOS on a server, open a support case to request the following changes:

* Root user administrator privileges on IPMI (to be able to change the Virtual Media Attach mode)
* To change the boot sequence to ‘IPMI Virtual Disk’ as first boot option. (Because ISO is not mounted, support can change only the boot device priority for now).

1. Log in to the IPMI management console by pointing your web browser to the IP that is specified in cloud.ibm.com.
1. Go to **Devices** > **your server (device details)** > **Remote Mgmt**. Specify the username and password.
1. Click **Configuration** > **Remote session** and change attach mode to **attach**. 
   In some older IPMI consoles this option is not available so you can skip this step.
   {: note}

1. To return to the system information page, go to **System** > **System information** and click the console window icon. Accept all security warnings.
1. When the console connects, you see login prompt.
1. Click **Virtual Media** > **Virtual Storage**.
1. Go to the **CDROM&ISO** tab and select the ISO File under **Logical Drive Type**
1. Click **Open image** and select the ISO on your local computer.
1. Click **Plug-in** to insert the ISO into the virtual CD-ROM drive and click **OK**.
1. Restart the server and use the **boot from the virtual CD-ROM drive** option. You might need to use the virtual keyboard in the iKVM viewer to select a boot device.

## Troubleshooting
{: #bm-mount-iso-troubleshooting}

* Not all users have default access to mount Virtual Media. If a permission error occurs, contact [Support](/docs/bare-metal?topic=bare-metal-gettinghelp) for an update to the Root IPMI User permissions.
* If an ISO is already mounted, an error message appears with the text **A disk is mounted**. You must unmount the existing disk and replace it with the new ISO. Two ISOs cannot be mounted at the same time.
* You might need to contact support to change the boot order in the BIOS.
