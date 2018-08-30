---



copyright:
  years: 2017, 2018
lastupdated: "2018-07-06"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Bare Metal Server 빌드
{: #ordering-baremetal-server}

다음 단계를 사용하여 사용자 정의 {{site.data.keyword.baremetal_short}}를 빌드하십시오.

1. [{{site.data.keyword.cloud_notm}} 카탈로그](https://console.bluemix.net/catalog/){:target="_blank"}를 여십시오.   
2. Bare Metal Server를 선택하십시오.
3. 작성을 클릭하십시오.
4. 서버 목록 아래에서 다음 문장을 찾으십시오. **다른 구성 옵션에 관심이 있으십니까? 여기를 클릭하십시오**. 이 옵션을 선택하십시오. 사용자 정의 서버 양식이 표시됩니다.
1. 서버의 데이터 센터 위치를 선택하십시오.
* **시작 단가** 링크를 클릭하여 세 개의 서버 카테고리에서 서버를 선택하십시오.
  * SAP 인증 서버(SAP 인증 서버를 프로비저닝하는 데 관한 자세한 정보는 [{{site.data.keyword.cloud_notm}}SAP Certified Infrastructure](/docs/bare-metal/bare-metal-sap-applications.html) 참조)
  * 단일 프로세서 멀티코어 서버
  * 듀얼 프로세서 멀티코어 서버

* 구성 옵션에서 선택하십시오. **데이터 센터**, **RAM** 및 **운영 체제**는 필수 필드입니다. 다른 모든 필드는 선택사항입니다. 선택사항 필드에 대한 자세한 정보는 **[추가 서버 구성 옵션](#addl-server-options)**을 참조하십시오.

    **참고**: 서버와 운영 체제 간에 충돌이 있으면 오류 메시지가 표시됩니다. 예를 들어 Microsoft SQL Server에서 Linux 선택합니다.* **주문에 추가**를 클릭하십시오. 체크아웃 페이지가 표시됩니다.

  체크아웃 페이지에서 재구성 옵션 중 하나를 클릭하여 구성 페이지로 돌아갈 수 있습니다.
* 고급 시스템 구성 섹션에서 추가 구성 옵션을 지정하십시오. 자세한 정보는 **[고급 시스템 구성](#adv-system-config)**을 참조하십시오.

*   **클라우드 서비스 이용 약관** 및 **써드파티 서비스 계약** 선택란을 클릭하십시오.
*   지불 정보를 확인하거나 입력하고 **주문 제출**을 클릭하십시오. 프로비저닝 주문 번호가 있는 화면으로 경로가 재지정됩니다. 화면이 프로비저닝 주문 영수증이기도 하므로 해당 화면을 인쇄할 수 있습니다.

  **견적으로 저장**을 클릭하여 구매하지 않고 이 주문을 저장할 수도 있습니다.

 프로비저닝 주문 수신확인, 프로비저닝 주문 승인 및 처리, 프로비저닝 완료 등 일련의 이메일이 관리자에게 전송됩니다. 프로비저닝 완료 이메일에는 {{site.data.keyword.cloud_notm}}에 로그인한 후의 *디바이스 세부사항* 페이지의 링크가 포함됩니다. 또한 {{site.data.keyword.slportal}}에 직접 로그인할 수 있습니다.

 ## 추가 서버 구성 선택사항
 {: #addl-server-options}

 Bare Metal Server를 프로비저닝할 때 사용할 수 있는 추가 옵션이 있습니다(예: 공용 대역폭, 업링크 포트 속도, 공용 2차 IP 주소 등). 표 1에는 추가 옵션이 설명되어 있습니다.


 |**필드** |**설명** |
 |-------------------|---------------|
 |서버 보안|예: Intel TXT(Trusted Execution Technology)|
 |Software Guard Extensions|중요한 코드와 데이터의 보안 강화(Intel SGX)<br><br>[Intel SGX로 Bare Metal Server 프로비저닝](../bare-metal/bare-metal-provision-SGX.html).|
 |RAM|서버 요구사항에 맞는 RAM 레벨을 선택하십시오.|
 |운영 체제 |CentOS, FreeBSD, Microsoft, Red Hat, Ubuntu 또는 기타에서 선택하십시오.|
 |하드 드라이브 |선택한 OS에 따라 필드를 미리 채워 하드 디스크를 설정하는 데 사용자 인터페이스의 도구를 사용하십시오.<br><br> Intel Optane SSD 드라이브를 사용하도록 선택할 수도 있습니다. [Intel Optane SSD DC P4800X 프로비저닝](../bare-metal/bm-provision_ssd.html)을 참조하십시오.
 |퍼블릭 대역폭 |한 달 동안 공용 인터페이스를 통해 전송할 수 있는 데이터의 양을 결정합니다. 테스트 환경의 경우 이 인터페이스를 통해 전송할 설치 데이터가 필요하며, 값은 초기에 전송된 데이터의 양을 초과하도록 적용되어야 합니다. {{site.data.keyword.cloud_notm}} 데이터 센터 중 하나에 초기 데이터를 로드하기 위해 [{{site.data.keyword.cloud_notm}} 컨텐츠 전송 네트워크](https://www.ibm.com/cloud/cdn)를 고려하십시오. 모든 {{site.data.keyword.baremetal_short}}는 무제한 대역폭을 포함하도록 업그레이드될 수 있습니다. 모든 무제한 디바이스는 사설 전용 포트에 있습니다.|
 |업링크 포트 속도 |내부 및 외부 인터페이스의 속도를 결정합니다. |
 |퍼블릭 보조 IP 주소 |서버에 추가 IP 주소를 지정합니다. 시나리오에 따라 서버에 할당된 IP 주소가 필요할 수 있습니다. 추가 IPv4 주소는 1, 2, 4, 8, 16 또는 32개 단위로 제공됩니다. |
 |기본 IPv6 주소 |서버의 외부 및 내부 인터페이스에 지정됩니다. |
 |퍼블릭 정적 IPv6 주소 |/64 블록에서 추가 IPv6 주소를 지정합니다. |
 |운영 체제 추가 기능|VMware, 백업 솔루션, 제어판, 데이터베이스, Hardware & Software Firewalls, 안티바이러스 및 스파이웨어 보호, 침입 감지 및 보호와 같은 옵션을 선택하십시오. <br><br>이러한 옵션의 세부사항에 대해 논의할 수 있도록 기업 보안 부서와 {{site.data.keyword.cloud_notm}} 지원 팀의 협업을 강력히 권장합니다.  |Evault |서버 간의 백업을 복제하기 위해 서버에 설치될 수 있는 에이전트 기반의 백업 도구입니다. |
 |서비스 추가 기능|모니터링, 자동화된 응답 및 보험과 같은 서비스 추가 기능을 선택하십시오.|
 {: caption="표 1. 추가 서버 옵션" caption-side="top"}

## 고급 시스템 구성
{: #adv-system-config}

**고급 시스템 구성**의 필드를 입력하면 프로비저닝 프로세스가 완료됩니다.

|**필드** |**설명** |
|---|---|
|호스트 이름 |서버의 영구적 또는 임시 이름입니다(예: _server1_). **참고**: SAP 인증 서버를 프로비저닝하는 경우 SAP 호스트 이름은 최대 13자의 영숫자 문자로 구성되어야 합니다. SAP 호스트 이름에 대한 자세한 정보는 [SAP 참고 611361](https://launchpad.support.sap.com/#/notes/2611361) 및 [129997](https://launchpad.support.sap.com/#/notes/129997)을 참조하십시오. SAP S-사용자 ID를 관리합니다. |
|도메인 |인터넷 도메인 이름과 충돌하지 않아야 하는 하위 도메인 이름입니다(예: _test.acme.com_). |
|VLAN 선택 |이미 하나 이상의 서버를 주문하였기 때문에, 계정 아래에 VLAN이 있는 경우 해당 VLAN에 새 서버를 추가할 수 있습니다. |
|프로비저닝 스크립트 |프로비저닝 후에 특정 단계를 자동화할 수 있는 스크립트를 제공할 수 있습니다. |
|SSH 키 |SSH 키에 대한 퍼블릭 키를 제공할 수 있습니다. 프로비저닝된 후에는 이를 사용하여 서버에 로그인할 수 있습니다.|
{: caption="표 2. 고급 시스템 구성" caption-side="top"}

 자세한 정보는 {{site.data.keyword.cloud_notm}} 지원을 참조하십시오.

 **참고:** 컴퓨팅 디바이스가 포함된 2차 서브넷을 주문할 수 있습니다. 그러나 2차 서브넷을 주문하면 컴퓨팅 디바이스를 재확보할 때 해당 서브넷이 재확보됩니다. 2차 서브넷을 개별적으로 주문하면(컴퓨팅 주문의 추가 기능 옵션으로 주문하지 않음) 명시적으로 취소할 때까지 서브넷을 보유할 수 있습니다. 컴퓨팅 디바이스를 재확보하는 경우 IP 주소를 의도치 않게 유실하지 않도록 이와 같이 구분하는 것이 중요합니다.

## 다음 단계
{{site.data.keyword.baremetal_short}}가 프로비저닝된 후에 관리를 시작할 수 있습니다. 자세한 정보는 [{{site.data.keyword.baremetal_short}} 관리](../bare-metal/managing.html)를 참조하십시오.
