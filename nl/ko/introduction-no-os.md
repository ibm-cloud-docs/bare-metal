---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: bare metal, no os, no operating system

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# OS 없음 옵션
{: #bm-no-os}

**OS 없음**은 운영 체제 없이 {{site.data.keyword.baremetal_long}}를 주문하기 위한 옵션입니다.

## OS 없이 {{site.data.keyword.baremetal_short}} 주문
{: #ordering-no-os}

1. [사용자 정의 베어메탈 서버 빌드](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server)에서 간략히 설명된 단계를 사용하여 서버를 주문하십시오.
2. **이미지** 아래에서 **OS 없음**을 선택하십시오.
3. 서버 주문을 완료하십시오. 

## OS 없음으로 변경
{: #changing-to-no-os}

OS 없음으로 서버를 재구성할 수 있습니다. 재구성은 OS 재로드를 통해 이루어집니다. 자세한 정보는 [OS 재로드](/docs/infrastructure/software?topic=software-reloading-the-os)를 참조하십시오.

1. **디바이스** > **디바이스 목록**을 클릭하십시오.
2. OS 없음으로 재구성할 서버를 선택하십시오.
3. **OS 재로드**를 클릭하고 해당되는 정보를 입력하십시오. 

## OS 없는 서버에 운영 체제 설치
{: #installing-os-on-no-os-server}

운영 체제 없는 {{site.data.keyword.baremetal_short}}에 운영 체제를 설치하는 두 가지 방법이 있습니다.

### 옵션 1: PXE 서버
{: #option-1}

운영 체제 없는 {{site.data.keyword.baremetal_short}}는 PXE 설정에서 부팅하고 OS를 로드하도록 설정될 수 있습니다. <!--(see [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) for more information)--> PXE 설정으로 네트워크 환경에서 {{site.data.keyword.baremetal_short}}를 배치하고(여기에는 일반적으로 DHCP 및 TFTP 디먼 실행이 포함됨) 네트워크 어댑터에서 부팅하도록 새 서버 BIOS를 구성하십시오. OS 없음 옵션이 제대로 작동하려면 PXE 설정이 {{site.data.keyword.baremetal_short}}와 동일한 VLAN에 있거나 DHCP 전달이 사용되어야 합니다.

이 옵션이 작동하려면 지원 티켓을 열어서 스위치 포트를 기본 모드로 다시 그룹화하도록 요청해야 할 수 있습니다. 이는 이제 중복성 제공을 위한 표준 기능인 링크 집계(LACP)와의 호환성이 PXE 프로토콜에서 필요하지 않기 때문입니다.<!--see [Link Aggregation](http://en.wikipedia.org/wiki/Link_aggregation))--> 다른 옵션은 바인딩되지 않은 업링크(링크 집계 없음)를 사용하여 서버를 주문한 다음 OS를 설치한 후에 중복 업링크로 변경하는 것입니다.
{: note}

### 옵션 2: IPMI 디바이스
{: #option-2}

포함된 IPMI 디바이스를 통해 ISO에서 부팅하여 운영 체제 없는 {{site.data.keyword.baremetal_short}}에 운영 체제를 설치하십시오. ISO에서 부팅에 대한 자세한 정보는 [베어메탈 서버에 ISO 마운트](/docs/bare-metal?topic=bare-metal-mounting-an-iso-on-a-bare-metal-server)를 참조하십시오.
