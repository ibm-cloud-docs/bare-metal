---

copyright:
  years: 2017, 2019
lastupdated: "2018-06-03"

keywords: mount iso bare metal

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 在裸机服务器上装载 ISO
{: #bm-mount-iso}

## 概述

尽管大多数 {{site.data.keyword.cloud}} 客户都使用服务器随附的其中一个标准操作系统，但您也可以在服务器上装载定制的 ISO（磁盘映像）。您有三个用于装载定制 ISO 的选项。

要使这些方法生效，您需要通过 SL VPN 服务（例如 [SoftLayer SSL VPN 门户网站 - AMS01](https://vpn.ams01.softlayer.com/prx/000/http/localhost/login)）或通过连接到专用网络的其他服务器来连接到该专用网络。

**注：**大于 50 MB 的 Lenovo 硬件磁盘映像必须使用 IMM 控制台界面中的“介质”选项卡来进行装载。

## 选项 1（首选）：使用 IPMI（CIFS 共享上的 ISO）
{: #bm-mount-iso-opt-1}

如果已在 {{site.data.keyword.cloud_notm}} 上部署了基础架构，那么可以将现有服务器配置为向内部网络提供 CIFS 共享。然后，可以将其中的任何 ISO 装载到裸机服务器。

这是在裸机服务器上安装定制操作系统的首选方法，因为它会通过本地网络安装，速度非常快，即便您从管理界面注销或断开连接，也可以使 ISO 保持装载。

要从 CIFS 共享安装定制操作系统，请执行以下步骤：

1. 确保已将 ISO 放置在 CIFS 共享上。
* 通过将 Web 浏览器指向 cloud.ibm.com 中指定的 IP，然后在“设备”-> 您的服务器（设备详细信息） -> “远程管理”下，登录到 IPMI 管理控制台。用户名和密码也在此处指定。
* 将鼠标悬停在**虚拟介质**上，然后单击 **CD-ROM 映像**
* 填写相应的详细信息，单击**保存并装载**。
* 并非所有用户都有权更改服务器的 BIOS。您可以根据需要向支持人员开具凭单以请求：
  * 授予对 IPMI 的 root 用户管理员特权（能够更改“虚拟介质连接”方式）
  * 将引导顺序更改为“IPMI 虚拟盘”作为第一个引导选项。
* 进行这些更改后，返回到 IPMI 管理控制台，并转至“配置”->“远程会话”，然后将连接方式更改为**连接**。在某些较低版本的 IPMI 控制台中，可以跳过此选项。
* 重新引导服务器，然后从虚拟介质引导。


## 选项 2：使用 IPMIView（CIFS 共享上的 ISO）
{: #bm-mount-iso-opt-2}

先决条件：<br/>
* 您具有可引导的 ISO
* 用于存储可引导 ISO 的 Windows CIFS 服务器或 NAS 存储器
* ISO 已上传到与服务器关联的文件存储器 (NAS)
* IPMIView 已安装或访问 KVM 控制台
* ISO 文件可使用 wget 进行下载
* 您具有 SSH 访问权，有权访问/安装包和创建装载


### Linux 和 Windows
要使用 IPMIVMView 来装载 ISO，请执行以下步骤。
1. 通过支持凭单，请求服务器将其虚拟 CD-ROM 作为第一个设备引导。每个设备都必须从其关联的虚拟 CD-ROM 进行引导。您可以在安装操作系统后还原此设置。
* 建立与 [VPN](http://www.softlayer.com/VPN-Access) 的 VPN 连接。如果使用的是 Microsoft Internet Explorer，请确保在“受信任的站点”列表中包含 .softlayer.com 和 .cloud.ibm.com，并使 JAVA 保持最新。
* 将 ISO 介质复制到 NAS 或 Windows CIFS 服务器。
  * 使用 SSH 连接到 Linux 跳板机。
  * 在 Linux 跳板机上装载 NAS 共享：

        mkdir /mnt/nasmount
        mount -t cifs //NAS_SERVER_NAME_ORIP/SLN#####-2 -o username=SLN#####-2,
        password=NAS_STORAGE_PW,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755 /mnt/nasmount
  * 装载命令参数键：
        NAS_SERVER_NAME_ORIP = NAS 存储器的名称或 IP。
        /SLN#####-2 = 用于连接到 NAS 存储器的用户名和文件夹名称。
        NAS_STORAGE_PW = NAS 存储器的密码。
        /mnt/nasmount = 用于装载 NAS 存储器的文件夹。
  * 将目录切换到新的 NAS 装载文件夹。
        cd /mnt/nasmount
  * 使用 wget 下载 iso 文件。
        wget http://www.linktoyouriso.com/isofilename.iso
  您将看到确认下载成功的消息。
* 下载 IPMIView，网址为：
      https://www.servethehome.com/download-supermicro-ipmiview-latest-version/
* 通过管理 IP 连接到服务器。
      <br>
      1. 连接到 `winadmin`。
      2. 打开 IPMIView 并转至**文件 > 新建 > 系统**。
      3. 使用硬件对象的 IPMI IP 地址来填写“服务器名称”和“IP 地址”字段。<br>
      4. 双击左侧具有相同 IP 地址的系统，输入 ADMIN 作为登录标识，并输入硬件对象的 IPMI 密码。
      5. 连接后，窗口中会提供许多选项卡。您可以使用**文本控制台**或 **KVM 控制台**来连接到服务器。

* 打开“虚拟介质”选项卡
* 填写 CD-ROM 映像连接详细信息。
  *
    * 共享主机 = NAS 存储器的 IP 地址。您可以通过对 NAS 存储服务器名称执行 ping 操作来查找此值。例如，`ping nas501.service.softlayer.com`
    * 共享名称 = NAS 存储器的用户名
    * 映像的路径 = ISO 文件的名称，格式如下：
          \NASusername\isoname.iso (i.e. \SLN123456\centos6.iso)
    * 用户 = NAS 存储器的用户名
    * 密码 = NAS 存储器的密码
* 重新引导服务器
* 打开 KVM 控制台视图
* 遵循系统提示来引导可引导的 ISO
* 安装操作系统
* 卸装虚拟介质
* 重新启动服务器

## 选项 3：从本地计算机装载 ISO
{: #bm-mount-iso-opt-3}

<a name="option3"></a>

您可以使用 Java iKVM 查看器（控制台）从本地计算机装载 ISO。这将支持您在连接到控制台时装载 ISO。根据因特网连接的上传速度和等待时间以及 Java 和计算机的性能，安装进展速度可能有所不同。

如果您无权更改服务器上的 BIOS，请向支持人员开具凭单以请求以下更改：
* 授予对 IPMI 的 root 用户管理员特权（能够更改“虚拟介质连接”方式）
* 将引导顺序更改为“IPMI 虚拟盘”作为第一个引导选项。（由于尚未装载 ISO，因此现在支持人员只应更改引导设备优先级。）


1. 通过将 Web 浏览器指向 cloud.ibm.com 中指定的 IP，登录到 IPMI 管理控制台。
* 单击“设备”>“您的服务器（设备详细信息）”>“远程管理”。指定用户名和密码。
* 单击“配置”>“远程会话”，然后将连接方式更改为**连接**。在某些较低版本的 IPMI 控制台中，此选项不可用，所以可以跳过此步骤。
* 单击“系统”>“系统信息”以返回到系统信息页面。您将看到控制台窗口图标。
* 单击“控制台”图标以打开控制台。接受所有安全警告。
* 控制台连接后，您将看到登录提示。
* 单击“虚拟介质”>“虚拟存储器”。
* 转至 **CDROM 和 ISO** 选项卡，然后选择**逻辑驱动器类型**下的“ISO 文件”。
* 单击**打开映像**，然后选择本地计算机上的 ISO。
* 单击**插入**以将 ISO 插入到虚拟 CD-ROM 驱动器。
* 单击**确定**。
* 重新引导服务器并使用**从虚拟 CD-ROM 驱动器引导**选项。您可能需要使用 iKVM 查看器中的虚拟键盘来选择引导设备。

## 故障诊断
{: #bm-mount-iso-troubleshooting}

* 并非所有用户都具有装载虚拟介质的缺省访问权。如果发生许可权错误，请联系支持人员更新 root IPMI 用户许可权。
* 如果已经装载 ISO，那么将显示一条错误消息，文本为**已装载有磁盘**。必须卸装现有磁盘并将其替换为新的 ISO。不能同时装载两个 ISO。
* 您可能需要联系支持人员来更改 BIOS 中的引导顺序。
* 装载 ISO 时，请使用 [SSL VPN](http://vpn.softlayer.com)，而不是 PPTP VPN。连接到该 VPN 网络后，还可以通过 IPMI 地址 (https://private-ip-IPMI-management) 访问系统的 IPMI。
* 输入 ISO 的路径时，请对该路径使用 UNC 名称语法（通用命名约定），例如：`\\<NAS username>\<isoname>.iso`
