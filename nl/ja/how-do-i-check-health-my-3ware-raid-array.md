---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 3ware RAID アレイの正常性の確認

3ware の場合、ブラウザー・インターフェースを使用できます。ただし、このインターフェースにはローカルからアクセスしない限り、セキュリティー・リスクになる可能性があります。そのため、コマンド・ライン・インターフェースを使用します。

<!--You can download the 3ware CLI utilities the software Library, located in the bottom of Customer Portal.  Please check http://downloads.service.softlayer.com for the latest version (VPN access required to access the downloads page). -->

**3ware CLI ツールのクイック・コマンド・リファレンス**

デバイスの後に、照会対象のデバイスを示す番号を続ける必要があります。

tw_cli /c0 show (出力では、RAID アレイの正常性を把握するために必要な情報が示されます)

./tw_cli /c1 show

例:

    Unit  UnitType  Status         %Cmpl  Stripe  Size(GB)  Cache  AVerify  IgnECC

    ------------------------------------------------------------------------------

    u0    RAID-5    OK             -      64K     465.641   OFF    OFF      OFF    

    Port   Status           Unit   Size        Blocks        Serial

    ---------------------------------------------------------------

    p0     OK               u0     233.76 GB   490234752     WD-WCANY1727093

    p1     OK               u0     233.76 GB   490234752     WD-WCANY1622544

    p2     OK               u0     233.76 GB   490234752     WD-WCANY1657267

    p3     NOT-PRESENT      -      -           -             -

*以下の点に注意してください。

c = コントローラー<br/>
コントローラーは 0 または 1 です<br/>
u = ユニット<br/>
ユニット番号は、アレイの数によって異なります。 ほとんどの場合、0 です。<br/>
p = ポート<br/>
ポートは、ポート番号を示します。 ほとんどの場合、0 から 4 です。
