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

# 3ware RAID 어레이의 상태 확인
{: #bm-check-health-3ware-raid}

3ware를 사용하여 브라우저 인터페이스를 사용할 수 있습니다. 그러나 로컬로 인터페이스에 액세스하지 않으면 보안 위험이 있을 수 있습니다. 따라서 명령행 인터페이스를 사용합니다.

[IBM Cloud CLI 플러그인 저장소](https://plugins.cloud.ibm.com/ui/repository.html#cf-plugins)에서 3ware CLI 유틸리티를 다운로드할 수 있습니다. CLI 유틸리티에 대한 자세한 정보는 [CLI용 VPN CLI 플러그인](https://cloud.ibm.com/docs/cli?topic=cloud-cli-vpn_cli_for_cf)을 참조하십시오.

**3ware CLI 도구에 대한 빠른 명령 참조**

해당 디바이스 다음에는 조회되는 디바이스를 표시하는 번호가 와야 합니다.

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

c = 제어기<br/>
제어기는 0 또는 1일 수 있음<br/>
u = 장치<br/>
장치 번호는 어레이 수에 따라 다릅니다. 대부분의 경우, 0입니다.<br/>
p = 포트<br/>
포트는 포트 번호를 표시합니다. 대부분의 경우, 0-4입니다.
