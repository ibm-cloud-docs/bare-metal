---
copyright:
  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID 모니터링 디먼의 이름 및 위치
{{site.data.keyword.cloud}}에서는 레거시 하드웨어에 대한 몇 가지 예외 외에는 주로 Adaptec 및 LSI RAID 카드를 사용합니다. 다음 표에서는 RAID 관리자 위치, 모니터 위치, 구성 및 RAID 경보 설정을 표시합니다.

RAID 카드에 대한 구성에서 SMTP 서버 및 알림 이메일 대상을 변경하여 포털 모니터링 프로세스를 우회하도록 RAID 경보를 구성할 수 있습니다. 이러한 구성이 변경되면 IBM이 사용자에게 RAID 문제를 알리거나 해결될 때까지 자동으로 문제점을 추적할 수 없습니다. 이러한 위험성을 인식하지 못한 상태로 제공된 구성을 변경하지 마십시오.

<caption>표 1. RAID 구성 및 설정</caption>

||LSI Linux|LSI Windows|Adaptec Linux|Adaptec Windows|
|---|---|---|---|---|
|**관리자 이름**|LSI MegaRAID Storage Manager|LSI MegaRAID Storage Manager|Adaptec Storage Manager|Adaptec Storage Manager|
|**관리자 위치**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**모니터 이름**|MR_Monitor|MRMonitor|Adaptec Event Manager|Adaptec Event Manager|
|**모니터 위치**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**프로세스 이름**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**로그 위치**|OS에 대한 기본 메시지 로그 위치(예: /var/log/messages).|GUI에서만|/usr/StorMan/RaidEvtA.log|GUI에서만|
|**이메일 대상 알림**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**이메일 소스 형식 알림**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**이메일 포트**|25|25|25|25|
|**SMTP 서버**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**대체 알림 옵션**|SMTP 서버를 로컬 SMTP 서버로 변경하십시오. 로컬 SMTP 서버에는 적절한 방화벽 구성이 필요합니다.|SMTP 서버를 로컬 SMTP 서버로 변경하십시오. 로컬 SMTP 서버에는 적절한 방화벽 구성이 필요합니다.|SMTP 서버를 로컬 SMTP 서버로 변경하십시오. 로컬 SMTP 서버에는 적절한 방화벽 구성이 필요합니다.|SMTP 서버를 로컬 SMTP 서버로 변경하십시오. 로컬 SMTP 서버에는 적절한 방화벽 구성이 필요합니다.|
