---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

keywords: bare metal, spare pools

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# 添加备用池
{: #adding-spare-pools}

备用池是一种保存特定设备的方式，这些设备被指定为备用设备，并且能够接管主设备的工作流程，或者充当客户群中的新设备。要将设备指定为备用设备，必须将其添加到备用池并关联到主设备。请遵循下面的步骤将设备添加到备用池。
{:shortdesc}

1. 使用您的唯一凭证访问 [{{site.data.keyword.cloud}} 控制台 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/){: new_window}。
2. 从导航栏中选择**设备 > 备用池**以访问*备用池*屏幕。
3. 单击**添加到备用池**链接。

   这将填充有资格添加到备用池的设备的列表。
   {:tip}

4. 选择要添加到备用池的设备。
5. 单击**添加所选设备**。
6. 单击**确认**以将设备添加到备用池。

## 后续步骤
启动设备到备用池的传输后，设备会在一小时内转换到备用池。设备在备用池中处于活动状态后，会显示在“备用池”屏幕上，并可指定为主设备的热备用。
