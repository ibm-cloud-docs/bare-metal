---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 在裸机服务器上安装 Ubuntu 服务器

如果要使用非 {{site.data.keyword.IBM&reg; Cloud}} 提供的操作系统，那么可以通过装载定制 ISO（磁盘映像）将其安装到裸机服务器上。要装载 ISO，请将其上传到与服务器关联的文件存储器 (NAS)。要将 ISO 上传到 NAS，请使用以下过程通过 IPMI 装载 ISO。
1. 使用**无操作系统**来订购裸机服务器 
* 您还可以选择免费操作系统（例如 CentOS）作为可用于连接到 NAS 的操作系统。
* 订购 NAS 存储器以存储可引导 ISO。如果已经具有任何 Windows CIFS 服务器，那么可以将其用于共享 ISO 映像。使用此 Windows CIFS 服务器，您将获得具有 20 GB 容量的旧 NAS。供应 NAS 之后，可以在客户门户网站中查看 NAS 的描述。
* 从 https://www.ubuntu.com/download/server 下载 ISO 映像。
* 将 ISO 映像上传到 NAS 或 Windows CIFS 服务器。如果您具有 NAS 存储器，那么可以使用 FTP 来上传 ISO 映像文件。

  样本 FTP 过程：
  ```
  #ftp <nas address>.service.softlayer.com
  已连接到 <nas address>.service.softlayer.com
  220 NAS FTP 服务
  用户 (<nas address>.service.softlayer.com:(none))：<nas username>
  331 请指定密码。
  密码：<nas password>
  230 登录成功。
  ftp> bin
  200 正在切换到二进制方式
  ftp> put <iso imagefile name>.iso
  200 PORT 命令成功。请考虑使用 PASV。
  150 正常发送数据。
  226 传输完成。
  ftp：已发送 3170893824 字节，用时 253.86 秒，速率 12490.77 千字节/秒
  ```
  
* 使用 IPMI 与 {{site.data.keyword.Bluemix_notm}} 建立 VPN 连接。您可以从“支持”菜单或通过以下 URL 启动 VPN 菜单：[VPN Access](http://www.softlayer.com/VPN-Access)
* 通过 IPMI 的“虚拟介质”菜单，使用“通过管理 IP 连接到 IPMI”装载 ISO 映像。
  1. 查看 IPMI 凭证
  * 登录到 IPMIView
  * 打开“虚拟介质”选项卡
  * 您需要是 root 用户并具有对 IPMI 的“管理员”特权。如果特权显示为*操作员*，请开具支持凭单以请求将特权更改为“管理员”。
  * 填充 ISO 映像连接详细信息
    共享主机 = NAS 的 IP 地址<br/示例：10.3.x.x
    映像的路径 = ISO 文件的名称，格式如下：\NASusername\imagefilesname.iso（例如：
\SLNxxxxxx\SLE-12-SP1-Server-DVD-x86_64-GM-DVD1.iso）
    用户 = NAS 的用户名
    密码 = NAS 的密码
  * 单击**装载**按钮
  * 确认设备
* 单击并启动 KVM 查看器，然后从“虚拟介质”菜单中打开“虚拟存储器”页面。如果已成功将 ISO 映像装载为 CDROM 设备，那么会在**连接状态历史记录**中看到该设备描述。
* 通过 SoftLayer 凭单请求服务器将虚拟 CD-ROM 作为第一个设备引导。对每台服务器完成此请求。安装操作系统之后可更改此引导设置。
  **注**：您不一定需要联系支持人员来更改 BIOS 中的引导顺序。这取决于您的服务器。请尝试重新引导一次，以确认引导顺序。
* 通过 KVM 视图重新引导服务器。
* 通过装载的 ISO 映像安装操作系统。
* 通过 ISO 将 Ubuntu 操作系统安装到裸机服务器。
* 配置网络设置（IP 地址/子网/网关/DNS 等）。如果未在安装步骤中正确配置这些设置，那么只能在重新引导后通过 KVM 控制台连接到此服务器。

* 卸装虚拟介质。您应该通过 IPMI 的“虚拟介质”选项卡从服务器中卸装虚拟介质。
* 重新引导服务器。
* 重新引导后，可以通过 SSH 访问服务器。
