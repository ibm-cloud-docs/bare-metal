---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 创建和调整 Adaptec RAID 配置

通过 Adaptec RAID BIOS，您可以配置和管理 RAID 设置。如果要使用[无操作系统](introduction-no-os.html)选项，并且希望设置特定驱动器配置，请使用此 BIOS。

## 访问 IPMI 设备以与 RAID BIOS 交互

不管计算机是具有 Adaptec 控制器还是 LSI 控制器，您都需要使用 IPMI 来访问服务器，以便与 RAID BIOS 进行交互。为了与 IPMI 交互，您首先需要连接到 Adaptec {{site.data.keyword.IBM&reg; Cloud}} VPN。
1. 通过 [SSL](/infrastructure/vpn/ssl-vpn-connections.html) 或 PPTP 登录到 VPN。请参阅 [VPN 主题页面](/infrastructure/vpn/index.html)。
* 访问[客户门户网站](https://control.softlayer.com/)中的“设备列表”。请参阅[访问设备列表](../vsi/vsi_managing.html)。
* 单击要访问的设备。
* 选择“远程管理”选项卡以查找服务器 IPMI 访问详细信息。
* 向浏览器提交 IPMI 设备的 IP 并登录。
* 要开始与远程控制台交互，请单击“远程控制”>“控制台重定向”。

## 创建 RAID 阵列

在引导过程中，按 Ctrl+A 键以访问 RAID BIOS。

要开始配置 RAID，请转至“逻辑设备配置”（第一个选项）。这会扫描驱动器的拓扑并显示一个菜单，通过该菜单可管理阵列、创建阵列和完成其他驱动器管理任务。

以下示例显示如何创建阵列。这将向您显示可在创建 RAID 阵列时使用的可用驱动器的列表。

1. 要选择驱动器，请按空格键以填充*所选驱动器*框。
* 选择好要在阵列中使用的所有驱动器后，按 ENTER 键以转至 RAID 配置步骤。
* 选择所需的 RAID 类型。如果您需要帮助来确定哪个 RAID 设置最适合您的需求，请参阅以下 [Adaptec 常见问题](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm)。
* 在配置过程中提供“阵列标签”。最好在标签中包含 RAID 类型（例如：RAID10-A）。
* 按 Enter 键以浏览其余设置。请使用缺省值。

完成配置选择后，选择“完成”；这将创建 RAID。可以通过从主菜单中选择“管理阵列”来查看新阵列。要退出配置实用程序，请按 ESC 键，直至提示您退出 Adaptec BIOS。

## 除去现有阵列

如果需要除去现有阵列，请转至“管理阵列”>“选择要除去的阵列”，然后按“删除”并确认。

## 示例配置

1. 在一台共有 6 个驱动器的服务器上，可以在 RAID0 中设置 2 个 SSD 用于操作系统，在 RAID10 中设置 4 个额外的驱动器用于实际数据。这使您能够快速重装服务器操作系统，而无需复原站点或服务数据（如果它位于辅助阵列上）。

* 在 cPanel 服务器上，可以使 /var 和 /home 位于单独的 SSD RAID 阵列上。由于它们是 cPanel 服务器上 IO 密集程度最高的两个目录，因此使用以下设置有可能缩短站点响应时间：
  * RAID0（2 个 SATA 驱动器）- /
  * RAID0（2 个 SSD 驱动器）- /var
  * RAID0（2 个 SSD 驱动器）- /home
  * RAID10（4 个 SATA 驱动器）- /backup

* 使用单个 RAID 阵列来设置多个逻辑分区。例如，使用在 RADI1 中设置的两个 4 TB 驱动器。您可以根据需要对 RAID 进行分区。例如：
  * 主分区 100 GB，用于操作系统
  * 第二个分区 500 GB，用于数据
  * 剩余空间作为第三个分区，用于备份
