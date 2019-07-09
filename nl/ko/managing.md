---

copyright:
  years: 2016, 2019
lastupdated: "2019-06-17"

keywords: manage bare metal servers, power off, replicate, reload os, delete server, manage server

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note .note}

# Bare Metal Server 관리
{: #bm-manage-servers}

서버를 취소, 중지 및 다시 시작할 수 있습니다.
{:shortdesc}

## 시작하기 전에
{: #before-you-begin}

* 콘솔의 디바이스 메뉴로 이동하십시오. 자세한 정보는 [디바이스로 이동](/docs/bare-metal?topic=virtual-servers-navigating-devices)을 참조하십시오.
* 필요한 계정 권한과 디바이스 액세스 권한이 있는지 확인하십시오. 계정 소유자 또는 **사용자 관리** 클래식 인프라 권한이 있는 사용자만 권한을 조정할 수 있습니다.

권한에 대한 자세한 정보는 [클래식 인프라 권한](/docs/iam?topic=iam-infrapermission#infrapermission) 및 [디바이스 액세스 권한 관리](/docs/bare-metal?topic=virtual-servers-managing-device-access)를 참조하십시오. 


<!-- ## Replicating a server instance
{: #bm-replicate-server-instance}

You can copy or clone a bare metal server instance to replicate the server configuration and quickly get a new server up and running.
{:shortdesc}

To clone the instance:
 1. Go to the **Device** menu and highlight the device to be copied.
 2. Click **Actions** and select **Configure Replica**. All configurations are copied. No data or content is not copied.
 3. Enter a unique server name.
 4. Specify the domain name. -->

<!-- ## Reloading the operating system
{: #bm-reload-os}

Occasionally, you might want to reload the operating system on your server.
{:shortdesc}

To reload the operating system, follow these steps.
 1. Back up all data before you start. If you don't back up your data, all data that is on the primary disk is lost. But, secondary disk data stays intact.
 2. Go to the **Devices** menu and highlight the device to be reloaded.
 3. Click **Actions** and select **OS Reload**. You can select one of these options:
  * Change the operating system to a different one and start over with new configurations.
  * Keep the existing operating system with the current configurations, but wipe out the server to start over.

During the OS reload, the server is offline and unavailable for use. Reload time varies based on server capacity and operating system. If you defined a provision script, all configurations are restored after the reload completes. Data was backed up before the OS reload can be uploaded the server when the server is available. -->

## 서버 인스턴스 삭제
{: #bm-delete-server-instance}

인스턴스가 더 이상 필요하지 않으며 요금이 부과되는 것을 원하지 않으면 언제든지 Bare Metal Server 인스턴스를 삭제할 수 있습니다.
{:shortdesc}

1. **디바이스** 메뉴로 이동하여 삭제할 디바이스를 강조 표시하십시오.
2. **조치**를 클릭하고 **서버 취소**를 선택하십시오.

## 서버 전원 끄기
{: #bm-power-off}

사용할 준비를 하기 위해 서버를 미리 작성할 수 있습니다. 서버가 작성되면 변경을 방지하고 액세스를 차단하도록 전원을 끄십시오. 준비가 되면 서버의 전원을 켜서 몇 분 안에 준비할 수 있습니다.
{:shortdesc}

1. **디바이스** 메뉴로 이동하여 전원 켜기/끄기를 수행할 디바이스를 강조 표시하십시오.
2. **조치**를 클릭하고 **전원 켜기/끄기**를 선택하십시오.

전원이 꺼진 동안 서버에 대해 비용이 청구됩니다. 서버의 전원이 꺼지면 꺼진 상태가 유지되므로 수동으로 전원을 켜야 합니다.
{: note}
