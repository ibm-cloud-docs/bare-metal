---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-21"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# 가장 많이 사용되는 서버에서 선택
가장 많이 사용되는 서버 목록의 서버는 대부분의 클라이언트 유스 케이스 요구사항을 충족시키도록 사전 구성되며, 주문한 후 30 - 40분 내에 실행할 준비가 됩니다.
1. [{{site.data.keyword.cloud_notm}} 카탈로그](https://console.bluemix.net/catalog/){:target="_blank"}를 여십시오.   
2. Bare Metal Server를 선택하십시오.
3. 작성을 클릭하십시오.
2. 다음 정보를 선택하십시오.
    <table>
    <CAPTION>표 1. Bare Metal 선택</CAPTION>
    <THEAD>
    <TR>
    <th>필드</th>
    <th>값</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>수량</td>
    <td>+ 및 - 아이콘을 사용하여 프로비저닝할 동일한 서버 수를 지정하십시오.<br>사양이 서로 다른 여러 서버를 프로비저닝하려는 경우 개별적으로 프로비저닝해야 합니다.
    <tr>
    <td>위치</td>
    <td>서버를 둘 지역과 데이터 센터를 선택하십시오.</td>
    </tr>
    <tr>
    <tr>
    <td>호스트 이름과 도메인</td>
    <td>해당 필드는 기본값으로 채워져 있습니다. 해당 값을 변경할 수 있습니다.</td>
    </tr>
    <tr>
    <td>서버 선택</td>
    <td>**가장 많이 사용되는 서버**에서 요구사항에 맞는 서버를 선택하십시오. 해당 서버는 사전 구성되며 30 - 40분 내에 사용할 준비가 됩니다.
    </tr>
    <tr>
    <td>RAM</td>
    <td>선택한 서버를 기반으로 하는 기본값입니다.</td>
    </tr>
    <tr>
    <td>SSH 키</td>
    <td>프로비저닝된 후 서버에 로그인하는 데 사용할 SSH 키의 공개 키를 제공하십시오.</td>
    </tr>
    <tr>
    <td>이미지 <br>(운영 체제)</td>
    <td>인스턴스의 운영 체제를 선택하십시오. **참고**: 서버와 운영 체제 간에 충돌이 있으면 오류 메시지가 표시됩니다. 예를 들어 Microsoft SQL Server에서 Linux 선택합니다.</td>
    </tr>
    <td>업링크 포트 속도</td>
    <td>내부 및 외부 인터페이스의 속도를 결정합니다.</td>
    </tr>
    <tr>
    <td>추가 기능</td>
    <td> 해당 옵션을 선택하거나 기본값을 사용하십시오.</td>
    </tr>
    </TBODY>
    </table>

3.  주문 요약 섹션에서 **시간별** 또는 **월별** 비용 청구를 선택하십시오.
4.  주문을 검토하십시오.
5.  나열된 써드파티 서비스 계약을 검토하고 **써드파티 서비스 계약** 선택란을 클릭하십시오.
6.  **프로비전**을 클릭하십시오. 프로비저닝 주문 번호가 있는 화면으로 경로가 재지정됩니다. 화면이 프로비저닝 주문 영수증이기도 하므로 해당 화면을 인쇄할 수 있습니다.

 프로비저닝 주문 수신확인, 프로비저닝 주문 승인 및 처리, 프로비저닝 완료 등 일련의 이메일이 관리자에게 전송됩니다. 프로비저닝 완료 이메일에는 *디바이스 세부사항* 페이지 링크가 포함되어 있으므로 {{site.data.keyword.cloud_notm}}에 로그인할 수 있습니다. 또한 {{site.data.keyword.slportal}}에 직접 로그인할 수 있습니다.


## 다음 단계
{{site.data.keyword.baremetal_short}}가 프로비저닝된 후에 관리를 시작할 수 있습니다. 자세한 정보는 [{{site.data.keyword.baremetal_short}} 관리](../bare-metal/managing.html)를 참조하십시오.
