---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

keywords: spare pools, cancel, bare metal

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# 取消备用池
{: #cancel-spare-pools}

已添加到备用池的设备只能在 {{site.data.keyword.cloud}} 控制台中的“备用池”屏幕中取消。取消备用池中的设备与取消“设备列表”中的设备相同。请遵循下面的步骤来取消备用池中的设备。
{:shortdesc}

## 取消备用池

1. 备份要取消的设备中需要保留的任何数据。

   取消设备会导致从取消的设备中除去所有数据。设备取消后，存储在该设备上的所有信息都无法再取回。
   {:tip}

2. 使用您的唯一凭证访问 [{{site.data.keyword.cloud}} 控制台 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/){: new_window}。
3. 从导航栏中选择**设备 > 备用池**以访问*备用池*屏幕。
4. 对于特定设备，选择**操作 > 取消设备**。
5. 从**原因**下拉列表中，选择取消原因。
6. 在提供的文本框中输入简要取消说明。
7. 单击**继续**以继续至下一个屏幕。单击**取消**以停止取消过程并返回到“备用池”屏幕。
8. 选择**数据丢失确认**以确认在取消过程中可能发生数据丢失。
9. 单击**取消设备**以取消设备。单击**关闭**以停止取消过程并返回到“备用池”屏幕。

## 后续步骤
在请求取消备用池中的设备后，系统会安排取消该设备。接着会立即回收该设备并将其从帐户中除去。
