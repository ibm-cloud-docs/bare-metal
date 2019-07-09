---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-25"

keywords: bare metal, 3ware 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 检查 3ware RAID 阵列的运行状况
{: #bm-check-health-3ware-raid}

通过 3ware，可以使用浏览器界面。但是，除非您在本地访问该界面，否则可能会带来安全风险。因此，请使用命令行界面。

您可以从 [IBM Cloud CLI 插件存储库](https://plugins.cloud.ibm.com/ui/repository.html#cf-plugins) 下载 3ware CLI 实用程序。有关 CLI 实用程序的更多信息，请参阅 [cf CLI 的 VPN CLI 插件](https://cloud.ibm.com/docs/cli?topic=cloud-cli-vpn_cli_for_cf)。

**3ware CLI 工具的快速命令参考**

这些设备必须后跟标识所查询设备的编号。

tw_cli /c0 show（输出显示了解 RAID 阵列运行状况所需的信息）

./tw_cli /c1 show

示例：

    Unit  UnitType  Status         %Cmpl  Stripe  Size(GB)  Cache  AVerify  IgnECC

    ------------------------------------------------------------------------------

    u0    RAID-5    OK             -      64K     465.641   OFF    OFF      OFF    

    Port   Status           Unit   Size        Blocks        Serial

    ---------------------------------------------------------------

    p0     OK               u0     233.76 GB   490234752     WD-WCANY1727093

    p1     OK               u0     233.76 GB   490234752     WD-WCANY1622544

    p2     OK               u0     233.76 GB   490234752     WD-WCANY1657267

    p3     NOT-PRESENT      -      -           -             -

*注意以下各项：

c = controller<br/>
控制器可以为 0 或 1<br/>
u = unit<br/>
单元号取决于数字数组。大多数情况下为 0。<br/> p = port<br/>
port 表示端口号。大多数情况下为 0-4。
