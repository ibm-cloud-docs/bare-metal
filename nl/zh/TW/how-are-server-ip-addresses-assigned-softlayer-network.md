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

# 指派及連結 IP 位址
{: #bm-assigning-and-binding-ip-addresses

請使用下列資訊，指派伺服器 IP 位址給您的伺服器，並且視需要連結次要 IP 位址給您的伺服器。
{: shortdesc}

## 指派伺服器 IP 位址
{: #bm-assign-ip-address}

{{site.data.keyword.cloud}} 會為伺服器配置下列位址：
專用網路上的 IPv4 位址
專用網路上低階管理存取用的 IPv4 位址
公用 IPv4 位址（如果要求的話）。

如果要求，會提供公用網路上的 IPv6 位址。所有這些 IP 位址統稱為**主要 IP 位址**。

在您透過[{{site.data.keyword.cloud_notm}} 主控台](https://cloud.ibm.com){: external}購買**次要子網路**之後，可以將更多 IP 位址連結至伺服器。您透過「客戶入口網站」購買，並且由您管理的 IP 位址，稱為**次要 IP 位址**。

如需獲得 IP 位址的相關資訊，請參閱[子網路和 IP](https://cloud.ibm.com/docs/infrastructure/subnets/){: external}。


## 連結次要 IP 位址
{: #bm-bind-secondary-ip-address}

購買次要子網路之後，您需要將作業系統配置成使用一個以上的 IP 位址。每一個作業系統會以不同方式配置 IP 位址，但通常稱為「介面別名」。
