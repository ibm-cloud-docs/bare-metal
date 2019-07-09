---
copyright:
  years: 2014, 2018
lastupdated: "2019-04-22"

subcollection: bare-metal

keywords: Avago SafeStore, encryption
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 使用 Avago SafeStore Encryption Services 启用驱动器安全性
{: #enabling-drive-security-by-using-avago-safestore-encryption-services}

设置驱动器安全性有助于防止在没有安全密钥的情况下访问已除去磁盘上的存储数据。没有此密钥，无法恢复驱动器数据。{{site.data.keyword.BluSoftlayer_full}} 在精选的数据中心内，为可在裸机服务器上购买的驱动器提供自加密驱动器 (SED)。我们的美国数据中心内提供了 10 TB 的 SATA 驱动器。

## 先决条件
{: #prerequisites-enabling-drive-security-by-using-avago-safestore-encryption-services}

* 具有 SED 驱动器的裸机服务器 - 10 TB SATA
* LSI/AVAGO MegaRAID SAS 9361 -8i 或类似 LSI/AVAGO RAID 卡
* 已安装的 Mega RAID Storage Manager 软件

## 使用 MegaRAID Storage Manager (MSM) 启用驱动器安全性
{: #enabling-drive-security-by-using-megaraid-storage-manager-msm-}

使用 MegaRAID Storage Manager，用户可以在除去的磁盘中设置安全密钥并保护数据。您还可以在服务器启动时使用需要安全密钥的 WebBIOS 界面来进入 MegaRAID 卡 BIOS，以配置驱动器安全设置。有关 MegaRAID Controller Card SAS 9361-8i 的更多信息，请参阅 Broadcom 站点 [MegaRAID SAS 9361-8i ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#documentation)。

### 识别预安装的 SED 驱动器
{: #identifying-preinstalled-sed-drives}

MegaRAID Storage Manager 预装在大多数受支持的操作系统上。如果不存在，您可以从 Broadcom 站点手动进行安装。有关更多信息，请参阅 [MegaRAID SAS 9361-8i downloads](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#downloads)。

您可以使用系统凭证来打开 MegaRAID Storage Manager。在示例中，使用的是 Windows 环境，并且预安装了 MSM。

启动 MSM 时，必须输入**用户名**和**密码**，这是特权用户 (Administrator) 和密码。

单击**物理**选项卡，并单击系统上可用的驱动器。**属性**窗格包含**驱动器安全属性**部分，其中包含**支持全磁盘加密**字段，该字段显示**是**。在使用的示例中，使用了两个非 SED 磁盘和四个 SED 磁盘。

### 在控制器上启用驱动器安全性
{: #enabling-drive-security-at-the-controller}

1. 要启用驱动器安全性，请在**物理**选项卡中右键单击**控制器 0：AVAGO MegaRAID SAS 9361-8i**，然后选择**启用驱动器安全性**。
  * 现在，可以输入**安全密钥标识**和**安全密钥**。如果有多个安全密钥，那么安全密钥标识可帮助您识别需要使用的安全密钥。必须将安全密钥记录在安全位置。重新配置驱动器（例如卸下或重新插入驱动器）时，需要使用安全密钥。如果没有安全密钥，那么无法检索根据 SED 创建的卷中存储的任何数据。无法检索忘记的安全密钥。还可以设置启动时间密码，这会使系统暂停，等待输入在此处设置的密码。启动时间密码是可选的，如果设置了此密码，那么每次重新引导系统时必须登录到 IPMI，并输入启动密码。向下滚动并选中显示**我记录了安全设置以供未来参考**的框，然后单击**是**以启用驱动器安全性。
  * 启用驱动器安全性后，将针对**控制器 0 AVAGO MegaRAID SAS 9361-8i** 显示一个黄色钥匙图像。
2. 现在使用 SED 创建安全卷。从**逻辑**选项卡右键单击 **Controller0** 选项卡，并选择  
**创建虚拟驱动器**。
3. 选择**高级**选项。屏幕要求将 **RAID 级别**和**驱动器安全方法**指定为**全磁盘加密 (FDE)**。选择需要的 FDE 驱动器，然后单击**添加** > **创建驱动器组** > **下一步**。
4. 查看虚拟驱动器设置并进行任何必要的更改。建议将**读取策略**设置为**始终预读**。建议将**写入策略**设置为**回写**。单击**创建虚拟驱动器**。通过单击**是**，接受 BBU 造成的“回写”策略影响。单击**下一步**并查看摘要屏幕。单击**完成**。
5. 要确认虚拟盘是否受保护，请单击**逻辑**选项卡和所创建的虚拟驱动器。您会在**驱动器安全属性**中看到**受保护**字段标记为**是**。

如果服务器随附了已使用 SED 驱动器创建的 RAID 卷，那么可以通过执行以下步骤来确保卷的安全。

在**逻辑**选项卡中，右键单击**驱动器组**，然后选择**保护 FDE 的使用**。如果针对某个卷混合使用 FDE 和非 FDE 驱动器，那么此选项不可见。

要除去驱动器安全性，必须先删除受保护的虚拟盘，然后右键单击控制器 0 以**禁用驱动器安全性**。此功能可安全地擦除其中的数据，并除去驱动器安全性。

您还可以使用 webBIOS，在启动时通过 IPMI 登录并输入 RAID BIOS 来设置驱动器安全性。<!--For more information, see **Avago SafeStore Encryption Services** in the **12 Gb/s MegaRAID SAS Software User Guide**.-->
