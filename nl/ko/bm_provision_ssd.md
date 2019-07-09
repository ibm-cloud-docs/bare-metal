---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-02"

keywords: provision Intel Optane compatible bare metal server, Intel Optane, optane 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Intel Optane 호환 가능 Bare Metal Server 프로비저닝
{: #bm-provision-optane-server}

Intel Optane 드라이브를 사용하여 Bare Metal Server를 프로비저닝하려면 다음을 수행하십시오.
1. 다음 프로시저를 사용하십시오. [사용자 정의 Bare Metal Server 빌드](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server).
* 주문 양식에서 다음 옵션을 선택하십시오.

|섹션|선택 옵션
|------|------|
|지역-데이터 센터|Intel Optane 드라이브를 사용하려면 다음 데이터 센터 중 하나를 선택하십시오.<br>유럽 - AMS03, FRA02, LON02, OSL01<br>NA 남부 DAL09, DAL10, DAL12<br>아시아 태평양 - MEL01<br>NA 동부 - MON01, TOR01, WDC04<br>NA 서부 - SJC03<br>|
|서버|1. **모든 서버** 선택<br>2. *듀얼 프로세서* 선택<br>3. 다음 서버 중 하나 선택<br>-Intel Xeon 4110(최대 12개 드라이브 포함)<br>-Intel Xeon 5120(최대 12개 드라이브 포함)<br>-Intel Xeon 6140(최대 12개 드라이브 포함)<br>-Intel Xeon E5-2620 v4)(GPU 지원 제공)<br>-Intel Xeon E5-2650 v4(GPU 지원 제공)<br>-Intel Xeon E5-2690 v4(GPU 지원 제공)<br><br>  **참고**: E5-2620 v4, E5-2650 v4 또는 E5-2650 v4를 선택하는 경우 Intel Optane 드라이브에서 GPU를 교체하므로, GPU와 Intel Optane 드라이브가 둘 다 있을 수 없습니다.|
|운영 체제|Intel에서 제공하는 Optane 드라이버의 경우 Intel에서 다음 운영 체제가 인증됩니다.<br>Windows Server 2016(모든 에디션)<br>Windows Server 2012 R2(모든 에디션)<br><br>작업함, 오픈 소스, 비Intel 드라이버의 경우 호환성과 기능의 유효성을 검증하지만 인증되지는 않습니다.<br>Red Hat Enterprise Linux 7.x(64비트)<br>Red Hat Enterprise Linux 6.x(64비트).
|이미지 추가 기능| 첫 번째와 두 번째 PCIe 컴포넌트 중 하나 또는 둘 다의 Intel Optane 드라이브를 선택하십시오.|
