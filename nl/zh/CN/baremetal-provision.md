---



copyright:
  years: 2017
lastupdated: "2017-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 供应裸机服务器

## 开始之前
您有两个选项可以供应公共 {{site.data.keyword.baremetal_long}}。第一个选项是通过 {{site.data.keyword.cloud}}“目录”供应，第二个选项是通过 {{site.data.keyword.slportal_full}}供应。“目录”和 {{site.data.keyword.slportal}}需要唯一登录标识。您的“目录”用户名和密码无法用于登录到门户网站，门户网站的用户名和密码也无法用于登录到“目录”。
{:shortdesc}

开始之前，请确保已设置 {{site.data.keyword.cloud_notm}}“目录”或 {{site.data.keyword.slportal}}凭证。

**注：**对于 {{site.data.keyword.cloud_notm}}“目录”，您必须具有升级的帐户才能订购 {{site.data.keyword.baremetal_short}}。有关升级帐户的更多信息，请参阅[切换到 IBM 标识](https://console.ng.bluemix.net/docs/admin/softlayerlink.html)。

## 登录
确保已通过 {{site.data.keyword.cloud_notm}}“目录”或 {{site.data.keyword.slportal}}登录：

  <table>
   <CAPTION>表 1. 选择登录位置</CAPTION>
   <THEAD>
   <TR>
   <th>如果登录要使用...</th>
   <th>请执行以下步骤...</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud“目录”</td>
   <td>
   <ol>
   <li>打开新的浏览器窗口并输入 <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>。</li>
   <li>单击<b>登录</b>链接。</li>
   <li>输入您的电子邮件或 IBM 标识，然后单击<b>继续</b>。</li>
   <li>输入您的密码，然后单击<b>登录</b>。</li>
   <li>选择<b>基础架构</b> > <b>计算</b>。</li>
   <li>单击 <b>{{site.data.keyword.baremetal_short}}</b> 磁贴。</li>
   <li>单击<b>创建</b>。这将打开 {{site.data.keyword.slportal}}的主页。</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>客户门户网站</td>
   <td>
   <ol>
   <li>打开新的浏览器窗口并输入 <a href="https://control.softlayer.com">https://control.softlayer.com</a>。</li>
   <li>输入您的用户名和密码，然后单击<b>登录</b>。或者，单击<b>使用 IBM 标识登录</b>。接着，输入您的电子邮件或 IBM 标识，然后单击<b>继续</b>。输入您的密码，然后单击<b>登录</b>。这将打开 {{site.data.keyword.slportal}}的主页。</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## 供应裸机服务器
{: #ordering-baremetal-server}
登录后，即可以开始供应 {{site.data.keyword.baremetal_short}}。您可以通过**设备**菜单或**设备**图标来供应 {{site.data.keyword.baremetal_short}}。

### 通过设备图标供应裸机服务器
要通过*设备*图标供应 {{site.data.keyword.baremetal_short}}，请完成以下步骤：

1.  在 {{site.data.keyword.slportal}}中，找到**订购**部分，然后单击**设备**。
2.  在“设备”页面上的 {{site.data.keyword.baremetal_short}} 下，单击**每小时**或**每月**。
3.  选择**数据中心**，滚动浏览页面，然后单击**起步价（单位）**链接以选择服务器。
4.  填写**配置 {{site.data.keyword.baremetal_short}}** 页面上的信息，然后单击**添加到订单**按钮以继续。有关如何配置服务器的更多信息，请参阅[配置 {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.html)。验证订单后，会将您重定向到**结帐**页面。
5.  输入服务器的**高级系统配置**。有关如何设置高级系统配置的更多信息，请参阅[配置 {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.html)。
6.  单击**云服务条款**和**第三方服务协议**复选框。
7.  确认或输入付款信息，然后单击**提交订单**按钮。这会将您重定向到具有供应订单号的屏幕。您可以打印屏幕内容，因为这也是您的供应订单收据。

 将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。登录到 {{site.data.keyword.cloud_notm}} 后，供应完成电子邮件会包含指向*设备详细信息*页面的链接。您还可以直接登录到 {{site.data.keyword.slportal}}。

### 通过设备菜单供应裸机服务器
{: #ordering-baremetal-devices-menu}

您还可以通过 {{site.data.keyword.slportal}}主页上的*设备*菜单来供应 {{site.data.keyword.baremetal_short}}。

1. 单击**设备 > 设备列表**。“设备”页面会显示您帐户内的所有设备类型 - 专用主机、虚拟服务器、裸机服务器和 NetScaler 应用程序交付控制器。
2. 单击右上角的**订购设备**链接。
3. 在“订购 SoftLayer 产品和服务”页面上的 {{site.data.keyword.baremetal_short}} 下，单击**每小时**或**每月**。
4. 选择**数据中心**，滚动浏览页面，然后单击**起步价（单位）**链接以选择服务器。
5.  填写**配置 {{site.data.keyword.baremetal_short}}** 页面上的信息，然后单击**添加到订单**按钮以继续。有关如何配置服务器的更多信息，请参阅[配置 {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.html)。验证订单后，会将您重定向到**结帐**页面。
6.  输入服务器的**高级系统配置**。有关如何设置高级系统配置的更多信息，请参阅[配置 {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.html)。
7. 单击**云服务条款**和**第三方服务协议**复选框。
8. 确认或输入付款信息，然后单击**提交订单**按钮。这会将您重定向到具有供应订单号的屏幕。您可以打印屏幕内容，因为这也是您的供应订单收据。

将向您的管理员发送一系列电子邮件：确认供应订单、供应订单核准和处理以及供应完成。登录到 {{site.data.keyword.cloud_notm}} 后，供应完成电子邮件会包含指向*设备详细信息*页面的链接。您还可以直接登录到 {{site.data.keyword.slportal}}。

### 后续步骤
供应 {{site.data.keyword.baremetal_short}} 后，您可以开始对其进行管理。有关更多信息，请参阅[管理 {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html)。
