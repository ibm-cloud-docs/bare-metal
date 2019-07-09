---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-16"

keywords: bare metal, getting started, {{site.data.keyword.cloud}}, {{site.data.keyword.cloud_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 入门教程
{: #getting-started}

{{site.data.keyword.baremetal_long}} 是单租户物理服务器，通过对硬件资源的低级别访问来提供性能和控制。您的服务器不会与“嘈杂的邻居”共享，而是供您专用！
{: shortdesc}

表 1 包含帮助您快速供应和配置 {{site.data.keyword.baremetal_short}} 的步骤。
<table>
   <CAPTION>表 1. 快速入门步骤</CAPTION>
   <THEAD>
   <TR>
   <th>任务</th>
   <th>详细信息</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>1. 查看可帮助您实施的内容</td>
   <td>IBM Cloud 和裸机服务器的新功能？以下站点提供了有助于您规划环境的有用信息。
   <li><a href="https://ibm.com/cloud-computing/">什么是 IBM Cloud</a></li>
   <li><a href="https://ibm.com/cloud/get-started">IBM Cloud 入门</a></li>
   <li><a href="https://www.ibm.com/cloud/bare-metal-servers">Bare Metal Servers</a></li>
   </td>
 <tr>
   <td>2. 注册 IBM Cloud</td>
   <td><a href="https://cloud.ibm.com/docs/account?topic=account-signup#signing-up-for-ibm-cloud">注册 IBM Cloud</a> 包含有关如何设置 IBM Cloud 帐户的步骤。</td>
 <tr>
   <td>3. 确定工作负载规范</td>
   <td>供应服务器之前，请确定将如何使用服务器，以及成功运作所需要的服务器大小。例如，是打算将其用于开发和测试环境还是生产环境？是要测试用户体验，处理冗长的算法，备份和恢复数据，还是缩短等待时间以提高速度？</td>  
 <tr>
   <td>4. 确定服务器大小并估算成本</td>
   <td>可以使用<a href="https://cloud.ibm.com/gen1/infrastructure/provision/bm">裸机搜索工具</a>来帮助确定服务器大小并估算成本。</td>
 <tr>
   <td>5. 登录到 IBM Cloud 帐户</td>
   <td>您可以通过 IBM Cloud“目录”或 IBM Cloud Infrastructure 客户门户网站来访问“裸机服务器订购表单”。您需要 <a href="https://cloud.ibm.com/docs/customer-portal?topic=customer-portal-getting-started#getting-started">IBM 标识和密码</a>才能访问目录和基础架构客户门户网站。
   <li><a href="https://cloud.ibm.com/catalog/">IBM Cloud“目录”</a></li>
   <li><a href="https://cloud.ibm.com">IBM Cloud 控制台</a></li>  
   </td>   
<tr>   
   <td>6. 供应服务器</td>
   <td>供应服务器时有三个选项：快速供应、定制和 SAP 认证。快速供应服务器是预配置的服务器，可满足大多数客户的需求，并且供应后 30 到 40 分钟即准备就绪可开始配置。


<br>定制服务器是您通过选择特定计算、连接、存储和网络选项以满足自身需求而创建的服务器。定制服务器需要更长时间才能完成供应，通常为 2 到 4 小时，并且运营成本更高。您可以[供应与 Intel Optane 兼容的裸机服务器](/docs/bare-metal?topic=bare-metal-provisioning-an-intel-optane-compatible-bare-metal-server#provisioning-an-intel-optane-compatible-bare-metal-server)或者采用 [Intel SGX 体系结构](/docs/bare-metal?topic=bare-metal-provisioning-a-bare-metal-server-with-intel-sgx-architecture#provisioning-a-bare-metal-server-with-intel-sgx-architecture)的裸机服务器。

<br>SAP 认证的服务器经过认证，支持 SAP HANA 和 SAP NetWeaver 架构。使用以下链接可获取该类型服务器的供应信息。请注意，对于 SAP 认证的服务器，您需要选择要供应的架构类型：SAP HANA 或 SAP NetWeaver。<br>
* [快速供应的裸机服务器](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers)<br>
* [定制裸机服务器](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server#ordering-baremetal-server)<br>
* [IBM Cloud SAP 认证的基础架构](/docs/bare-metal?topic=bare-metal-ibm-cloud-sap-certified-infrastructure#ibm-cloud-sap-certified-infrastructure)
  </td>
 <tr>
   <td>7. 配置裸机服务器</td>
   <td>服务器现在已准备好进行配置。请参阅**配置**下的主题。</td>
   </td>
   </tr>
   </TBODY>
   </table>
