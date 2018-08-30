---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-21"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 从最常用的服务器中进行选择
“最常用服务器”列表中的服务器已预配置，可满足大多数客户用例的需求，并且这些服务器在您订购后 30 到 40 分钟即准备就绪可运行。
1. 打开 [{{site.data.keyword.cloud_notm}} 目录](https://console.bluemix.net/catalog/){:target="_blank"}。   
2. 选择“裸机服务器”。
3. 单击“创建”。
2. 选择以下信息：
    <table>
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
    <td>使用 + 和 - 图标来指定要供应的完全相同的服务器数。<br>如果要供应具有不同规格的多个服务器，您需要单独供应这些服务器。<tr>
    <td>位置</td>
    <td>选择您希望服务器位于的区域和数据中心。</td>
    </tr>
    <tr>
    <tr>
    <td>主机名和域</td>
    <td>这些字段将使用缺省值进行填充。您可以对其进行更改。</td>
    </tr>
    <tr>
    <td>选择服务器</td>
    <td>在**常用服务器**下，选择满足您需求的服务器。这些服务器已预配置，在 30 到 40 分钟后即准备就绪可使用。
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
    <td>为实例选择操作系统。**注**：如果服务器与操作系统之间存在冲突，那么会显示错误消息。例如，在 Microsoft SQL Server 上选择 Linux。</td>
    </tr>
    <td>上行端口速度</td>
    <td>确定内部和外部接口的速度。</td>
    </tr>
    <tr>
    <td>附加组件</td>
    <td> 选择相应的选项或使用缺省值。</td>
    </tr>
    </TBODY>
    </table>

3.  在“订单摘要”部分中，选择**每小时**或**每月**计费。
4.  复查订单。
5.  查看列出的任何第三方服务协议，然后单击**第三方服务协议**复选框。
6.  单击**供应**。这会将您重定向到具有供应订单号的屏幕。您可以打印屏幕内容，因为这也是您的供应订单收据。

 将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。供应完成电子邮件包含*设备详细信息*页面的链接，以便您可以登录到 {{site.data.keyword.cloud_notm}}。您还可以直接登录到 {{site.data.keyword.slportal}}。


## 后续步骤
供应 {{site.data.keyword.baremetal_short}} 后，您可以开始对其进行管理。有关更多信息，请参阅[管理 {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html)。
