---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 无操作系统选项
{: #bm-no-os}

“无操作系统”选项用于订购不带操作系统的裸机服务器。

## 如何订购无操作系统的裸机服务器？

首先通过 [SoftLayer.com](https://www.softlayer.com) 或[客户门户网站](https://control.softlayer.com)订购裸机服务器。

1. 从**系统配置 > 操作系统**中选择**其他**。
2. 选择**无操作系统**。

## 如何在无操作系统的服务器上安装操作系统？

有两种方法可用于在无操作系统的裸机服务器上安装操作系统。

### 选项 1：PXE 服务器

无操作系统的裸机服务器可以设置为通过 PXE 设置来引导和装入操作系统（有关更多信息，请参阅 [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment)）。只需在设置了 PXE 的网络环境中部署裸机服务器（这通常涉及运行 DHCP 和 TFTP 守护程序），并将新的裸机服务器 BIOS 配置为从网络适配器引导。要使“无操作系统”选项正常运行，PXE 设置需要与裸机服务器位于同一 VLAN 中，或者需要使用 DHCP 转发。

**注：**可能需要开具支持凭单，请求以基本方式将交换机端口重新分组，才能使此选项正常工作。这是由于 PXE 协议不需要与链路聚集（即 LACP，请参阅[链路聚集](http://en.wikipedia.org/wiki/Link_aggregation)）相兼容，现在这是提供冗余的标准功能。另一个选项是订购使用无绑定上行链路（无链路聚集）的服务器，然后在安装操作系统后，将其更改为冗余上行链路。

### 选项 2：IPMI 设备

通过随附的 IPMI 设备从 ISO 进行引导，将操作系统安装到无操作系统的裸机服务器上。单击[此处](mount-iso-bare-metal-server.html)以获取有关从 ISO 进行引导的其他信息。
