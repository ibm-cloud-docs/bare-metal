---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# OS 없음 옵션
{: #bm-no-os}

OS 없음은 운영 체제 없이 Bare Metal Server를 주문할 수 있는 옵션입니다.

## OS 없이 Bare Metal Server를 주문할 수 있는 방법은 무엇입니까?

[SoftLayer.com](https://www.softlayer.com) 또는 [고객 포털](https://control.softlayer.com)을 통해 Bare Metal Server를 주문하는 것부터 시작하십시오.

1. **시스템 구성 > 운영 체제**에서 **기타**를 선택하십시오.
2. **운영 체제 없음**을 선택하십시오.

## OS가 없는 서버에 운영 체제를 설치하는 방법은 무엇입니까?

운영 체제가 없는 Bare Metal Server에 운영 체제를 설치하는 두 가지 방법이 있습니다.

### 옵션 1: PXE 서버

운영 체제가 없는 Bare Metal Server는 PXE 설정에서 OS를 부팅하고 로드하도록 설정할 수 있습니다(자세한 정보는 [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment)를 참조하십시오). PXE 설정을 사용하여 네트워크 환경에서 Bare Metal Server를 배치하고(이는 일반적으로 DHCP 및 TFTP 디먼 실행과 연관됨) 새 Bare Metal Server BIOS가 네트워크 어댑터에서 부팅되도록 구성하기만 하면 됩니다. 비OS 옵션이 올바르게 작동하려면 PXE 설정이 Bare Metal Server와 같은 VLAN 에 있거나 DHCP 전달이 사용되어야 합니다.

**참고:** 이 옵션이 작동하려면 스위치 포트가 기본 모드에서 다시 그룹화되도록 요청하는 지원 티켓을 열어야 하는 경우가 있습니다. PXE 프로토콜이 현재 중복성을 제공하기 위한 표준 기능인 링크 집계(LACP. [링크 집계](http://en.wikipedia.org/wiki/Link_aggregation)를 참조하십시오)와의 호환성을 요구하지 않기 때문입니다. 다른 옵션은 바인딩되지 않은 업링크(링크 집계 없음)를 사용하여 서버를 주문한 다음 OS를 설치한 후에 중복 업링크로 변경하는 것입니다.

### 옵션 2: IPMI 디바이스

포함된 IPMI 디바이스를 통해 ISO에서 부팅하여 운영 체제 없이 Bare Metal Server에 운영 체제를 설치하십시오. ISO에서 부팅하는 방법에 대한 추가 정보를 보려면 [여기](mount-iso-bare-metal-server.html)를 클릭하십시오.
