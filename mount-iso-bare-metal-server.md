---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-02"

keywords: mount iso bare metal server, mount iso, iso on server, iso

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

Although most {{site.data.keyword.Bluemix_notm}} customers use one of the standard Operating Systems that come with our servers, you can mount custom ISOs (disk images) on servers. There are three options for mounting custom ISOs.

For the methods to work you will need to be connected to the private network through the SL VPN service, such as [SoftLayer SSL VPN Portal - AMS01](https://vpn.ams01.softlayer.com/prx/000/http/localhost/login) or through another server you already have connected to the network.

**Note:** Lenovo hardware disk images larger than 50 MB must be mounted using the IMM console interface > media tab.

## Option 1 (preferred): using IPMI (ISO on a CIFS share)
{: #bm-mount-iso-opt-1}

If you already have infrastructure deployed on {{site.data.keyword.Bluemix_notm}}, you can configure an existing server to offer a CIFS share to the internal network. You can then mount any ISO on there to a bare metal server.

This is the preferred method for installing a custom OS on a bare metal server because it installs over the local network, which is very fast and can keep an ISO mounted even if you log out or get disconnected from the management interface.

Follow these steps to install a Custom OS from a CIFS Share:

1. Make sure you have placed the ISO on the CIFS Share.
* Login to the IPMI management console by pointing your webbrowser to the IP specified in control.softlayer.com and under devices -> your server (device details) -> Remote Mgmt. The username and password are also specified here.
* Hover over the **Virtual Media** and click **CD-ROM image**
* Fill in the appropriate details, click **Save and Mount**.
* Not all users have permission to change the BIOS of the server. If necessary you can open a ticket to support requesting:
  * root user administrator privileges on IPMI (to be able to change the Virtual Media Attach mode)
  * Change the boot sequence to ‘IPMI Virtual Disk’ as first boot option.
* After these changes have been made, go back to the IPMI management console and go to configuration -> Remote session and change attach mode to; **attach**. In some older IPMI consoles, you can skip this option.
* Reboot the server and boot from the virtual media.


## Option 2: Using IPMIView (ISO on a CIFS share)
{: #bm-mount-iso-opt-2}

Prerequisites:<br/>
* You have a bootable ISO
* A Windows CIFS Server or NAS Storage to store the Bootable ISO
* The ISO is uploaded to the File Storage (NAS) associated with the server.
* IPMIView is installed or access KVM Console
* ISO File is downloadable using wget
* You have SSH access with privileges to access / install packages and create a mount


### Linux and Windows
Follow the steps below to mount an ISO with IPMIView.
1. Through a support ticket, request that your server boots their Virtual CD-ROM as the first device. Each device must boot from their associated virtual CD-ROM. You can revert this setting after you install the OS.
* Establish a VPN Connection to [VPN](http://www.softlayer.com/VPN-Access). If you are using Microsoft Internet Explorer, make sure to include .softlayer.com in your Trusted Sites list and keep your JAVA up to date.
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
      http://knowledgelayer.softlayer.com/procedure/download-ipmiview
* Connect to Server over the Management IP.
      http://knowledgelayer.softlayer.com/procedure/log-ipmiview
      http://knowledgelayer.softlayer.com/procedure/view-ipmi-credentials
* Open the Virtual Media Tab
* Complete the CD-ROM Image connection details.
  *
    * Share host = The IP Address of the NAS Storage. You can find this value pinging your NAS storage server name. For example, ```ping nas501.service.softlayer.com```
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


1. Login to the IPMI management console by pointing your webbrowser to the IP specified in control.softlayer.com.
* Click Devices > your server (device details) > Remote Mgmt. Specify the username and password.
* Click Configuration > Remote session and change attach mode to **attach**. In some older IPMI consoles this option is not available so you can skip this step.
* Click System > System information to return to the system information page.You will see a console window icon.
* Click the console icon to open the console. Accept all security warnings.
* When the console is connected you will see login prompt.
* Click Virtual Media > Virtual Storage
* Go to the **CDROM&ISO** tab and select the ISO File under **Logical Drive Type**
* Click **Open Image** and select the ISO on your local computer
* Click **Plug in** to insert the ISO into the virtual cd-rom drive.
* Click **OK**.
* Reboot the server and use the **boot from the virtual cd-rom drive** option. You may need to use the virtual keyboard in the iKVM viewer to select a boot device.

## Troubleshooting
{: #bm-mount-iso-troubleshooting}

* Not all users have default access to mount Virtual Media. If a permission error occurs, contact Support for an update to the Root IPMI User permissions.
* If an ISO is already mounted, an error message will appear with the text **There is a disk mounted**. You must unmount the existing disk and replace it with the new ISO. Two ISOs may not be mounted at the same time.
* You may need to contact support to change the boot order in the BIOS.
* When mounting an ISO please use SSL VPN (http://vpn.softlayer.com) instead of PPTP VPN.  Once connected to the VPN network you can also access the system's IPMI through the IPMI address (https://<private-ip-IPMI-management>).
* When you input a path to an ISO, use the UNC Name Syntax (Universal Naming Convention) for the path, for example:
  ```\\<NAS username>\<isoname>.iso```
