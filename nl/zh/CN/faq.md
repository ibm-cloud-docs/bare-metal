---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-16"

keywords: bare metal, faq, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 常见问题：裸机服务器
{: #bm-faq}

## 什么是 UEFI 引导模式？
{: faq}
统一可扩展固件界面 (UEFI) 是操作系统和固件之间的软件界面规范。

IBM Cloud 对 BIOS 引导模式的支持会分阶段停止，以支持 UEFI。

有关 UEFI 的更多信息，请参阅硬件制造商文档或转至 [https://uefi.org/](https://uefi.org/)

## 为什么 BIOS 要求输入密码？
{: faq}

目前，由于各种原因，{{site.data.keyword.cloud}} 未提供直接访问 BIOS 的方法。但是，可以更改 BIOS。如果需要在 BIOS 中修改任何内容（包括引导顺序），请通过 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/){: new_window} 在“支持”>“添加凭单”下创建凭单，并请求所需的特定更改。

\*\*注\*\* 这需要重新引导服务器，因此请准备好核准重新引导和/或提供您希望执行更改的时间范围。

## 提供免费操作系统重装吗？
{: faq}

自动操作系统重装是免费的，可通过 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/){: new_window} 执行。这包括定制的操作系统重装（更改操作系统、添加/除去控制面板/分区编辑等）。有关执行操作系统重装的更多信息，请参阅[操作系统重装过程](/docs/infrastructure/software?topic=software-reloading-the-os)。


## 裸机服务器上的主驱动器显示为 /dev/sdb。出了什么问题？
{: faq}

导致此问题的原因可能是 IPMI 的“虚拟盘”占用 /dev/sda 槽。可以通过连接到 IPMIView 并浏览到“虚拟介质”选项卡来安全禁用此功能。选择**选项 > 禁用**，然后单击**应用**按钮以进行更改。下次重新引导 {{site.data.keyword.baremetal_short}} 时，主驱动器将显示 /dev/sda。⁄


## 为什么 CPU 速度不正确？
{: faq}

您登录到服务器来检查 CPU 信息，并注意到处理器速度不正确。导致这种差异的原因可能是增强型 Intel SpeedStep 技术 (EIST)。EIST 是 Intel 对动态频率调整技术的叫法。这种技术在较旧系统中也称为 *CPU 调速*或*总线压摆*。某些 AMD 系统也有类似技术，称为 *Cool'N'Quiet* 或 *PowerNow!*。虽然这些技术并不完全一样，但目标一致，都是要在处理器工作量不大时，通过降低 CPU 速度来减少功耗和产生的热量。在服务器恢复大工作量时，可根据需要提高时钟速度。

如果您希望了解服务器上的 Intel 处理器是否支持 SpeedStep，请在客户门户网站中使用以下过程：
1. 单击**设备**。
* 在列表中识别您的服务器。
* 单击服务器名称以查看**设备详细信息**。
* 找到标题为**硬件**的子部分，以找到服务器处理器 CPU 速度对应的型号。
* 有了服务器处理器型号后，转至 [Intel Processor Finder ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://processorfinder.intel.com/){: new_window}，使用此型号来查找有关该处理器的更多信息，并了解此型号是否支持增强型 Intel SpeedStep 技术。

EIST 是一种完善的技术。通常并不需要关闭 EIST。不过，如果您决定不想使用此功能，请向支持团队开具凭单以请求禁用此功能。要禁用此功能，需要重新引导服务器。


## 如果裸机服务器的固件已过期怎么办？
{: faq}

保持固件更新非常重要，可确保裸机服务器拥有最佳的设备兼容性和稳定性。如果 {{site.data.keyword.baremetal_short}} 固件版本过时，可以通过从设备列表中选择裸机服务器，然后从操作菜单中选择**更新固件**来更新固件。

您可以在 [{{site.data.keyword.slportal}} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/){: new_window} 中的[操作系统重装](/docs/infrastructure/software?topic=software-reloading-the-os)流程期间初始化固件更新。

## 客户使用完裸机服务器中的驱动器后，这些驱动器会怎么样？
{: faq}

取消时，服务器会自动移至一个回收 VLAN 中，并在其中保留设定的时间。完成后，将启动回收过程，并且将使用 DOD 5220.22-M 算法来擦除驱动器。将使用驱动器上的序列号来跟踪回收操作。完成后，服务器将移入供应以供重新分配。驱动器发生故障时，会提示手动干预，随后会将驱动器设置为使用寿命结束。

存在故障或者寿命或大小超过支持范围时，即会启动结束使用寿命过程。发生上述任一情况时，即会如前所述擦除驱动器。擦除过程完成后，驱动器将通过破坏、压碎或粉碎设备等物理方式销毁。将使用驱动器上的序列号来跟踪物理销毁过程。

## 我可以看到哪些裸机服务器可供购买吗？
{: faq}

可以！现在，供应裸机服务器时，您可以看到在哪个数据中心内提供了哪些服务器。但是，此选项仅适用于按小时提供服务的产品。对于按月提供服务的产品，您无法查看服务器可用性。有关供应裸机服务器的更多信息，请参阅[从快速供应服务器中选择](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers#bm-select-popular-servers)。

## 我预留的裸机服务器包含哪些内容？
{: faq}

CPU、RAM、磁盘驱动器和 RAID 根据合同条款包含在预留中。如果需要更高的网络带宽、更大的存储容量、更好的操作系统和第三方软件，那么这些附加组件将按月收费。

## 我的预留裸机服务器合同到期后会怎样？
{: faq}

您的云服务将根据合同到期时适用的费率，按每月服务时间段继续运行。
