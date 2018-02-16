---



copyright:
  years: 2017
lastupdated: "2017-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 베어메탈 서버 프로비저닝

## 시작하기 전에
퍼블릭 {{site.data.keyword.baremetal_long}}를 프로비저닝하는 옵션은 두 가지입니다. 첫 번째 옵션은 {{site.data.keyword.cloud}} 카탈로그를 통하는 것이며 두 번째 옵션은 {{site.data.keyword.slportal_full}}을 통하는 것입니다. 카탈로그 및 {{site.data.keyword.slportal}}에는 고유 로그인 ID가 필요합니다. 카탈로그 사용자 이름 및 비밀번호를 포털에 로그인하는 데 사용할 수 없으며 반대의 경우도 마찬가지입니다.
{:shortdesc}

시작하기 전에 {{site.data.keyword.cloud_notm}} 카탈로그 또는 {{site.data.keyword.slportal}} 신임 정보가 설정되었는지 확인하십시오.

**참고:** {{site.data.keyword.cloud_notm}} 카탈로그의 경우 {{site.data.keyword.baremetal_short}}를 주문하려면 업그레이드된 계정이 있어야 합니다. 계정 업그레이드에 대한 자세한 정보는 [IBM ID로 전환](https://console.ng.bluemix.net/docs/admin/softlayerlink.html)을 참조하십시오.

## 로그인
{{site.data.keyword.cloud_notm}} 카탈로그 또는 {{site.data.keyword.slportal}}을 통해 로그인했는지 확인하십시오.

  <table>
   <CAPTION>표 1. 로그인 위치 선택</CAPTION>
   <THEAD>
   <TR>
   <th>다음을 통해 로그인</th>
   <th>수행할 조치</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud 카탈로그</td>
   <td>
   <ol>
   <li>새 브라우저 창을 열고 <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>를 입력하십시오.</li>
   <li><b>로그인</b> 링크를 클릭하십시오. </li>
   <li>이메일 및 IBM ID를 입력하고 <b>계속</b>을 클릭하십시오.</li>
   <li>비밀번호를 입력하고 <b>로그인</b>을 클릭하십시오.</li>
   <li><b>인프라</b> > <b>컴퓨팅</b>을 선택하십시오.</li>
   <li><b>{{site.data.keyword.baremetal_short}}</b> 타일을 클릭하십시오.</li>
   <li><b>작성</b>을 클릭하십시오. {{site.data.keyword.slportal}}의 기본 페이지가 열립니다.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>고객 포털</td>
   <td>
   <ol>
   <li>새 브라우저 창을 열고 <a href="https://control.softlayer.com">https://control.softlayer.com</a>을 입력하십시오.</li>
   <li>사용자 이름 및 비밀번호를 입력하고 <b>로그인</b>을 클릭하십시오. 또는 <b>IBM ID로 로그인</b>을 클릭하십시오. 그런 다음 이메일 또는 IBM ID를 입력하고 <b>계속</b>을 클릭하십시오. 비밀번호를 입력하고 <b>로그인</b>을 클릭하십시오. {{site.data.keyword.slportal}}의 기본 페이지가 열립니다.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## 베어메탈 서버 프로비저닝
{: #ordering-baremetal-server}
로그인한 다음 {{site.data.keyword.baremetal_short}} 프로비저닝을 시작할 수 있습니다. **디바이스** 메뉴 또는 **디바이스** 아이콘을 통해 {{site.data.keyword.baremetal_short}}를 프로비저닝할 수 있습니다.

### 디바이스 아이콘을 통해 베어메탈 서버 프로비저닝
*디바이스* 아이콘을 통해 {{site.data.keyword.baremetal_short}}를 프로비저닝하려면 다음 단계를 완료하십시오.

1.  {{site.data.keyword.slportal}}에서 **주문** 섹션을 찾아서 **디바이스**를 클릭하십시오.
2.  디바이스 페이지의 {{site.data.keyword.baremetal_short}} 아래에서 **시간별** 또는 **월별**을 클릭하십시오.
3.  **데이터 센터**를 선택하고 페이지를 스크롤한 다음 **시작 가격 대상** 링크를 클릭하여 서버를 선택하십시오.
4.  **{{site.data.keyword.baremetal_short}} 구성** 페이지에서 정보를 입력하고 **주문에 추가** 단추를 클릭하여 계속하십시오. 서버 구성 방법에 대한 자세한 정보는 [{{site.data.keyword.baremetal_short}} 구성](../bare-metal/configuring.html)을 참조하십시오. 주문이 확인되면 **체크아웃** 페이지로 경로가 재지정됩니다.
5.  서버에 대한 **고급 시스템 구성**을 입력하십시오. 설정 방법에 대한 자세한 정보는 [{{site.data.keyword.baremetal_short}} 구성](../bare-metal/configuring.html)을 참조하십시오.
6.  **클라우드 서비스 이용 약관** 및 **써드파티 서비스 계약** 선택란을 클릭하십시오.
7.  지불 정보를 확인하거나 입력하고 **주문 제출** 단추를 클릭하십시오. 프로비저닝 주문 번호가 있는 화면으로 경로가 재지정됩니다. 화면이 프로비저닝 주문 영수증이기도 하므로 해당 화면을 인쇄할 수 있습니다.

 프로비저닝 주문 수신확인, 프로비저닝 주문 승인 및 처리, 프로비저닝 완료 등 일련의 이메일이 관리자에게 전송됩니다. 프로비저닝 완료 이메일에는 {{site.data.keyword.cloud_notm}}에 로그인한 후의 *디바이스 세부사항* 페이지에 대한 링크가 포함됩니다. 또한 {{site.data.keyword.slportal}}에 직접 로그인할 수 있습니다.

### 디바이스 메뉴를 통해 베어메탈 서버 프로비저닝
{: #ordering-baremetal-devices-menu}

또한 기본 {{site.data.keyword.slportal}} 페이지의 *디바이스* 메뉴를 통해 {{site.data.keyword.baremetal_short}}를 프로비저닝할 수 있습니다.

1. **디바이스 > 디바이스 목록**을 클릭하십시오. 디바이스 페이지에는 사용자 계정 내의 모든 디바이스 유형(전용 호스트, 가상 서버, 베어메탈 서버 및 NetScaler 애플리케이션 전송 컨트롤러)이 표시됩니다.
2. 오른쪽 상단 모서리에 있는 **디바이스 주문** 링크를 클릭하십시오.
3. SoftLayer 제품 및 서비스 주문 페이지의 {{site.data.keyword.baremetal_short}} 아래에서 **시간별** 또는 **월별**을 클릭하십시오.
4. **데이터 센터**를 선택하고 페이지를 스크롤한 다음 **시작 가격 대상** 링크를 클릭하여 서버를 선택하십시오.
5.  **{{site.data.keyword.baremetal_short}} 구성** 페이지에서 정보를 입력하고 **주문에 추가** 단추를 클릭하여 계속하십시오. 서버 구성 방법에 대한 자세한 정보는 [{{site.data.keyword.baremetal_short}} 구성](../bare-metal/configuring.html)을 참조하십시오. 주문이 확인되면 **체크아웃** 페이지로 경로가 재지정됩니다.
6.  서버에 대한 **고급 시스템 구성**을 입력하십시오. 설정 방법에 대한 자세한 정보는 [{{site.data.keyword.baremetal_short}} 구성](../bare-metal/configuring.html)을 참조하십시오.
7. **클라우드 서비스 이용 약관** 및 **써드파티 서비스 계약** 선택란을 클릭하십시오.
8. 지불 정보를 확인하거나 입력하고 **주문 제출** 단추를 클릭하십시오. 프로비저닝 주문 번호가 있는 화면으로 경로가 재지정됩니다. 화면이 프로비저닝 주문 영수증이기도 하므로 해당 화면을 인쇄할 수 있습니다.

프로비저닝 주문 수신확인, 프로비저닝 주문 승인 및 처리, 프로비저닝 완료 등 일련의 이메일이 관리자에게 전송됩니다. 프로비저닝 완료 이메일에는 {{site.data.keyword.cloud_notm}}에 로그인한 후의 *디바이스 세부사항* 페이지에 대한 링크가 포함됩니다. 또한 {{site.data.keyword.slportal}}에 직접 로그인할 수 있습니다.

### 다음 단계
{{site.data.keyword.baremetal_short}}가 프로비저닝된 후에 관리를 시작할 수 있습니다. 자세한 정보는 [{{site.data.keyword.baremetal_short}} 관리](../bare-metal/managing.html)를 참조하십시오.
