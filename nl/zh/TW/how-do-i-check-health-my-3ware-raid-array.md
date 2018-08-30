---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 檢查 3ware RAID 陣列的性能

有了 3ware，您可以使用瀏覽器介面。不過，除非您在本端存取介面，否則可能會有安全風險。因此，請使用指令行介面。

<!--You can download the 3ware CLI utilities the software Library, located in the bottom of Customer Portal.  Please check http://downloads.service.softlayer.com for the latest version (VPN access required to access the downloads page). -->

**3ware CLI 工具的快速指令參考手冊**

這些裝置的後面必須接著識別要查詢哪些裝置的數字。

tw_cli /c0 show（輸出會顯示知道 RAID 陣列性能所需的資訊）

./tw_cli /c1 show

範例：

    Unit  UnitType  Status         %Cmpl  Stripe  Size(GB)  Cache  AVerify  IgnECC

    ------------------------------------------------------------------------------

    u0    RAID-5    OK             -      64K     465.641   OFF    OFF      OFF    

    Port   Status           Unit   Size        Blocks        Serial

    ---------------------------------------------------------------

    p0     OK               u0     233.76 GB   490234752     WD-WCANY1727093

    p1     OK               u0     233.76 GB   490234752     WD-WCANY1622544

    p2     OK               u0     233.76 GB   490234752     WD-WCANY1657267

    p3     NOT-PRESENT      -      -           -             -

*請注意下列項目：

c = 控制器<br/>
控制器可以是 0 或 1<br/>
u = 裝置<br/>
裝置號碼取決於數字陣列。在大部分情況下，它是 0。<br/>
p = 埠<br/>
埠表示埠號。在大部分情況下，它是 0-4。
