---
copyright:
  years: 2018
lastupdated: "2018-05-16"

keywords: WSUS, Microsoft Windows

subcollection: software

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Updating an instance to use a local WSUS server
{: #updating-an-instance-to-use-a-local-wsus-server}

If your virtual server instance that is running Microsoft Windows was provisioned with a cloud-init enabled image, you might want to manually update the Windows registry to use local {{site.data.keyword.BluSoftlayer_full}} Windows Server Update Services (WSUS) servers, rather than the default Microsoft WSUS servers.
{:shortdesc}

If you order a virtual server with a Windows Server operating system without any add-ons, such as more software, post-provisioning scripts, or advanced monitoring, it is likely that your server is provisioned with a cloud-init image. With cloud-init provisions, the WSUS server defaults to the Microsoft WSUS server.

If you want to update the virtual server to use the {{site.data.keyword.cloud_notm}} local WSUS server, use the following .reg file after your server is provisioned. Make the following changes before you use this file.
- Change *wsusdal0102* to the local data center where your virtual server is provisioned.  
- The line that includes *"DoNotConnectToWindowsUpdateInternetLocations"* forces the server to use the WSUS server. You can leave it out if you'd like to be able to check against Windows Update and WSUS.

```
 Windows Registry Editor Version 5.00

    [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate]
    "ElevateNonAdmins"=dword:00000000
    "WUServer"="http://wsusdal0102.service.softlayer.com"
    "WUStatusServer"="http://wsusdal0102.service.softlayer.com"
    "DoNotConnectToWindowsUpdateInternetLocations"=dword:00000001

    [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU]
    "AUOptions"=dword:00000005
    "NoAutoRebootWithLoggedonUsers"=dword:00000001
    "NoAutoUpdate"=dword:00000000
    "RebootReLaunchTimeout"=dword:000000f0
    "RebootReLaunchTimeoutEnabled"=dword:00000001
    "RebootWarningTimeout"=dword:0000000a
    "RebootWarningTimeoutEnabled"=dword:00000001
    "RescheduleWaitTime"=dword:0000000a
    "RescheduleWaitTimeEnabled"=dword:00000001
    "ScheduledInstallDay"=dword:00000000
    "ScheduledInstallTime"=dword:00000002
    "UseWUServer"=dword:00000001
```
{: codeblock}
