---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 检查 3ware RAID 阵列的运行状况

通过 3ware，可以使用浏览器界面。但是，除非您在本地访问该界面，否则可能会带来安全风险。因此，请使用命令行界面。

<!--You can download the 3ware CLI utilities the software Library, located in the bottom of Customer Portal.  Please check http://downloads.service.softlayer.com for the latest version (VPN access required to access the downloads page). -->

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

c = 控制器<br/>
控制器可以为 0 或 1<br/>
u = 单元<br/>
单元号取决于阵列数。大多数情况下为 0。<br/>
p = 端口<br/>
端口表示为端口号。大多数情况下为 0-4。
