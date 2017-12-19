---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Installing Ubuntu server on a bare metal server

If you want to use an operating system that is not provided by {{site.data.keyword.IBM&reg; Cloud}}, you can install them onto bare metal servers by mounting custom ISOs (disk images). To mount an ISO upload, it to the File Storage (NAS) associated with the server. To upload an ISO to NAS, use the following procedures to mount an ISO with IPMI.
1. Order the Bare Metal Server with **No Operating System** 
* You can also select the free OS (e.g. CentOS) as operating system which can be used to connect to the NAS.
* Order the NAS storage to store the Bootable ISO. If you already have any Windows CIFS server, you can use it to share the ISO image. With this Windows CIFS server, you will get the legacy NAS with 20GB capacity. After provisioning the NAS, you can see the description of your NAS from the customer portal.
* Download the ISO image from https://www.ubuntu.com/download/server.
* Upload ISO image to NAS or Windows CIFS Server. If you have the NAS storage, you can upload the ISO image file by using FTP.

  Sample FTP procedure:
  ```#ftp <nas address>.service.softlayer.com
  Connected to <nas address>.service.softlayer.com
  220 NAS FTP Service
  User (<nas address>.service.softlayer.com:(none)): <nas username>
  331 Please specify the password.
  Password: <nas password>
  230 Login successful.
  ftp> bin
  200 Switching to Binary mode
  ftp> put <iso imagefile name>.iso
  200 PORT command successful. Consider using PASV.
  150 Ok to send data.
  226 Transfer complete.
  ftp: 3170893824 bytes sent in 253.86 Seconds 12490.77Kbytes/sec.```
  
* Establish a VPN Connection to {{site.data.keyword.Bluemix_notm}} with the IPMI. You can launch the VPN menu from the Support menu or following URL: [VPN Access](http://www.softlayer.com/VPN-Access)
* Mount the ISO image from IPMI Virtual Media Menu by using the Connect to IPMI over the Management IP.
  1. View IPMI Credentials
  * Log IPMI View
  * Open the Virtual Media Tab
  * You need root user with Administrator privileges on IPMI. If priveleges show as *Operator*, open a support ticket to change the privileges to Administrator.
  * Fill in the ISO image connection details
    Share host = The IP address of the NAS<br/Example: 10.3.x.x
    Path to image = The name of the ISO file, formatted like this: \NASusername\imagefilesname.iso (i.e. \SLNxxxxxx\SLE-12-SP1-Server-DVD-x86_64-GM-DVD1.iso)
    User = The username of the NAS
    Password = The password for the NAS
  * Click **Mount** button
  * Confirm the device
* Click and launch the KVM Viewer, and open the Virtual Storage page from the Virtual Media menu. If you are successful in mounting your ISO image as CDROM device, you will see the device description in the **Connection Status History**.
* Request that your server boots their Virtual CD-ROM as the first device via SoftLayer ticket. Complete this request for each server. You change the boot setting after OS is installed. 
  **Note**:You may not need to contact support to change the boot order in the BIOS. It depends on your server. Please try to reboot once for confirming the boot order.
* Reboot the server from KVM view.
* Install OS from the mounted ISO image.
* Install the Ubuntu OS to the bare metal server from ISO.
* Configure the network settings (IP address/subnet/gateway/DNS etc). If you don't configure it correctly during the installation step, you can only connect to this server via KVM console after reboot.

* Unmount the Virtual media. You should unmount the virtual media from the server via IPMI Virtual Media tab.
* Reboot the server.
* After reboot, you can access the server via SSH.
