---

copyright:
  years: 1994, 2018
lastupdated: "2018-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 分配服务器 IP 地址

{{site.data.keyword.cloud}} 可将服务器配置为使用专用网络上的 IPv4 地址、专用网络上用于低级别管理访问的 IPv4 地址，以及公共 IPv4 地址（如果请求）。可以使用公用网络上的 IPv6 地址（如果请求）。所有这些 IP 地址统称为**主 IP 地址**。

通过[客户门户网站 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://control.softlayer.com) 购买**辅助子网**后，可以将更多 IP 地址绑定到服务器。您通过客户门户网站购买并由您管理的 IP 地址称为**辅助 IP 地址**。

有关获取 IP 地址的更多信息，请参阅[子网和 IP](https://console.bluemix.net/docs/infrastructure/subnets/)。


# 绑定辅助 IP 地址

购买辅助子网后，需要将操作系统配置为使用一个或多个 IP 地址。每个操作系统配置 IP 地址的方式不同，但通常称为设置“接口别名”。 
