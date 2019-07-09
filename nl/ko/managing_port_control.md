---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-18"

keywords: manage bare metal port control

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 디바이스의 포트 제어 관리
{: #bm-manage-port-control}

계정과 연관된 각 디바이스에는 수신 트래픽을 받는 두 개의 네트워크가 있습니다. 하나는 공용 네트워크 트래픽용이고 다른 하나는 사설 네트워크 트래픽용입니다. 해당 포트를 언제든 사용하거나 사용 안함으로 설정하여 디바이스가 받는 네트워크 트래픽을 제어할 수 있습니다. 다음 단계를 완료하여 디바이스의 포트 제어 설정을 업데이트하십시오.

## 시작하기 전에
* 콘솔의 디바이스 메뉴로 이동하십시오. 자세한 정보는 [디바이스로 이동](/docs/bare-metal?topic=virtual-servers-navigating-devices)을 참조하십시오.
* 필요한 계정 권한과 디바이스 액세스 권한이 있는지 확인하십시오. 계정 소유자 또는 **사용자 관리** 클래식 인프라 권한이 있는 사용자만 권한을 조정할 수 있습니다.

권한에 대한 자세한 정보는 [클래식 인프라 권한](/docs/iam?topic=iam-infrapermission#infrapermission) 및 [디바이스 액세스 권한 관리](/docs/bare-metal?topic=virtual-servers-managing-device-access)를 참조하십시오. 

## 디바이스의 포트 제어 관리

1. **디바이스 목록**에 액세스하여 업데이트할 **디바이스 이름**을 선택하십시오.  
2. 디바이스의 **조치** 드롭 다운 목록을 클릭하십시오.
3. **포트 제어**를 선택하십시오.
4. 다음 조치 중 하나를 완료하여 *공용 네트워크* 및/또는 *사설 네트워크* 드롭 다운 상자를 업데이트하십시오.
   * 원하는 속도를 선택하여 네트워크 액세스를 가능하게 하십시오.
   * 연결 끊기를 선택하여 네트워크 액세스를 사용하지 않게 설정합니다.
5. 업데이트 단추를 클릭하십시오.
6. 닫기 단추를 클릭하여 창을 닫으십시오.

## 다음 단계

**사용 안함**을 선택한 경우 디바이스 인터페이스에 대한 사용하지 않는 포트의 네트워크 액세스는 중단됩니다. **사용**을 선택한 경우 사용된 포트의 네트워크 액세스가 가능합니다. 선택한 설정의 포트 제어는 수동으로 변경할 때까지 그대로 남아 있습니다.
