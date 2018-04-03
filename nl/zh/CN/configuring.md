---



copyright:
  years: 2017
lastupdated: "2017-12-05"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 配置裸机服务器

在供应 {{site.data.keyword.baremetal_long}} 之前，最好花些时间进行配置决策。这将使供应过程更快、更顺利。
{:shortdesc}

## 确定服务器用途和调整大小

第一个任务是确定打算如何使用 {{site.data.keyword.baremetal_short}}。例如，是打算将其用于开发/测试环境还是生产环境？是要测试用户体验，处理冗长的算法，备份和恢复数据，还是缩短等待时间以提高速度？

确定 {{site.data.keyword.baremetal_short}} 的用途后，需要调整大小。[SoftLayer 总拥有成本计算器](http://www.softlayer.com/tco/)可帮助根据您的需求确定最佳的 {{site.data.keyword.baremetal_short}} 配置。

## 选择服务器

{{site.data.keyword.cloud_notm}} 提供了 7 台快速供应服务器，以确保您拥有工作负载所需的性能。这些服务器目前在英国和美国南部区域可用。

| **配置**| **处理器**| **内存**| **硬盘驱动器**| **端口速度**|
|-------------------|---------------|------------|----------------|----------------|
| Intel Xeon E3-1270 V3|单 Intel Xeon E3-1270 V3（4 核，3.50 GHz）|32 GB RAM|1 个内部硬盘驱动器|100 Mbps 最大端口速度|
|Intel Xeon E5-2620 V3|双 Intel Xeon E5-2620 V3（6 核，2.40 GHz）|64 GB RAM|2 个内部硬盘驱动器|100 Mbps 最大端口速度|
|Intel Xeon E3-1270 V3|单 Intel Xeon E3-1270 V3（4 核，3.50 GHz）|32 GB RAM|2 个内部硬盘驱动器|100 Mbps 最大端口速度|
|Intel Xeon E5-2650 V3|双 Intel Xeon E5-2650 V3（10 核，2.30 GHz）|128 GB RAM|1 个内部硬盘驱动器|100 Mbps 最大端口速度|
|Intel Xeon E5-2690 V3|双 Intel Xeon E5-2690 V3（12 核，2.60 GHz）|128 GB RAM|2 个内部硬盘驱动器|100 Mbps 最大端口速度|
|Intel Xeon E5-2690 V3|双 Intel Xeon E5-2690 V3（12 核，2.60 GHz）|64 GB RAM|4 个内部硬盘驱动器|1,000 Mbps 最大端口速度|
|Intel Xeon E5-2690 V3|双 Intel Xeon E5-2690 V3（12 核，2.60 GHz）|256 GB RAM|4 个内部硬盘驱动器|1,000 Mbps 最大端口速度|

除了 7 台快速供应服务器外，{{site.data.keyword.cloud_notm}} 还扩展了其 {{site.data.keyword.baremetal_short}} 产品，现包含基于 POWER8 的裸机系统。这些系统采用 {{site.data.keyword.IBM_notm}} POWER8 处理器和一个基于 OpenPOWER 的平台进行构建，该平台已专门针对在 Linux 上基于云部署数据、认知和 Web 工作负载而调整。

任何 {{site.data.keyword.baremetal_short}} 都可以升级为包含不限流量（无限制）的带宽。所有不限流量的设备均位于私有专用端口。

## 设置裸机服务器

选择数据中心、服务器和记帐选项（每月或每小时）后，需要决定如何配置服务器。在**配置 {{site.data.keyword.baremetal_short}}** 页面上的某些字段（服务器、RAM、图形处理单元和辅助图形处理单元）中，将根据您的服务器选择设置缺省值。下表描述了可以为其定义值的字段。

| **字段**| **描述**|
|-------------------|---------------|
|操作系统|从 CentOS、FreeBSD、Microsoft、Red Hat、Ubuntu 或“其他”中选择。|
|硬盘驱动器|“磁盘配置”工具通过根据选择的操作系统预填字段来帮助您设置硬盘。|
|公共带宽|确定在一个月内可通过公共接口传输的数据量。对于需要通过此接口传输安装数据的测试环境，值需要调整到超过最初传输的数据量。您可能要考虑 [{{site.data.keyword.cloud_notm}} 内容交付网络](https://www.ibm.com/cloud/cdn)以将初始数据装入交付到某个 {{site.data.keyword.cloud_notm}} 数据中心。|
|上行端口速度|确定内部和外部接口的速度。|
|公共辅助 IP 地址|将一个额外的 IP 地址分配给服务器。根据您的场景，可能需要为服务器分配更多 IP 地址。按以下数量提供额外的 IPv4 地址：1、2、4、8、16 或 32。|
|主 IPv6 地址|分配给服务器的内部以及外部接口。|
|公共静态 IPv6 地址|从 /64 块分配额外的 IPv6 地址。|
|硬件和软件防火墙、防病毒软件和间谍软件防御，以及侵入和检测与防御|如果服务器将面向因特网，请选择相应的选项。强烈建议企业安全部门与 {{site.data.keyword.cloud_notm}} 支持合作，共同讨论这些选项的详细信息。|
|Evault |可以安装在服务器上以在服务器之间复制备份的基于代理程序的备份工具。|

请查阅 或联系 {{site.data.keyword.cloud_notm}} 支持以获取进一步的信息。


## 高级系统配置

单击**添加到订单**按钮并重定向到“结帐”页面后，会执行高级系统配置。下表描述了“高级系统配置”下的字段。

| **字段**| **描述**|
|-------------------|---------------|
|主机名|服务器的永久名称或临时名称，例如 _server1_。|
|域|子域名称，不应与因特网域名冲突，例如 _test.acme.com_。|
|VLAN 选择|如果因为您已经订购了至少一台服务器，而在您的帐户下有一个 VLAN，那么可以将新服务器添加到该 VLAN。|
|供应脚本|可以提供脚本，用于在供应服务器后自动执行某些步骤。|
|SSH 密钥|可以为 SSH 密钥提供公用密钥，以允许您在供应服务器后登录到服务器。|
