---



copyright:
  years: 2017, 2018
lastupdated: "2018-07-06"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 构建定制裸机服务器
{: #ordering-baremetal-server}

使用以下步骤来构建定制 {{site.data.keyword.baremetal_short}}。

1. 打开 [{{site.data.keyword.cloud_notm}} 目录](https://console.bluemix.net/catalog/){:target="_blank"}。   
2. 选择“裸机服务器”。
3. 单击“创建”。
4. 在服务器列表下面，查找以下语句：**对其他配置选项感兴趣？请单击此处**。选择此选项。这将显示定制服务器表单。
1. 选择服务器的数据中心位置。
* 通过单击**起步价（单位）**链接，从三个服务器类别中选择服务器。
  * SAP 认证的服务器（有关供应 SAP 认证服务器的更多信息，请参阅 [{{site.data.keyword.cloud_notm}} SAP 认证的基础架构](/docs/bare-metal/bare-metal-sap-applications.html)）
  * 单处理器多核服务器
  * 双处理器多核服务器

* 从配置选项中进行选择。**数据中心**、**RAM** 和**操作系统**是必填字段。其他所有字段都是可选字段。有关可选字段的更多信息，请参阅**[其他服务器配置选项](#addl-server-options)**。

    **注**：如果服务器与操作系统之间存在冲突，那么会显示错误消息。例如，在 Microsoft SQL Server 上选择 Linux。
* 单击**添加到订单**。这将显示“结帐”页面。

  在“结帐”页面中，可以通过单击其中一个“重新配置”选项来返回到配置页面。
* 在“高级系统配置”部分中，指定其他配置选项。有关更多信息，请参阅**[高级系统配置](#adv-system-config)**。

*   单击**云服务条款**和**第三方服务协议**复选框。
*   确认或输入付款信息，然后单击**提交订单**。这会将您重定向到具有供应订单号的屏幕。您可以打印屏幕内容，因为这也是您的供应订单收据。

  您还可以通过单击**另存为报价**来保存此订单而不购买。

 将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。登录到 {{site.data.keyword.cloud_notm}} 后，供应完成电子邮件包含*设备详细信息*页面的链接。您还可以直接登录到 {{site.data.keyword.slportal}}。

 ## 其他服务器配置选项
 {: #addl-server-options}

 供应裸机服务器时，您还可以选择其他选项，例如公共带宽、上行端口速度、公共辅助 IP 地址等。表 1 描述了这些其他选项。


 |**字段**|**描述**|
 |-------------------|---------------|
 |服务器安全性|例如，可信执行技术 (Intel TXT)|
 |Software Guard Extensions|提高了敏感代码和数据的安全性 (Intel SGX)。<br><br>请参阅[供应采用 Intel SGX 的裸机服务器](../bare-metal/bare-metal-provision-SGX.html)。|
 |RAM|选择满足您服务器需求的 RAM 级别。|
 |操作系统|从 CentOS、FreeBSD、Microsoft、Red Hat、Ubuntu 或“其他”中进行选择。|
 |硬盘驱动器|使用用户界面中的该工具，通过基于操作系统选择来预填充字段，从而设置硬盘。<br><br> 您还可以选择使用 Intel Optane SSD 驱动器。请参阅[供应 Intel Optane SSD DC P4800X](../bare-metal/bm-provision_ssd.html)。 |公共带宽|确定在一个月内可通过公共接口传输的数据量。对于需要通过此接口传输安装数据的测试环境，值需要调整到超过最初传输的数据量。请考虑 [{{site.data.keyword.cloud_notm}} 内容交付网络](https://www.ibm.com/cloud/cdn)以将初始数据负载交付到其中一个 {{site.data.keyword.cloud_notm}} 数据中心。任何 {{site.data.keyword.baremetal_short}} 都可以升级为包含不限流量（无限制）的带宽。所有不限流量的设备均位于私有专用端口。|
 |上行端口速度|确定内部和外部接口的速度。|
 |公共辅助 IP 地址|将更多 IP 地址分配给服务器。根据您的场景，可能需要为服务器分配更多 IP 地址。按以下数量提供了更多 IPv4 地址：1、2、4、8、16 或 32。|
 |主 IPv6 地址|分配给服务器的内部以及外部接口。|
 |公共静态 IPv6 地址|从 /64 块中分配更多 IPv6 地址。|
 |操作系统附加组件|选择 VMware、备份解决方案、控制面板、数据库、硬件和软件防火墙、防病毒和防间谍软件、入侵检测和保护等选项。<br><br>强烈建议企业安全部门与 {{site.data.keyword.cloud_notm}} 支持合作，共同讨论这些选项的详细信息。 |Evault |可以安装在服务器上以在服务器之间复制备份的基于代理程序的备份工具。|
 |服务附加组件|选择任何服务附加组件，例如监视、自动响应和保险。|
 {: caption="表 1. 其他服务器选项" caption-side="top"}

## 高级系统配置
{: #adv-system-config}

**高级系统配置**下的字段用于完成供应过程。

|**字段**|**描述**|
|---|---|
|主机名|服务器的永久名称或临时名称，例如 _server1_。**注**：如果要供应 SAP 认证的服务器，那么 SAP 主机名必须由最多 13 个字母数字字符组成。有关 SAP 主机名的更多信息，请参阅 [SAP Notes 2611361](https://launchpad.support.sap.com/#/notes/2611361) 和 [129997](https://launchpad.support.sap.com/#/notes/129997)。需要 SAP S 用户标识。|
|域|不应与因特网域名相冲突的子域名，例如 _test.acme.com_。|
|VLAN 选择|如果因为您已经订购了至少一台服务器，而在您的帐户下有 VLAN，那么可以将新服务器添加到该 VLAN。|
|供应脚本|可以提供脚本，用于在供应后自动执行某些步骤。|
|SSH 密钥|可以提供 SSH 密钥的公用密钥，以允许您在供应服务器后登录到服务器。|
{: caption="表 2. 高级系统配置" caption-side="top"}

 请咨询 {{site.data.keyword.cloud_notm}} 支持以获取进一步信息。

 **注：**您可以为计算设备订购辅助子网。但是，如果订购辅助子网，那么回收计算设备时会回收这些子网。如果单独订购辅助子网（而不是作为计算订单的附加组件选项），那么可以保留子网，直到您将其显式取消为止。记住这一区别非常重要，以便您在回收计算设备时，不会无意中丢失某些 IP 地址。

## 后续步骤
供应 {{site.data.keyword.baremetal_short}} 后，您可以开始对其进行管理。有关更多信息，请参阅[管理 {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html)。
