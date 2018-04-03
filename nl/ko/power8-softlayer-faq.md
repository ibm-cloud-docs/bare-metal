---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}}의 POWER8 - FAQ

|1.|오퍼링 세부사항||
|---|---|---|
|1.1|다음 경우에 발생하는 사항|<ul><li>SoftLayer가 POWER8 기반의 베어메탈 시스템을 포함하도록 오퍼링을 확장했습니다. 이러한 시스템은 데이터, 코그너티브 및 웹 워크로드를 Linux에 클라우드 기반으로 배치할 수 있도록 특별히 조정된 IBM의 새 POWER8 프로세서 및 OpenPOWER 기반의 플랫폼을 사용하여 빌드됩니다.</li><li>서비스로서의 가상 머신이 베타 테스트되어 가까운 미래에 제공될 것으로 기대됩니다.</li></ul>|
|1.2|OpenPOWER의 개념 및 고려해야 하는 이유|<ul><li>OpenPOWER 기반의 서버는 데이터 집중적인 워크로드용으로 디자인된 유일한 프로세서인 POWER8 아키텍처에 빌드되는 개방형의 강력하고 사용자 정의할 수 있는 시스템의 새 기종입니다.</li><li>OPF(OpenPOWER Foundation)는 2013년 8월에 커다란 아이디어를 가진 다섯 회사의 컨소시엄으로 소박하게 시작하여, 개방형 개발에 사용 가능한 POWER 하드웨어 및 소프트웨어를 만들어 기술 및 혁신에 대한 새로운 접근법을 사용 가능하게 했고, 플랫폼에서 혁신가들의 생태계를 확장할 수 있도록 업계 차원의 연합을 구축했습니다. OPF는 짧은 시간 내에 190명이 넘는 참가자가 생길 만큼 성장했습니다. 이러한 빠른 성장은 "데이터 센터에 대한 새로운 생각"을 위한 노력에 대해 업계 전반에서 보여주는 기대감을 반영합니다.</li><li>OpenPOWER 플랫폼은 POWER8의 기능 및 혁신적인 결과를 OpenPOWER 간의 개방적 협업에서 SoftLayer 퍼블릭 클라우드로 가져올 것입니다.</li></ul>|
|1.3|SoftLayer에서 POWER8 플랫폼의 장점은 무엇입니까?|<ul><li>POWER8은 데이터 워크로드에 최적화된 아키텍처가 있는 전통적인 클라우드 플랫폼에 고유 대안을 제공합니다. 성능 테스트는 데이터 워크로드에 대한 유사한 x86 시스템에 대해 평균 두 배 이상의 성능을 보여줍니다. POWER8에 표시된 벤치마킹 테스트는 다음 결과를 제공합니다.<ul><li>DB2(BLU 사용)에 대해 시간당 1.76x 많은 조회, 쿼리당 20% 저렴한 비용.</li><li>클라우드에서 POWER8에 대한 DB2(BLU 가속화 사용)는 동일한 시간 동안 43% 빠른 코그너티브 통찰 및 65% 더 많은 통찰.</li><li>데이터 분류 및 예상 분석에서 Spark 기계 학습에 대해 64% 뛰어난 성능.</li><li>빅데이터 클러스터에서 널리 사용되는 Spark SQL 처리에 대해 66% 더 빠른 속도.</li><li>Spark 그래프 워크로드를 기반으로 할 때 완전한 소셜 연결 및 제품 추천이 83% 빨라짐.</li></ul></li></ul>|
|1.4|오퍼링의 세부사항은 무엇입니까?|<ul><li>POWER8 시스템의 첫 번째 단계는 월별 대여로 사용 가능하며 Ubuntu OS가 설치된 베어메탈 배치의 네 가지 고정된 구성(소형, 중형, 대형 및 SSD가 포함된 대형)을 포함합니다.</li><li>오퍼링은 표준 SoftLayer API 지원 및 스토리지, 네트워킹 및 방화벽과 같은 대부분의 보조 서비스 오퍼링을 포함합니다.</li><li>POWER8 시스템은 초기에는 DAL09 데이터 센터에 있었으며 2016년 이후에 기타 지역으로 확장될 것입니다.</li></ul>|
|||![POWER8 C81](images/power8_fig1.png)<br /><br />![POWER8 그림 2](images/power8_fig2.png)|
||||
|1.5|이름은 무엇을 의미합니까?|새 POWER8 이름 형식은 C812L입니다. 여기서,<ul><li>"C" = 클라우드</li><li>"8" = POWER8</li><li>"1" = 코어 수</li><li>"2" = 2U</li><li>"L"= Linux를 의미합니다.</li></ul>|
|1.6|지원되는 운영 체제는 무엇입니까? AIX 또는 IBM i를 실행할 수 있습니까?|<ul><li>SoftLayer는 초기에는 Ubuntu Linux 14.04 LTS 운영 체제를 제공할 것이며 이후에 기타 Linux 배포를 추가할 것입니다.</li><li>이러한 시스템에서는 AIX 또는 IBM i를 실행할 수 없습니다. 서비스로서의 AIX는 IBM의 클라우드 관리 서비스에서 사용 가능하며 호스트되는 IBM i는 수많은 당사의 글로벌 비즈니스 파트너를 통해 사용 가능합니다.</li></ul>|
||AIX 또는 IBM i 운영 체제가 있는 시스템을 대여할 수 있습니까?|<ul<li>IBM은 IBM의 클라우드 관리 서비스 및 기타 파트너를 통해 클라우드에서 계속 AIX를 제공할 것입니다. IBM i 기반의 클라우드 서비스 또한 수많은 MSP 파트너를 통해 사용할 수 있습니다.</li></ul>|
|**2.**|**시장 진입**||
|2.1|누가 POWER8을 사용할 때 혜택을 받을 수 있습니까?|<ul><li>SoftLayer의 POWER8 오퍼링의 초기 스위트는 하이브리드 클라우드 솔루션용 기존 시스템의 가치를 높이고자 하는 기존 Power 고객에게 적합합니다.</li><li>데이터 워크로드에 최적화된 이러한 시스템은 클라우드에서 개발/테스트용으로 쉽게 활용될 수 있으며 전원의 성능 장점을 검증하기 위한 신속한 POC를 제공하며 POWER 또는 <a href="https://www-304.ibm.com/partnerworld/wps/servlet/ContentHandler/stg_com_sys_power-development-platform">Power Developer Cloud</a> 및 <a href="https://www-304.ibm.com/webapp/set2/sas/f/lopdiags/sdklop.html">SDK for Linux on Power</a>로 <a href="https://www.ibm.com/developerworks/library/l-port-linux-on-x86-application/">애플리케이션을 쉽게 이식</a>합니다.</li><li>SoftLayer 클라우드의 POWER8은 사설 및 퍼블릭 클라우드 자원 둘 다를 활용하는 통합 애플리케이션을 지원하는 데도 사용될 수 있습니다.</li><li>POWER8 베어메탈 시스템은 유전체학, 재무 또는 코그너티브 서비스 등의 새로운 애플리케이션에 대해서도 우수한 호스팅 플랫폼이 될 수 있습니다.</li></ul>|
|2.2|가장 일반적인 유스 케이스는 무엇입니까?|<ul><li>DB2(BLU 사용), Cognos 또는 WebSphere와 같은, Ubuntu OS에서 실행되는 데이터 및 분석 집중적인 워크로드입니다.</li><li>Apache Spark, MariaDB 등의 오픈 소스 애플리케이션 및 e-commerce 또는 컨텐츠 관리 시스템 등의 LAMP 사용 가능 애플리케이션입니다.</li><li>Linux on Power 워크로드에 대한 개발/테스트, 이식 및 조정입니다.</li><li>경쟁 제품인 UNIX 워크로드 및 기타 애플리케이션 스택에 대한 개념 증명입니다.</li></ul>|
|2.3|고객에 대한 혜택은 무엇입니까?|<ul><li>POWER8은 데이터용으로 디자인된 유일한 프로세서이며 IBM Power Systems 서버 라인의 상단에 위치합니다. {{site.data.keywords_baremetal_short}}는 클라우드에서 부담이 큰 데이터 집중적인 코그너티브 워크로드를 실행하고자 하는 비즈니스에 이상적입니다.</li><li>데이터 및 분석 워크로드의 경우, POWER8의 증가된 스레드, 메모리 대역폭 및 속도가 유사한 x86 기반의 시스템에 비해 더 많은 처리량 및 성능을 제공할 수 있습니다.</li></ul>|
|2.4|POWER8 {{site.data.keywords_baremetal_short}}를 어떻게 주문합니까?|<ul><li>서비스로서의 POWER8 베어메탈은 기타 SoftLayer 서비스와 같이 카탈로그에서 이용 가능하며 주문할 수 있습니다.</li><li>또한 POWER8 베어메탈은 IBM 및 BP 판매자에 의한 모든 IBM Cloud 계약에 작성된 표준 IBM Cloud 오퍼링으로 사용 가능합니다.</li></ul>|
|2.5|POWER8 시스템은 어떤 방법으로 가격이 책정됩니까?|<ul><li>POWER8 베어메탈 시스템은 제공되는 성능을 기반으로 하여 유사한 x86 시스템을 기준으로 가격이 측정됩니다.</li><li><strong>소형:</strong> 8 코어, 64GB RAM, 1x1TB SATA, 10 Gbps, 이중 전원입니다.</li><li><strong>중형:</strong> 10 코어, 256GB RAM, 2x4TB SATA, 10 Gbps, 이중 전원입니다.</li><li><strong>대형:</strong> 10 코어, 512GB RAM, 2x6TB SATA, 10 Gbps, 이중 전원입니다.</li><li><strong>대형/SSD:</strong> 10 코어, 256GB RAM, 2x960 SSD, 10 Gbps, 이중 전원입니다.</li></ul>|
|**3.**|**SoftLayer에서 Power 구현**|||
|3.1|계층 애플리케이션 환경에 대해 SoftLayer에서 인접한 x86 플랫폼에 이러한 새 POWER8 시스템을 연결할 수 있습니까?|<ul><li>예. 이러한 시스템은 기타 SoftLayer 오퍼링과 Power 및 x86 기술이 둘 다 필요한 계층 애플리케이션 환경에 대한 애플리케이션에 인접하게 구성될 수 있습니다.</li></ul>|
|3.2|운영 체제 없이 POWER8 시스템을 프로비저닝 할 수 있습니까?|<ul><li>"OS 없음"을 실행하기 위한 옵션은 지금 사용할 수 없습니다.</li></ul>|
|3.3|RHEL 또는 SUSE 등의 Linux 운영 체제를 가져올 수 있습니까?|<ul><li>예. 그러나 이러한 구성은 지원되거나 검증되지 않습니다. 고객은 소프트웨어 공급업체에 대한 라이센스 관리, 패치, 로열티 및 유지보수의 책임이 있습니다. SoftLayer는 하드웨어를 계속 지원할 것이며, 하드웨어에 문제가 있는 경우 고객에게 하드웨어 고장과 관련된 syslog 및 오류 메시지를 얻을 수 있는 액세스 권한을 요구할 수 있습니다.</li></ul>|
|3.4|POWER8 아키텍처에서 언제 가상 머신(VMaaS)을 사용할 수 있습니까?|<ul><li>POWER8에서 VMaaS는 일반적으로 2016년 후반부에 사용 가능하게 될 예정입니다.</li></ul>|
|3.5|POWER8에 대해 사용 가능한 자동화 및 프로비저닝 도구는 무엇입니까?|<ul><li>Canonical의 JuJu Charms가 Ubuntu OS에 대한 배치를 자동화할 수 있습니다. Ubuntu에서 수많은 IBM 및 오픈 소스 패키지의 배치를 자동화하기 위해 사용할 수 있는 사전 빌드된 패키지가 많이 있습니다. Canonical의 <a href="https://jujucharms.com/store">JuJu Charm Store</a>에서 사용 가능합니다.</li></ul>|
|3.6|빠른 프로비저닝을 위해 디자인된 이러한 시스템을 업그레이드할 수 있습니까? 또한 미래에 구성 가능한 베어메탈을 제공할 계획이 있습니까?|<ul><li>SoftLayer는 향후 구성 옵션, 추가 기능 서비스, 운영 체제 선택 및 시간별 가격 책정을 추가할 예정입니다.</li></ul>|
|**4.**|**향후 방향 및 추가 정보**||
|4.1|이러한 새 POWER8 시스템과 함께 사용 가능한 추가 데이터 센터 인프라 및 서비스는 무엇입니까?|<ul><li>SoftLayer는 몇 가지 예외(eVault 및 소프트웨어 기반의 방화벽)만 제외하고 현재 x86에 대해 제공되는 것과 동일한 POWER8 시스템용 데이터 센터 옵션을 제공할 것입니다.</li><li>SoftLayer는 추가 구성 및 스토리지 옵션, 운영 체제, 기타 데이터 센터로의 확장, GPU 및 오퍼링의 선택사항 및 기능을 개선하기 위한 기타 오퍼링을 포함하여 시간 경과에 따라 계속 POWER8 구성 및 오퍼링을 확장할 것입니다. </li></ul>|
