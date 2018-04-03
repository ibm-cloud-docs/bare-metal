---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 3ware RAID 어레이의 상태 확인

3ware를 사용하면 브라우저 인터페이스를 사용할 수 있습니다. 하지만 인터페이스에 로컬로 액세스하지 않으면 보안 위험이 있을 수 있습니다. 따라서 명령행 인터페이스를 사용하도록 권장합니다.

<!--You can download the 3ware CLI utilities the software Library, located in the bottom of Customer Portal.  Please check http://downloads.service.softlayer.com for the latest version (VPN access required to access the downloads page). -->

**3ware CLI 도구에 대한 빠른 명령 참조**

해당 디바이스 뒤에는 조회되는 대상을 표시하는 번호가 와야 합니다.

tw_cli /c0 show(출력에 RAID 어레이의 상태를 파악하는 데 필요한 정보가 표시됨)

./tw_cli /c1 show

예:

    Unit  UnitType  Status         %Cmpl  Stripe  Size(GB)  Cache  AVerify  IgnECC

    ------------------------------------------------------------------------------

    u0    RAID-5    OK             -      64K     465.641   OFF    OFF      OFF    

    Port   Status           Unit   Size        Blocks        Serial

    ---------------------------------------------------------------

    p0     OK               u0     233.76 GB   490234752     WD-WCANY1727093

    p1     OK               u0     233.76 GB   490234752     WD-WCANY1622544

    p2     OK               u0     233.76 GB   490234752     WD-WCANY1657267

    p3     NOT-PRESENT      -      -           -             -

*다음을 참고하십시오.

c = 컨트롤러<br/>
컨트롤러는 0 또는 1일 수 있습니다.<br/>
u = 장치<br/>
장치 번호는 어레이 번호에 따라 다릅니다. 대부분의 경우, 0입니다.<br/>
p = 포트<br/>
포트는 포트 번호를 표시합니다. 대부분의 경우, 0-4입니다.
