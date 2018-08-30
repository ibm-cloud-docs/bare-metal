---



copyright:
  years: 2014, 2018
lastupdated: "2018-02-01"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# 重新激活备用池中的设备 
{: #reactivating-spare-pools}

将设备添加到备用池后，“设备列表”中该设备的状态将从“活动”（指示设备有资格用于标准交互）更改为“备用池”。属于备用池的设备专用于该功能，而不能像其他设备一样用于传统日常操作。要从备用池中除去设备，使其可以恢复为传统功能，必须对其重新激活。要重新激活设备，请完成以下步骤。
{:shortdesc}

## 重新激活备用池中的设备 

1. 使用您的唯一凭证来访问 [{{site.data.keyword.slportal_full}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com/){: new_window}。
2. 从导航栏中选择**设备 > 备用池**以访问*备用池*屏幕。
3. 对于所需设备，选择**操作 > 重新激活设备**。
4. 单击**是**以重新激活该服务器。单击**否**以取消该操作。

## 后续步骤
启动重新激活过程后，设备将变为脱机状态，固件会更新，然后该设备可供常规使用。重新激活过程大约需要一小时。从备用池中除去的设备不再有资格用作故障转移方法。通过再次将设备添加到备用池，可随时使设备返回到备用池。有关更多信息，请参阅[向备用池添加设备](../vsi/adding_spare_pool.html)。
