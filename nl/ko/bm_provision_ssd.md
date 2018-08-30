---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Intel Optane 호환 가능 Bare Metal Server 프로비저닝
Intel Optane 드라이브를 사용하여 Bare Metal Server를 프로비저닝하려면 다음을 수행하십시오.
1. 다음 프로시저를 사용하십시오. [사용자 정의 Bare Metal Server 빌드](../bare-metal/baremetal-provision.html).
* 주문 양식에서 다음 옵션을 선택하십시오.

|섹션|선택 옵션
|------|------|
|데이터 센터|Intel Optane 드라이브를 사용하려면 다음 데이터 센터 중 하나를 선택하십시오. <br>AMS03 - Amsterdam<br>DAL09 - Dallas<br>DAL10 - Dallas<br>DAL12 - Dallas<br>FRA02 - Frankfurt<br>LON02 - London<br>MEL01 - Melbourne<br>MON01 - Montreal<br>OSL01 - Oslo<br>SJC03 - San Jose<br>TOR01 - Toronto<br>WDC04 - Washington, DC|
|서버|다음 서버는 Intel Optane 드라이브와 호환 가능합니다.<br>최대 12개의 드라이브가 있는 Intel Xeon 4110<br>최대 12개의 드라이브가 있는 Intel Xeon 5120<br>최대 12개의 드라이브가 있는 Intel Xeon 6140<br>GPU를 지원하는 Intel Xeon E5-2620 v4<br>GPU를 지원하는 Intel Xeon E5-2650 v4<br>GPU를 지원하는 Intel Xeon E5-2690 v4<br><br>  **참고**: E5-2620 v4, E5-2650 v4 또는 E5-2650 v4를 선택하는 경우 Intel Optane 드라이브에서 GPU를 교체하므로, GPU와 Intel Optane 드라이브가 둘 다 있을 수 없습니다.|
|PCIe 컴포넌트| 첫 번째와 두 번째 PCIe 컴포넌트 중 하나 또는 둘 다의 Intel Optane 드라이브를 선택하십시오.|
|운영 체제|Intel에서 제공하는 Optane 드라이버의 경우 Intel에서 다음 운영 체제가 인증됩니다.<br>Windows Server 2016(모든 에디션)<br>Windows Server 2012 R2(모든 에디션)<br><br>작업함, 오픈 소스, 비Intel 드라이버의 경우 호환성과 기능의 유효성을 검증하지만 인증되지는 않습니다.<br>Red Hat Enterprise Linux 7.x(64비트)<br>Red Hat Enterprise Linux 6.x(64비트).
