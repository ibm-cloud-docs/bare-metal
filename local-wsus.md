---
copyright:
  years: 2018, 2024
lastupdated: "2024-09-13"


keywords:

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Updating a server to use a local WSUS server
{: #updating-an-instance-to-use-a-local-wsus-server}

If your server that is running Windows&reg; is provisioned with a cloud-init enabled image, you might want to manually update the Windows registry to use local {{site.data.keyword.BluSoftlayer_full}} Windows Server Update Services (WSUS) servers, rather than the default Microsoft&reg; WSUS servers.
{: shortdesc}

If you order a server with a Windows Server operating system without any add-ons, such as more software, post-provisioning scripts, or monitoring, it is likely that your server is provisioned with a cloud-init image. With cloud-init provisions, the WSUS server defaults to the Microsoft WSUS server.

If you want to update the server to use the {{site.data.keyword.cloud_notm}} local WSUS server, use the following _.reg_ file after you provision the server. Make the following changes before you use this file.

- Change _wsusdal0102_ to the local data center where your server is provisioned.
- The line that includes _"DoNotConnectToWindowsUpdateInternetLocations"_ forces the server to use the WSUS server. You can leave it out if you want to check against Windows Update and WSUS.

```text
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
