---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-18"

keywords: manage bare metal port control

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 管理设备的端口控制
{: #bm-manage-port-control}

与帐户关联的每个设备都有两个接收入局流量的网络端口 - 一个用于公用网络流量，一个用于专用网络流量。您可以随时启用或禁用这些端口，以控制设备接收的网络流量。要更新设备的端口控制设置，请完成以下步骤。

## 准备工作
* 导航至控制台的设备菜单。有关更多信息，请参阅[导航至设备](/docs/bare-metal?topic=virtual-servers-navigating-devices)。
* 确保您具有任何必要的帐户许可权和设备访问权。只有帐户所有者或具有**管理用户**经典基础架构许可权的用户才能调整许可权。

有关许可权的更多信息，请参阅[经典基础架构许可权](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理设备访问权](/docs/bare-metal?topic=virtual-servers-managing-device-access)。

## 管理设备的端口控制

1. 访问**设备列表**并选择要更新的**设备名**。  
2. 单击设备的**操作**下拉列表。
3. 选择**端口控制**。
4. 通过完成以下其中一个操作来更新*公用网络*和/或*专用网络*下拉框：
   * 选择所需的速度以启用网络访问。
   * 选择“已断开连接”以禁用网络访问。
5. 单击“更新”按钮。
6. 单击“关闭”按钮以关闭窗口。

## 后续步骤

如果选择**已禁用**，那么用于设备接口的已禁用端口的网络访问将停止。如果选择了**已启用**，那么网络访问可用于已启用的端口。端口控制将保留在所选设置中，直到手动更改为止。
