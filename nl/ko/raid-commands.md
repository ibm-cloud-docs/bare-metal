---
copyright:
  years: 1994, 2018
lastupdated: "2018-5-10"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID 제어기 명령

Adapatec 명령행 유틸리티를 사용하여 RAID 제어기 명령을 실행합니다.
다음은 사용할 수 있는 가장 일반적인 RAID 제어기 명령입니다.
{:shortdesc}

**참고:** Windows와 VMware는 storcli 명령을 실행하는 경로가 서로 다릅니다. 적절한 명령 경로는 다음 명령을 참조하십시오.

Windows(CMD 사용)
`C:\Program Files (x86)\MegaRAID Storage Manager>`      
또는
`C:\Program Files\LSIStorCli>`

VMware(storcli 명령을 실행하기 전에 storcli를 설치해야 함)
`/opt/lsi/storcli/`

## 명령 RAID 제어기 명령

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_에서는 조작 유형, 논리 드라이브 번호, 논리 드라이브 크기
및 운영 진행상태를 나열합니다. 다음 항목과 같이 실행 중인 백그라운드 명령의 상태도 볼 수 있습니다.
<ul>
  <li> 최신 다시 빌드
  <li> 동기화
  <li> 논리 드라이브 마이그레이션
  <li> 압축/확장
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1</b></code> <br>
_GETCONFIG_에서는 제어기, 논리 드라이브 및 실제 드라이브에 대한 정보를 나열합니다. 다음 항목과 같은 정보가 표시됩니다.
<ul>
  <li> 제어기 유형
  <li> BIOS, 부트 블록, 디바이스 드라이버 및 펌웨어 버전
  <li> 실제 디바이스 유형, 디바이스 ID, PFA 존재 여부
  <li> 실제 디바이스 상태
  <li> 격납장치 정보: 팬, 전원 공급 장치 및 온도
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular</code></b>
_GETLOGS_에서는 제어기의 상태와 이벤트 로그에 대한 액세스 권한을 제공합니다. _DEVICE xxx_에서는 제어기에서 발생하는 디바이스 오류 로그가 표시됩니다.

_GETLOGS_ 명령을 사용하여 작성된 출력의 다음 예를 참조하십시오.
```
driveErrorEntry
smartError.. ............................ false 
vendorID ................................ WDC
serialNumber ............................ WD-XXX
wwn ..................................... xxxxxxxxxxxxxxxx - CC_FILTER
deviceID ................................ 10
productID ............................... WD1003FB
numParityErrors ......................... 0
linkFailures ............................ 0
hwErrors ................................ 0
abortedCmds ............................. 7
mediumErrors ............................ 20
smartWarning ............................ 0
```

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show all | grep -iE "det|cou|tem|SN|S.M|fir” </code></b><br>
이 명령을 사용하여 특정 드라이브와 가능한 드라이브 오류를 보여줍니다.
다음 예제에서는 출력을 보여줍니다.
```
Drive /c0/e252/s0 - Detailed Information: 
Shield Counter = 0
 Media Error Count = 0
 Other Error Count = 0 
Drive Temperature = 24C (75.20 F) 
Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No 
SN = XXXX 
Firmware Revision = SN04

 Drive /c0/e252/s1 - Detailed Information: 
Shield Counter = 0 
Media Error Count = 0 
Other Error Count = 0 
Drive Temperature = 22C (71.60 F) 
Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No 
SN = xxxx 
Firmware Revision = SN03 

Drive /c0/e252/s2 - Detailed Information:
 Shield Counter = 0 
Media Error Count = 0 
Other Error Count = 0 
Drive Temperature = 21C (69.80 F)
 Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No
 SN = xxxx 
Firmware Revision = SN04

 Drive /c0/e252/s3 - Detailed Information:
 Shield Counter = 0 
Media Error Count = 0
 Other Error Count =
 Drive Temperature = 23C (73.40 F) 
Predictive Failure Count = 0
 S.M.A.R.T alert flagged by drive = No 
SN = xxxx
Firmware Revision = SN03  
```

<!--<code><b>/opt/MegaRAID/storcli/storcli64 /c0 show all | less </code></b>-->
<!--You use this command to view RAID health, size, name, and other important information.-->

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show rebuild</code></b>
이 명령에서는 다시 빌드를 완료할 예상 시간과 모든 드라이브의 다시 빌드 상태를 표시합니다. 명령을 실행하면 다음 출력이 표시됩니다.
```
---------------------------------------------
Drive-ID Progress% Status Estimated Time Left 
---------------------------------------------
/c0/e252/s0 - Not in progress
 /c0/e252/s1 - Not in progress
 /c0/e252/s2 - Not in progress
 /c0/e252/s3 - Not in progress
--------------------------------------------- 
```

<b>RAID alert "Spam"</b>
Change the "global" section of the default config (/opt/lsi/mrmonitor/MegaMonitor/config-current.xml): 
```<global>
 <severity level="FATAL"> 
<do-systemlog/> 
<do-email/>
 </severity>
<severity level="CRITICAL"> 
<do-email/>
 <do-systemlog/> 
</severity>
 <severity level="WARNING">
 <do-email/> 
<do-systemlog/> 
</severity>
 <severity level="INFO"> <do-systemlog/>
</severity>
 </global> 
```
to this: 
```
<global> 
<severity level="FATAL"> 
<do-systemlog/> 
<do-email/>
 </severity> 
<severity level="CRITICAL"> 
<do-email/> 
<do-systemlog/> 
</severity> 
<severity level="WARNING"> 
<do-systemlog/> 
</severity> 
<severity level="INFO">
<do-systemlog/>
 </severity> 
</global> 
```
**참고:** "WARNING" 레벨의 "do-email" 태그를 제거하십시오. 또는 보안 레벨을 "INFO"로 변경하십시오.

## 공통 드라이브 오류

가장 일반적인 드라이버 오류는 스마트 오류, 하드웨어 오류 및 매체 오류입니다. 드라이브에 장애가 발생하면 이 오류가 표시됩니다. 따라서 최대한 빨리 드라이브를 교체해야 합니다.

일반적이지는 않지만 중단된 명령은 또 다른 일반 오류입니다. 그러나 중단 명령의 수가 늘어나면(예: 100) 지원 티켓을 여십시오.  

링크 오류에서 케이블을 재고정해야 하거나 교체해야 할 수도 있음을 나타냅니다.

## 지원 티켓 정보

<b>Adaptec RAID 카드</b>
지원 티켓을 작성할 때 `arcconf getconfig 1/arcconf getlogs 1 device tabular`의 전체 출력을 포함하십시오. 이 정보를 제공하면 지원 팀이 드라이브 순서, 어레이 멤버십, 어레이 기하학 및 케이블링 문제를 파악하는 데 도움이 됩니다. 이 정보는 유실된 RAID 구성 복구에 중요합니다. 초기 업데이트에서 다시 시작/전원 끄기 권한을 부여하거나 핫스왑 가능하도록 요청하면 지원 티켓 프로세스 속도가 증가합니다.

<b>LSI RAID cards</b>
다음 명령을 사용하여 LSI RAID 카드의 로그 파일을 가져오십시오. 지원 티켓으로 해당 로그 파일의 전체 출력을 포함시켜야 합니다.
```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```

**참고**: 문제점 해결을 완료하기 전에 작업을 백업하십시오.
