---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-02"

keywords: provision bare metal, popular servers, {{site.data.keyword.baremetal_short}}, provision

subcollection: bare-metal


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 从最常用的服务器中进行选择
{: #bm-select-popular-servers}

“最常用服务器”列表中的服务器已预配置，可满足大多数客户用例的需求，并且这些服务器在您订购后 30 到 40 分钟即准备就绪可运行。
1. 打开 [{{site.data.keyword.cloud_notm}} 目录 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/catalog/){: new_window}。   
2. 选择“裸机服务器”。
3. 单击“继续”。如果未看到“继续”按钮，那么可能需要登录。
2. 在 {{site.data.keyword.baremetal_short}} 部分中，选择以下信息：<table>
    <CAPTION>表 1. 裸机选择</CAPTION>
    <THEAD>
    <TR>
    <th>字段</th>
    <th>值</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>数量</td>
    <td>使用 + 和 - 图标来指定要供应的**相同**服务器的数量。缺省值为 1。<br>如果要供应具有**不同**规格的多个服务器，您需要单独供应这些服务器。<tr>
    <tr>
    <td>计费类型</td>
    <td>选择按小时或按月<tr>
    <td>主机名和域</td>
    <td>这些字段将使用缺省值进行填充。您可以对其进行更改。</td>
    </tr>
    <tr>
    <td>位置</td>
    <td>选择您希望服务器位于的区域。使用下拉列表，选择区域中的数据中心。</td>
    </tr>
    <tr>
    <tr>
    <td>选择服务器</td>
    <td>选择**常用服务器**并选择满足您需求的服务器。这些服务器已预配置，在 30 到 40 分钟后即准备就绪可使用。
    </tr>
    <tr>
    <td>RAM</td>
    <td>基于您选择的服务器的缺省值。</td>
    </tr>
    <tr>
    <td>SSH 密钥</td>
    <td>提供 SSH 密钥的公用密钥，用于登录到已供应的服务器。</td>
    </tr>
    <tr>
    <td>映像<br>（操作系统）</td>
    <td>选择服务器的操作系统。根据您选择的服务器，您的“映像”选项可能受到限制。</td>
    </tr>
    <td>附加组件</td>
    <td>展开“附加组件”部分以选择相应的选项或使用缺省值。<td>
    </tr>
    </TBODY>
    </table>
3. 在“存储磁盘”部分中，已选择“存储磁盘”作为“常用服务器”选项。如果想要将 IBM Cloud Backup 添加为服务器，请展开“附加组件”部分。
4. 在“网络接口”部分中，选择“上行端口速度”。展开“附加组件”部分以选择相应的选项或使用缺省值。
4.  复查订单。
4. 如果您拥有可应用于订单的促销码，请展开“应用促销码”。  
5.  查看列出的任何第三方服务协议，然后单击**第三方服务协议**复选框。
6.  单击**供应**。这会将您重定向到具有供应订单号的屏幕。您可以打印屏幕内容，因为这也是您的供应订单收据。

 将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。

 _供应完成电子邮件_包含*设备详细信息*页面的链接，以便您可以登录到 {{site.data.keyword.cloud_notm}}。您还可以直接登录到 {{site.data.keyword.slportal}}。


## 后续步骤

供应 {{site.data.keyword.baremetal_short}} 后，您可以开始对其进行管理。有关更多信息，请参阅[管理 {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers)。
