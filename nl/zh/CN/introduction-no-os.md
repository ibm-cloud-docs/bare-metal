---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: bare metal, no os, no operating system

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# 无操作系统选项
{: #bm-no-os}

**无操作系统**选项用于订购不带操作系统的 {{site.data.keyword.baremetal_long}}。

## 订购不带操作系统的 {{site.data.keyword.baremetal_short}}
{: #ordering-no-os}

1. 使用[构建定制裸机服务器](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server)中概述的步骤订购您的服务器。
2. 在**映像**下选择**无操作系统**。
3. 完成服务器订单。 

## 更改为无操作系统
{: #changing-to-no-os}

服务器可以重新配置为没有操作系统。重新配置是通过操作系统重装完成的。有关更多信息，请参阅[重装操作系统](/docs/infrastructure/software?topic=software-reloading-the-os)。

1. 单击**设备** > **设备列表**。
2. 选择重新配置为无操作系统的服务器。
3. 单击**操作系统重装**并输入适用的信息。

## 在无操作系统的服务器上安装操作系统
{: #installing-os-on-no-os-server}

在无操作系统的 {{site.data.keyword.baremetal_short}} 上安装操作系统有两种方法。

### 选项 1：PXE 服务器
{: #option-1}

可以将无操作系统的 {{site.data.keyword.baremetal_short}} 设置为根据 PXE 设置来引导和装入操作系统。<!--(see [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) for more information)-->在带有 PXE 设置（这通常涉及运行 DHCP 和 TFTP 守护程序）的网络环境中部署 {{site.data.keyword.baremetal_short}}，并将新的服务器 BIOS 配置为从网络适配器引导。要使“无操作系统”选项正常运行，PXE 设置需要与 {{site.data.keyword.baremetal_short}} 位于同一 VLAN 中，或者需要使用 DHCP 转发。

可能需要开具支持凭单，请求以基本方式将交换机端口重新分组，才能使此选项正常工作。这是由于 PXE 协议不需要与链路聚集 (LACP) 相兼容<!--see [Link Aggregation](http://en.wikipedia.org/wiki/Link_aggregation))-->，现在 LACP 是提供冗余性的标准功能。另一个选项是订购使用无绑定上行链路（无链路聚集）的服务器，然后在安装操作系统后，将其更改为冗余上行链路。
{: note}

### 选项 2：IPMI 设备
{: #option-2}

通过经由随附的 IPMI 设备从 ISO 进行引导，在 {{site.data.keyword.baremetal_short}} 上安装操作系统。有关从 ISO 引导的更多信息，请参阅[在裸机服务器上安装 ISO](/docs/bare-metal?topic=bare-metal-mounting-an-iso-on-a-bare-metal-server)。
