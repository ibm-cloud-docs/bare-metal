---

copyright:
  years: 1994, 2018
lastupdated: "2018-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 서버 IP 주소 지정

{{site.data.keyword.cloud}}에서는 사설 네트워크의 IPv4 주소,
사설 네트워크의 하위 레벨 관리 액세스를 위한 IPv4 주소 및 요청된 경우
공용 IPv4 주 소를 사용하여 서버를 구성합니다.
요청된 경우 공용 네트워크에서 IPv6 주소를 사용할 수 있습니다. 해당 IP 주소는 모두
집합적으로 **1차 IP 주소**라고 합니다.

[고객 포털
![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com)을 통해 **2차 서브넷**을 구매한 후 추가 IP 주소를 서버에 바인드할 수 있습니다. 고객 포털을 통해 구매하고 사용자가 관리하는
IP 주소는 **2차 IP 주소**라고 합니다.

IP 주소 확보에 대한 자세한 정보는 [서브넷 및 IP](https://console.bluemix.net/docs/infrastructure/subnets/)를 참조하십시오.


# 2차 IP 주소 바인딩

2차 서브넷을 구매한 다음 하나 이상의 IP 주소를 사용하도록
운영 체제를 구성해야 합니다. 운영 체제마다 IP 주소를 서로 다르게 구성하지만, 일반적으로 이 작업은 "인터페이스 별명" 설정이라고 합니다. 
