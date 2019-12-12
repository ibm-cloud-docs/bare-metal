---

copyright:
  years: 2017, 2019
lastupdated: "2019-12-03"

keywords: mount iso bare metal

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Mounting an ISO on a bare metal server
{: #bm-mount-iso}

## Overview
{: #bm-mounting-iso-overview}

Although most {{site.data.keyword.cloud}} customers use one of the standard Operating Systems that come with our servers, you can mount custom ISOs (disk images) on servers. You have three options for mounting custom ISOs.

For the methods to work, you need to connect to the private network through the SL VPN service, such as [IBM Cloud SSL VPN - AMS01](https://vpn.ams01.softlayer.com/prx/000/http/localhost/login) or through another server that is connected to the network.

**Note:** Lenovo hardware disk images larger than 50 MB must be mounted by using the IMM console **interface > media tab**.

## Option 1 (preferred): using IPMI (ISO on a CIFS share)
{: #bm-mount-iso-opt-1}

If your infrastructure is already deployed on {{site.data.keyword.cloud_notm}}, you can configure an existing server to offer a CIFS share to the internal network. You can then mount any ISO on there to a bare metal server.

This option the preferred method for installing a custom OS on a bare metal server. IPMI installs over the local network, which is fast and can keep an ISO mounted even if you log out or get disconnected from the management interface.

Follow these steps to install a Custom OS from a CIFS Share:

1. Make sure that the ISO is on the CIFS Share.
* Log in to the IPMI management console by pointing your web browser to the IP specified in cloud.ibm.com. 
* Go to **Devices** > your server (device details)** > **Remote Mgmt**. **Note:** The username and password are also specified here.
* Hover over the **Virtual Media** and click **CD-ROM image**
* Fill in the appropriate details and click **Save and Mount**.

Not all users have permission to change the BIOS of the server. If necessary, you can open a ticket to support requesting:
  * Root user administrator privileges on IPMI (to be able to change the Virtual Media Attach mode).
  * Change the boot sequence to ‘IPMI Virtual Disk’ as first boot option.
  {: note}
  
### What next

After you make these changes, go back to the IPMI management console and go to configuration -> Remote session and change attach mode to; **attach**. In some older IPMI consoles, you can skip this option.
* Reboot the server and boot from the virtual media.


## Option 2: Using IPMIView (ISO on a CIFS share)
{: #bm-mount-iso-opt-2}

Prerequisites:<br/>
* Have a bootable ISO
* A Windows CIFS Server or NAS Storage to store the Bootable ISO
* The ISO is uploaded to the File Storage (NAS) associated with the server.
* IPMIView is installed or access KVM Console
* ISO File is downloadable using wget
* SSH access with privileges to access / install packages and create a mount


### Linux and Windows
Follow the steps below to mount an ISO with IPMIView.
1. Through a support ticket, request that your server boots their Virtual CD-ROM as the first device. Each device must boot from their associated virtual CD-ROM. You can revert this setting after you install the OS.
* Establish a VPN Connection to [VPN](http://www.softlayer.com/VPN-Access). If you are using Microsoft Internet Explorer, make sure to include .softlayer.com and .cloud.ibm.com in your Trusted Sites list and keep your JAVA up to date.
* Copy ISO Media to NAS or Windows CIFS Server.
  * Connect to your Linux jumpbox using SSH.
  * Mount NAS share on your Linux jumpbox:

        mkdir /mnt/nasmount
        mount -t cifs //NAS_SERVER_NAME_ORIP/SLN#####-2 -o username=SLN#####-2,
        password=NAS_STORAGE_PW,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755 /mnt/nasmount
  * Mount Command parameter key:
        NAS_SERVER_NAME_ORIP = The name or IP of the NAS storage.
        /SLN#####-2 = The username and folder name to connect to your NAS storage.
        NAS_STORAGE_PW = The password to your NAS storage.
        /mnt/nasmount = The Folder to mount the NAS storage.
  * Change Directory to your new NAS mount folder.
        cd /mnt/nasmount
  * Download the iso file using wget.
        wget http://www.linktoyouriso.com/isofilename.iso
  You will see a confirmation that the download was successful.
* Download IPMI View here:
      https://www.servethehome.com/download-supermicro-ipmiview-latest-version/
* Connect to Server over the Management IP.<br>
      1. Connect to the `winadmin`.
      2. Open IPMIView and go to **File > New > System**.
      3. Use the IPMI IP address from the hardware object to complete the Server Name and IP address fields.<br>
      4. Double-click the system with the same IP address on the left side and enter ADMIN for Login ID and the IPMI password from the hardware object.
      5. After you connect, you have many tabs available in the window. You can use **Text Console** or **KVM Console** to connect to the server.

* Open the Virtual Media Tab
* Complete the CD-ROM Image connection details.
  *
    * Share host = The IP Address of the NAS Storage. You can find this value pinging your NAS storage server name. For example, `ping nas501.service.softlayer.com`
    * Share Name = The Username of the NAS storage
    * Path to image = The name of the ISO file, in the following format:
          \NASusername\isoname.iso (i.e. \SLN123456\centos6.iso)
    * User = The user name of the NAS storage
    * Password = The Password for the NAS storage
* Reboot the server
* Open KVM Console view
* Follow system prompts to Boot the BOOTABLE ISO
* Install OS
* Unmount the Virtual Media
* Restart Server

## Option 3: Mounting an ISO from your local computer
{: #bm-mount-iso-opt-3}

<a name="option3"></a>

You can mount an ISO from your local computer by using the Java iKVM viewer (console). This will enable you to mount an ISO while connected to the console. The speed at which the installation progresses may vary depending on the upload speed and latency of your internet connection, performance of java and your computer.

If you do not have permission to change the BIOS on a server, open a ticket to support requesting the following changes:
* Root user administrator privileges on IPMI (to be able to change the Virtual Media Attach mode)
* To change the boot sequence to ‘IPMI Virtual Disk’ as first boot option. (Because ISO is not yet mounted, support should only change the boot device priority for now).


1. Log in to the IPMI management console by pointing your web browser to the IP that is specified in cloud.ibm.com.
* Go to **Devices** > **your server (device details)** > **Remote Mgmt**. Specify the username and password.
* Click **Configuration** > **Remote session** and change attach mode to **attach**. **Note:** In some older IPMI consoles this option is not available so you can skip this step.
* To return to the system information page, go to **System** > **System information** and click the console window icon. Accept all security warnings.
* When the console connects, you see login prompt.
* Click **Virtual Media** > **Virtual Storage**.
* Go to the **CDROM&ISO** tab and select the ISO File under **Logical Drive Type**
* Click **Open Image** and select the ISO on your local computer.
* Click **Plug-in** to insert the ISO into the virtual CD-ROM drive and click **OK**.
* Restart the server and use the **boot from the virtual CD-ROM drive** option. You might need to use the virtual keyboard in the iKVM viewer to select a boot device.

## Troubleshooting
{: #bm-mount-iso-troubleshooting}

* Not all users have default access to mount Virtual Media. If a permission error occurs, contact Support for an update to the Root IPMI User permissions.
* If an ISO is already mounted, an error message will appear with the text **There is a disk mounted**. You must unmount the existing disk and replace it with the new ISO. Two ISOs may not be mounted at the same time.
* You may need to contact support to change the boot order in the BIOS.
* When mounting an ISO please use [SSL VPN](http://vpn.softlayer.com) instead of PPTP VPN.  Once connected to the VPN network you can also access the system's IPMI through the IPMI address (https://private-ip-IPMI-management).
* When you input a path to an ISO, use the UNC Name Syntax (Universal Naming Convention) for the path, for example:
  `\\<NAS username>\<isoname>.iso`
