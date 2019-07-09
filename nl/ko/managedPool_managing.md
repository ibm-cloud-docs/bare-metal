---

copyright:
  years:  2019
lastupdated: "2018-05-15"

keywords: number servers managed pool, managed pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 고객 관리 풀에서 서버 수 지정
{: #set-amount-servers-pool}

다음 API 호출을 사용하여 관리 풀에서 서버 수를 설정하십시오.

|API 호출|매개변수|설명|
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank">관리 풀 수량 설정</a>|poolKeyName|풀을 식별하는 키 이름입니다. IBM에서 이 값을 제공합니다.|
|  | backendRouter | 풀의 백엔드 라우터를 식별합니다. IBM에서 이 값을 제공합니다.|
|  | quantity | 풀에 필요한 총 서버 수입니다.<br><br>풀에 있는 서버의 현재 수가 여기에 제공하는 값 미만이면 서버가 추가됩니다. <br>풀에 있는 서버의 현재 수가 여기에 제공하는 값을 초과하면 서버가 제거됩니다.|
