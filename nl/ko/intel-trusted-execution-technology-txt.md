---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 하드웨어 모니터링 및 보안 제어

악성 위협의 확산 및 치밀함으로 인해 더 엄격한 보안 요구사항을 채택하고 실행 환경의 모든 면을 면밀히 관찰해야 할 필요성이 대두되었습니다. 또한 클라우드 제공업체가 알려진 위치의 신뢰할 수 있는 하드웨어에서 워크로드가 실행되는지 여부를 파악할 수 있는 하드웨어 모니터링 및 보안 제어를 제공할 것을 기대합니다. {{site.data.keyword.cloud}}에서는 Intel&reg; TXT(Intel&reg; Trusted Execution Technology)를 사용하여 실행 환경의 개선된 보안 검증과 함께 하이브리드 및 클라우드 환경을 배치할 수 있도록 함으로써 해당 방법을 선도하고 있습니다.
{:shortdesc}

## 작동 방법

Intel TXT는 {{site.data.keyword.cloud_notm}} 인프라에 배치되거나 마이그레이션된 워크로드가 알려진 위치의 신뢰할 수 있는 하드웨어에서 실행 중인지 여부를 비즈니스에서 확인하는 데 도움이 되는 하드웨어 모니터링 및 보안 제어를 제공합니다. {{site.data.keyword.cloud_notm}}에서는 {{site.data.keyword.baremetal_short}} 범위에서 Intel TXT를 지원합니다. 전체 목록은 http://www.softlayer.com/intel-txt 를 참조하십시오.

Intel TXT는 운영 체제 또는 하이퍼바이저에서부터 컴퓨팅 시스템의 부팅 펌웨어 및 하드웨어까지의 컴퓨팅 시스템의 컴포넌트를 분석하고 측정합니다. 분석에는 시스템의 기본 입력/출력 시스템(BIOS), 마스터 부팅 레코드(MBR) 및 부팅 로더가 포함됩니다. 측정치는 시스템을 신뢰할 수 있는지 여부를 판별하는 표준 기준선과 비교됩니다. 시스템 소프트웨어 및 로컬 또는 원격 관리 소프트웨어는 신뢰 결정을 사용하여 해당 컴퓨팅 시스템이 실행 중인 워크로드를 승인하거나 거부할 수 있습니다. Intel TXT가 부팅 동안 분석 및 측정을 수행하므로, 추가된 보안때문에 애플리케이션에 성능 오버헤드가 부과되지는 않습니다.

기준선 측정치는 TPM(Trusted Platform Module) 하드웨어 디바이스에 저장됩니다. TPM 디바이스는 서버 시스템 내에서 통합되며 Intel TXT 보안 관련 기능의 범위를 제공합니다.

## 장점

Intel TXT는 의료, 재무 서비스 및 정부 조직과 같이 준수 및 감사 규제가 적용되는 대형 엔터프라이즈에 특히 적합합니다. 관련된 준수 조직(HIPAA, PCI, FedRAMP, ISO, FISMA 및 SSAE 16 등)과 함께 모든 신뢰할 수 있는 자원 추적을 통합, 관리 및 보고할 수 있습니다. 처음으로, 해당 조직에서 클라우드 컴퓨팅 시스템이 다음과 같은 워크로드에 대해 적절히 보안되는지 확인할 수 있습니다.

* 통제 및 엔터프라이즈 위험성
* 정보 및 라이프사이클 관리
* 준수 및 감사
* 애플리케이션 보안
* ID 및 액세스 관리
* 사고 대응

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}의 Intel TXT에 대한 자세한 정보를 보려면 http://www.softlayer.com/intel-txt 를 참조하십시오.

[IBM, VMware 및 HyTrust를 사용하는 신뢰할 수 있는 보안 클라우드 솔루션](http://wpc.c320.edgecastcdn.net/00C320/DeploymentGuide_IBM_Intel_HyTrust_VMware_v1%200.pdf) 링크는 워크로드에 추가 보안 및 규제 준수를 추가하는 방법에 대한 정보를 제공합니다.

**특수 기술 주의사항** Intel TXT(Intel Trusted Execution Technology)는 Intel&reg;에 의해 제공되며 지원 및 관리에 특수한 기술적 지식이 필요한 {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}에서 작동합니다. {{site.data.keyword.cloud_notm}}의 현재 제공되는 모델은 Intel TXT 켜기 또는 끄기를 허용합니다. **{{site.data.keyword.cloud_notm}}에서는 고객 환경 및 데이터의 민감성으로 인해 Intel TXT 설정 구성을 지원하지 않습니다.**. Intel TXT 기술에 관해 잘 아는 숙련된 직원이 있어야 합니다. 또는 RoT(Root of Trust) 및 MLE(Measured Launch Environment) 아키텍처를 조율하는 검증된 전문가가 있는 컨설팅 회사를 고용하는 것이 좋습니다.
