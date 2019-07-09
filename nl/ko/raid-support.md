---

copyright:
  years: 1994, 2019
lastupdated: "2018-5-31"

keywords: raid support, raid help

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# RAID 지원 티켓 정보
{:# bm-raid-support-ticket}

베어메탈 서버에서 RAID 사용에 대한 문제점이나 질문이 있으면 [IBM developerWorks dW Answers](https://developer.ibm.com/answers/topics/ibm-cloud/){:new_window} 포럼에서 답변을 찾을 수 있습니다.
지원 티켓을 열 수도 있습니다. 지원 티켓에 대한 정보는 [지원 티켓 열기](https://test.cloud.ibm.com/docs/get-support?topic=get-support-getting-customer-support#open-ticket){:new_window}를 참조하십시오.
{:shortdesc}

<!--During a drive or RAID failure, support tickets are automatically created. You can create a support ticket for other problems.--> 지원 티켓이 작성되면 RAID 로그 파일을 제공해야 합니다. RAID 로그 파일의 정보는 유실된 RAID 구성의 복구에 반드시 필요합니다. 로그 파일을 제공하면 지원 팀이 드라이브 순서, 어레이 멤버십, 어레이 기하학 및 케이블링 문제를 식별하는 데 도움이 됩니다. 사용하는 RAID 제어기의 유형(Adaptec 또는 LSI)에 따라 다음 명령을 사용하여 RAID 로그 파일을 가져오십시오. 

**참고:** 초기 업데이트에서 재시작/전원 끄기 권한을 부여하거나 핫스왑될 드라이브를 요청하면 지원 티켓 프로세스의 속도가 증가합니다.

<b>Adaptec RAID 카드</b><br>
다음 명령을 사용하여 Adaptec RAID 카드의 로그 파일을 가져올 수 있습니다. 반드시 지원 티켓에 이 로그 파일의 전체 출력을 포함해야 합니다. 

`arcconf getconfig 1/arcconf getlogs 1 device tabular`.

<b>LSI RAID cards</b><br>
다음 명령을 사용하여 LSI RAID 카드의 로그 파일을 가져오십시오. 지원 티켓에 다음 로그 파일의 전체 출력을 포함해야 합니다.
```/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
**중요:** 문제점 해결을 시작하기 전에 반드시 작업을 백업하십시오.
