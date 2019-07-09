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

# 分配和绑定 IP 地址
{: #bm-assigning-and-binding-ip-addresses
使用以下信息将服务器 IP 地址分配到服务器，并根据需要将辅助 IP 地址绑定到服务器。
{: shortdesc}

## 分配服务器 IP 地址
{: #bm-assign-ip-address}

{{site.data.keyword.cloud}} 使用以下地址配置服务器：
专用网络上的 IPv4 地址
专用网络上用于低级别管理访问的 IPv4 地址
公共 IPv4 地址（如果请求）。

可以使用公用网络上的 IPv6 地址（如果请求）。所有这些 IP 地址统称为**主 IP 地址**。

通过 [{{site.data.keyword.cloud_notm}} 控制台](https://cloud.ibm.com){: external}购买**辅助子网**后，可以将更多 IP 地址绑定到服务器。您通过客户门户网站购买并由您管理的 IP 地址称为**辅助 IP 地址**。

有关获取 IP 地址的更多信息，请参阅[子网和 IP](https://cloud.ibm.com/docs/infrastructure/subnets/){: external}。


## 绑定辅助 IP 地址
{: #bm-bind-secondary-ip-address}

购买辅助子网后，需要将操作系统配置为使用一个或多个 IP 地址。每个操作系统配置 IP 地址的方式不同，但通常称为设置“接口别名”。
