---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: custom server, {{site.data.keyword.baremetal_short}}, {{site.data.keyword.Bluemix_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# 构建定制的裸机服务器
{: #ordering-baremetal-server}

使用以下步骤来构建定制 {{site.data.keyword.baremetal_long}}。

## 通过 {{site.data.keyword.cloud_notm}} 目录供应
{: #provision-through-the-catalog}

使用以下步骤通过 {{site.data.keyword.cloud_notm}} 来供应 {{site.data.keyword.baremetal_short}}。

1. 打开 [{{site.data.keyword.cloud_notm}} 目录](https://cloud.ibm.com/catalog/){: external}。   
2. 在**计算**下选择 {{site.data.keyword.baremetal_short}}。
3. 单击“继续”。如果未看到“继续”按钮，那么可能需要登录。
4. 输入要供应的**相同**服务器的**数量**。缺省值为 1。如果要供应具有_不同_规格的多个服务器，您需要单独供应这些服务器。
5. **主机名**是服务器的永久或临时名称，例如 bakremetal01。单击**信息**以获取格式的具体要求。
6. **域**是用于定义因特网中管理控制的标识字符串，例如 Customer-123456.cloud。单击**信息**以获取格式的具体要求。
7. **计费**是**按小时**或**按月**进行的。
8. 选择服务器所在的**位置**、区域和数据中心。
9. 单击**所有服务器**以查看处理器（单处理器、双处理器和四处理器）和经认证的服务器（SAP 和 VMware）的列表。选择最符合您的工作负载的服务器。
10. 选择 **RAM**。对于某些服务器，RAM 基于 CPU 型号使用缺省值并且无法更改。 

对于 SAP 认证的服务器，RAM 和操作系统根据选择的服务器使用缺省值。本地存储器选项也将根据选择的服务器使用缺省值。{ :note}

11. 输入 **SSH 密钥**的可选公用密钥，可用于登录已供应的服务器。
12. 为服务器选择**映像**（操作系统）。您的选项基于所选服务器。
13. 展开**附加组件**以选择与服务器配置相关的选项。
14. **存储磁盘**根据选择的服务器进行了预配置。在供应 {{site.data.keyword.baremetal_short}} 后，展开**附加组件**以添加文件或块存储卷。 
15. 在**网络接口**下，选择“上行端口速度”和“专用 VLAN”选项。展开**附加组件**以选择相应的选项或使用缺省值。
16. 在“订单”摘要中查看您的订单。
17. 在**应用促销码**下输入您拥有的任何促销码。
18. 单击任何所列协议的第三方服务协议。
19. 单击**创建**以供应服务器。这会将您重定向到包含您的供应订单号的屏幕，您可以打印此屏幕，因为它也是您的回执。

将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。

_供应完成_电子邮件包含*设备详细信息*页面的链接，以便您可以登录到 {{site.data.keyword.cloud_notm}}。您还可以直接登录到 {{site.data.keyword.slportal}}。

您还可以选择将订单另存为报价或将其添加到估算。保存报价时，一条链接将发送到与您的帐户关联的电子邮件地址。打开该链接可查看已保存的报价信息。另一个选项是转至“管理”>“计费和使用情况”，然后选择“销售”>“设备报价”。如果您具有相应访问权，那么可以通过单击报价并确认订单来购买报价的产品。添加到估算会将配置建议的成本放在定价计算器中。单击**信息**以获取定价计算器的更多详细信息。

## 通过客户门户网站供应
使用以下步骤通过 {{site.data.keyword.slportal}} 来供应 {{site.data.keyword.baremetal_short}}。

1. 使用您的唯一凭证登录到 [{{site.data.keyword.slportal}}](control.softlayer.com){: external}。
2. 转至**帐户** > **下订单**。
3. 选择**按小时**或**按月**。
3. 从列表中选择希望 {{site.data.keyword.baremetal_short}} 位于的数据中心，然后通过单击**起步价**，选择经认证的服务器（SAP 或 VMware）或处理器（单处理器、双处理器和四处理器）。
4. 输入要供应的**相同**服务器的_数量_。缺省值为 1。如果要供应具有_不同_规格的多个服务器，您需要单独供应这些服务器。
5. 选择 **RAM**。对于某些服务器，RAM 基于 CPU 型号使用缺省值并且无法更改。 

对于 SAP 认证的服务器，RAM 和操作系统根据选择的服务器使用缺省值。本地存储器选项也将根据选择的服务器使用缺省值。{ :note}

6. 选择您的操作系统。
7. 选择硬盘驱动器和其他系统附加组件。
8. 单击将您重定向到的**添加到订单**，以确认订单。
9. 确认或编辑服务器的域信息。**主机名**是服务器的永久或临时名称，例如 bakremetal01。 
10. 选择**云服务条款**和**第三方服务协议**。
11. 在**促销码**下输入您拥有的任何促销码，并单击**应用**。
12. 确认或输入付款信息，然后单击**提交订单**。这会将您重定向到包含您的供应订单号的屏幕，您可以打印此屏幕，因为它也是您的回执。 

将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。“供应完成”电子邮件包含一个链接，用于在您登录到 {{site.data.keyword.Bluemix_notm}} 后转至*设备详细信息*页面。您还可以直接登录到 {{site.data.keyword.slportal}}。

## 后续步骤
供应 {{site.data.keyword.baremetal_short}} 后，您可以开始对其进行管理。有关更多信息，请参阅[管理 {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers)。
