---

copyright:
  years: 1994, 2019
lastupdated: "2019-06-17"

keywords: server IP addresses, bare metal, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# IP 주소 지정 및 바인딩
{: #bm-assigning-and-binding-ip-addresses
다음 정보를 사용하면 서버 IP 주소를 서버에 지정하고 2차 IP 주소를 서버에 바인드(필요한 경우)할 수 있습니다.
{: shortdesc}

## 서버 IP 주소 지정
{: #bm-assign-ip-address}

{{site.data.keyword.cloud}}는 사설 네트워크의 IPv4 주소, 사설 네트워크의 하위 레벨 관리 액세스를 위한 IPv4 주소 및 공용 IPv4 주소(요청한 경우) 등의 주소를 사용하여 서버를 구성합니다. 

요청된 경우 공용 네트워크에서 IPv6 주소를 사용할 수 있습니다. 해당 IP 주소는 모두
집합적으로 **1차 IP 주소**라고 합니다.

[{{site.data.keyword.cloud_notm}} 콘솔](https://cloud.ibm.com){: external}을 통해 **2차 서브넷**을 구매한 후 추가 IP 주소를 서버에 바인드할 수 있습니다. 고객 포털을 통해 구매하고 사용자가 관리하는
IP 주소는 **2차 IP 주소**라고 합니다.

IP 주소 확보에 대한 자세한 정보는 [서브넷 및 IP](https://cloud.ibm.com/docs/infrastructure/subnets/){: external}를 참조하십시오.


## 2차 IP 주소 바인딩
{: #bm-bind-secondary-ip-address}

2차 서브넷을 구매한 다음 하나 이상의 IP 주소를 사용하도록
운영 체제를 구성해야 합니다. 운영 체제마다 IP 주소를 서로 다르게 구성하지만, 일반적으로 이 작업은 "인터페이스 별명" 설정이라고 합니다.
