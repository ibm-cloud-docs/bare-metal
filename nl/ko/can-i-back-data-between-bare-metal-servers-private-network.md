---

copyright:
  years: 1994, 2019
lastupdated: "2019-05-02"

keywords: back up, recovery, IBM Cloud Backup, r1soft

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 백업 및 복구
{: #sm-back-up-recovery}

{{site.data.keyword.Bluemix_notm}}는 사용자의 백업 요구사항에 맞게 다양한 확장 가능 [백업 및 스토리지 솔루션 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/cloud/storage){: new_window}을 제공합니다. 그러나 {{site.data.keyword.Bluemix_notm}}에서는 고객 디바이스의 백업을 완료하지 않습니다. 해당 계정의 사용자가 디바이스에 대한 모든 스케줄된 백업 및 일회성 백업을 시작해야 합니다.

둘 이상의 {{site.data.keyword.baremetal_short}}가 한 계정에 존재하는 경우, 한 디바이스의 데이터가 다른 디바이스에서 백업될 수 있습니다. 사설 네트워크 트래픽에 대한 대역폭 한계가 적용되지 않으므로 동시에 계정을 공유하는 임의의 디바이스로 데이터가 전송되거나 백업될 수 있습니다. 다음을 솔루션을 포함하여 {{site.data.keyword.baremetal_short}}에 여러 백업 솔루션을 사용할 수 있습니다.

* [IBM Cloud 백업](/docs/infrastructure/Backup?topic=Backup-getting-started#getting-started)은 여러 서버 간의 백업을 자동화할 수 있는 엔터프라이즈 백업 솔루션입니다. 데이터는 엔터프라이즈 SAN(Storage Area Network)에 저장됩니다.
* [NAS(Network Attached Storage)](/docs/infrastructure/network-attached-storage?topic=network-attached-storage-GettingStarted#GettingStarted)는 업계 표준이며 중요한 데이터에 대한 오프서버 스토리지를 제공합니다. 데이터는 엔터프라이즈 SAN(Storage Area Network)에 저장됩니다.
* [R1Soft CDP](/docs/infrastructure/software?topic=software-ordering-r1soft#ordering-r1soft)는 중심 관리 및 데이터 저장소 기능을 수행하는 고성능 디스크 간 서버 백업을 제공합니다. R1Soft CDP는 데이터를 블록 레벨에서 보호하며 서버의 고유한 디스크 블록이 모든 복구 지점에서 한 번만 저장되므로 스토리지 효율성이 높습니다.
