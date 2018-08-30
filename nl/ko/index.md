---



copyright:
  years: 2018, 2018
lastupdated: "2018-06-18"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Bare Metal Server 시작하기
{: #getting-started}

{{site.data.keyword.baremetal_long}}는 하드웨어 리소스에 대한 하위 레벨 액세스 권한과 함께 성능과 제어를 제공하는 단일 테넌트 물리적 서버입니다. "소란스러운 이웃"과 서버를 공유하지 않고 사용자 전용입니다!
{: shortdesc}

표 1에는 {{site.data.keyword.baremetal_short}}를 신속하게 프로비저닝하고 구성할 수 있는 단계가 포함되어 있습니다.
<table>
   <CAPTION>표 1. 빠른 시작 단계</CAPTION>
   <THEAD>
   <TR>
   <th>태스크</th>
   <th>세부사항</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>1. 구현에 도움을 줄 수 있는 컨텐츠 검토</td>
   <td>IBM Cloud와 Bare Metal Server를 처음 사용해 보십니까? 다음 사이트에서는 환경을 계획하는 데 도움이 되는 유용한 정보를 제공합니다.
   <li><a href="https://ibm.com/cloud-computing/">IBM Cloud의 개념</a></li>
   <li><a href="https://ibm.com/cloud/get-started">IBM Cloud 시작하기</a></li>
   <li><a href="https://www.ibm.com/cloud/bare-metal-servers">Bare Metal Server</a></li>
   </td>
 <tr>
   <td>2. IBM Cloud 신청</td>
   <td><a href="https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-ibm-cloud">IBM Cloud 신청</a>에는 IBM Cloud 계정 설정 방법에 대한 단계가 포함되어 있습니다.</td>
 <tr>
   <td>3. 워크로드 사양 판별</td>
   <td>서버를 프로비저닝하기 전에 성공적으로 수행하는 데 필요한 서버의 크기와 서버 사용 방법을 결정하십시오. 예를 들어 개발, 테스트 또는 프로덕션용으로 서버를 사용할 계획입니까? 사용자 경험, 긴 알고리즘 처리, 데이터 백업 및 복원 또는 대기 시간 줄이기 등을 테스트할 것입니까?</td>  
 <tr>
   <td>4. 서버 크기 및 비용 예측</td>
   <td><a href="https://www.ibm.com/cloud-computing/bluemix/bare-metal-search">Bare Metal 검색 도구</a>를 사용하여 서버의 크기와 비용을 예측하십시오.</td>
 <tr>
   <td>5. IBM Cloud 계정에 로그인</td>
   <td>IBM Cloud 카탈로그 또는 IBM Cloud 인프라 고객 포털에서 Bare Metal Server 주문 양식에 액세스할 수 있습니다. 카탈로그와 인프라 고객 포털에 액세스하려면 <a href="https://console.bluemix.net/docs/customer-portal/getting-started.html#getting-started">IBM ID 및 비밀번호</a>가 있어야 합니다.
   <li><a href="https://console.bluemix.net/catalog/">IBM Cloud 카탈로그</a></li>
   <li><a href="https://control.softlayer.com">IBM Cloud 인프라 고객 포털</a></li>  
   </td>   
<tr>   
   <td>6. 서버 프로비저닝</td>
   <td>서버 프로비저닝 시 세 가지 옵션(가장 많이 사용, 사용자 정의 및 SAP 인증)이 있습니다. 가장 많이 사용되는 서버는 대부분의 고객 요구사항을 충족하는 사전 구성된 서버이고 프로비저닝 후 30 - 40분 내에 구성할 준비가 됩니다. 
   
     
<br>사용자 정의 서버는 요구사항을 충족시키기 위해 특정 컴퓨팅, 연결, 스토리지 및 네트워크 옵션을 선택하여 작성하는 서버입니다. 사용자 정의 서버는 프로비저닝하는 데 더 오래 걸리며(일반적으로 2 - 4시간) 운영 비용이 높아집니다. <a href="bm_provision_ssd.html">Intel Optane 호환 가능 Bare Metal Server를 프로비저닝</a>하는 옵션 또는 <a href="bare-metal-provision-SGX.html">Intel SGX 아키텍처</a>를 사용하는 옵션도 있습니다. 
     
<br>SAP 인증 서버는 SAP HANA 및 SAP NetWeaver 환경을 지원하도록 특별하게 인증되었습니다.
해당 서버 유형의 정보를 제공하기 위해 작성된 링크를 사용하십시오. SAP 인증 서버를 사용하면 프로비저닝할 환경 유형(SAP HANA 또는 SAP NetWeaver)을 선택해야 합니다.  
  <li><a href="baremetal-provision-popular.html">신속하게 프로비저닝된 Bare Metal Server</a></li>
  <li><a href="baremetal-provision.html">사용자 정의 Bare Metal Server</a></li>
  <li><a href="bare-metal-sap-applications.html">IBM Cloud SAP-Certified Infrastructure</a></li>
  </td>
 <tr>
   <td>7. Bare Metal Server 구성</td>
   <td>현재 서버를 구성할 준비가 되었습니다. *구성*의 주제를 참조하십시오.</td>
   </td>
   </tr>
   </TBODY>
   </table>
