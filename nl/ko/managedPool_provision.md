---

copyright:
  years:  2019
lastupdated: "2019-02-01"

keywrods: provision managed pool, managed pools

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 고객 관리 풀 프로비저닝
{: #bm-provision-managed-pools}

서버의 고객 관리 풀을 프로비저닝하려면 IBM에 직접 문의하십시오. [도움 및 지원 받기](/docs/bare-metal?topic=bare-metal-gettinghelp).

다음 정보를 제공하십시오.
* 관리 풀을 둘 데이터 센터. (관리 풀의 모든 서버는 같은 데이터 센터에 있어야 합니다.)
* 관리 풀에 둘 서버 수
* 풀링된 서버에 필요한 사양

풀을 작성하고 나면 IBM에서 다음 매개변수값을 제공합니다. 풀을 관리하기 위해 API 명령을 전송할 때 이 값이 필요합니다.
* poolKeyName
* backendRouter

## 관리 풀에서 서버 주문
{: #bm-order-server-managed-pool}
표준 프로비저닝 프로세스를 사용하여 풀의 서버를 주문하십시오. 풀에서 주문을 이행하고 주문한 서버 수로 풀이 보충됩니다.

## 다음 단계

고객 관리 풀을 프로비저닝하고 관리 풀에서 서버를 주문하고 나면 풀의 서버 수를 관리할 수 있습니다. [고객 관리 풀에서 서버 수 지정](/docs/bare-metal?topic=bare-metal-set-amount-servers-pool#set-amount-servers-pool)을 참조하십시오.
