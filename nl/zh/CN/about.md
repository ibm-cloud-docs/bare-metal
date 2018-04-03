---



copyright:
  years: 2016
lastupdated: "2016-01-19"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 开始使用 {{site.data.keyword.baremetal_short}}

通过 {{site.data.keyword.baremetal_long}}，您将具备卓越性能和控制能力。{{site.data.keyword.baremetal_short}} 并不在系统管理程序中运行，因此您将获取对硬件资源的低级别访问权。此外，没有其他任何客户与您共享该服务器 - 仅供您独家享用！
{:shortdesc}

创建 {{site.data.keyword.baremetal_short}} 时，可以定制从处理器和区域到操作系统和硬盘驱动器等各种规范。

要供应 {{site.data.keyword.baremetal_short}}，请执行以下操作：
  1. 转至**计算 > {{site.data.keyword.baremetal_short}}**，然后单击**添加**。
  2. 选择要供应 {{site.data.keyword.baremetal_short}} 实例的位置。这是其中一个 {{site.data.keyword.Bluemix}} 区域中的数据中心。
  3. 选择服务器的配置。此配置将应用于为此实例创建的所有服务器。
  4. 选择要为此实例创建的服务器数。对于每个服务器，输入唯一的主机名。
  5. **可选：**输入已定义的脚本或文本文件的 URL 来配置服务器。供应脚本必须使用 HTTPS 协议。脚本会在实例供应后下载并执行（如果可能）。如果 URL 未与可执行脚本相关联，那么将只下载该脚本。
  6. 为服务器选择操作系统。此操作系统将应用于为此实例创建的所有服务器。

在一小时内，{{site.data.keyword.baremetal_short}} 将得到供应并可供使用。
