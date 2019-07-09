---

copyright:
  years: 2016, 2019
lastupdated: "2019-06-17"

keywords: manage bare metal servers, power off, replicate, reload os, delete server, manage server

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note .note}

# 管理裸机服务器
{: #bm-manage-servers}

您可以取消、停止和重新启动服务器。
{:shortdesc}

## 准备工作
{: #before-you-begin}

* 导航至控制台的设备菜单。有关更多信息，请参阅[导航至设备](/docs/bare-metal?topic=virtual-servers-navigating-devices)。
* 确保您具有任何必要的帐户许可权和设备访问权。只有帐户所有者或具有**管理用户**经典基础架构许可权的用户才能调整许可权。

有关许可权的更多信息，请参阅[经典基础架构许可权](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理设备访问权](/docs/bare-metal?topic=virtual-servers-managing-device-access)。


<!-- ## Replicating a server instance
{: #bm-replicate-server-instance}

You can copy or clone a bare metal server instance to replicate the server configuration and quickly get a new server up and running.
{:shortdesc}

To clone the instance:
 1. Go to the **Device** menu and highlight the device to be copied.
 2. Click **Actions** and select **Configure Replica**. All configurations are copied. No data or content is not copied.
 3. Enter a unique server name.
 4. Specify the domain name. -->

<!-- ## Reloading the operating system
{: #bm-reload-os}

Occasionally, you might want to reload the operating system on your server.
{:shortdesc}

To reload the operating system, follow these steps.
 1. Back up all data before you start. If you don't back up your data, all data that is on the primary disk is lost. But, secondary disk data stays intact.
 2. Go to the **Devices** menu and highlight the device to be reloaded.
 3. Click **Actions** and select **OS Reload**. You can select one of these options:
  * Change the operating system to a different one and start over with new configurations.
  * Keep the existing operating system with the current configurations, but wipe out the server to start over.

During the OS reload, the server is offline and unavailable for use. Reload time varies based on server capacity and operating system. If you defined a provision script, all configurations are restored after the reload completes. Data was backed up before the OS reload can be uploaded the server when the server is available. -->

## 删除服务器实例
{: #bm-delete-server-instance}

如果不再需要裸机服务器实例，也不想再为其支付费用，那么可以随时删除该实例。
{:shortdesc}

1. 转至**设备**菜单，并突出显示要删除的设备。
2. 单击**操作**，然后选择**取消服务器**。

## 关闭服务器的电源
{: #bm-power-off}

可以预先创建服务器以准备使用。创建服务器后，关闭其电源以确保不会发生任何更改，并且任何人都无法对其进行访问。准备就绪后，可以打开服务器电源，服务器将在数分钟后就绪。
{:shortdesc}

1. 转至**设备**菜单，并突出显示要关闭或打开电源的设备。
2. 单击**操作**，然后选择**打开/关闭电源**。

当服务器电源关闭时，仍会对您计费。如果关闭服务器的电源，服务器将保持断电状态，您需要手动打开其电源。
{: note}
