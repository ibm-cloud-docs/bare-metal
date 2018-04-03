---



copyright:
  years: 2016
lastupdated: "2016-01-19"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# {{site.data.keyword.baremetal_short}} 시작하기

{{site.data.keyword.baremetal_long}}에서는 성능과 제어를 제공합니다. {{site.data.keyword.baremetal_short}}는 하이퍼바이저에서 실행되지 않으며 하드웨어 자원에 대한 하위 레벨의 액세스 권한을 얻습니다. 또한 다른 고객과 서버를 공유하지 않으며 사용자 단독으로 사용합니다.
{:shortdesc}

{{site.data.keyword.baremetal_short}} 작성 시, 프로세서 및 지역에서 운영 체제 및 하드 드라이브까지 사양을 사용자 정의할 수 있습니다.

{{site.data.keyword.baremetal_short}}를 프로비저닝하려면 다음을 수행하십시오.
  1. **컴퓨팅 > {{site.data.keyword.baremetal_short}}**로 이동하여 **추가**를 클릭하십시오.
  2. {{site.data.keyword.baremetal_short}} 인스턴스를 프로비저닝할 위치를 선택하십시오. 이는 {{site.data.keyword.Bluemix}} 지역 중 하나에 위치한 데이터 센터입니다.
  3. 서버에 대한 구성을 선택하십시오. 이 구성은 이 인스턴스에 대해 작성된 모든 서버에 적용됩니다.
  4. 사용자가 해당 인스턴스에 대해 작성할 서버의 수를 선택하십시오. 각 서버에 대해 고유 호스트 이름을 입력하십시오.
  5. **선택사항:** 서버를 구성하기 위해 정의한 스크립트 또는 텍스트 파일에 URL을 입력하십시오. 프로비저닝 스크립트는 HTTPS 프로토콜을 사용해야 합니다. 이 스크립트는 인스턴스가 프로비저닝된 후에 다운로드되고 실행됩니다(가능한 경우). URL이 실행 가능한 스크립트와 연관되지 않은 경우, 스크립트가 다운로드만 됩니다.
  6. 서버에 대한 운영 체제를 선택하십시오. 이 운영 체제는 이 인스턴스에 대해 작성된 모든 서버에 적용됩니다.

한 시간 내에 {{site.data.keyword.baremetal_short}}가 프로비저닝되어 사용할 수 있게 됩니다.
