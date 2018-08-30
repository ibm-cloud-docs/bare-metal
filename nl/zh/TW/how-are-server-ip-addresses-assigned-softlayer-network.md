---

copyright:
  years: 1994, 2018
lastupdated: "2018-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 指派伺服器 IP 位址

{{site.data.keyword.cloud}} 會為伺服器配置專用網路上的 IPv4 位址、專用網路上進行低階管理存取之用的 IPv4 位址，以及在要求的情況下配置公用 IPv4 位址。如果要求，會提供公用網路上的 IPv6 位址。所有這些 IP 位址統稱為**主要 IP 位址**。

在您透過[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com) 購買**次要子網路**之後，可以將更多 IP 位址連結至伺服器。您透過「客戶入口網站」購買，並且由您管理的 IP 位址，稱為**次要 IP 位址**。

如需獲得 IP 位址的相關資訊，請參閱[子網路和 IP](https://console.bluemix.net/docs/infrastructure/subnets/)。


# 連結次要 IP 位址

購買次要子網路之後，您需要將作業系統配置成使用一個以上的 IP 位址。每一個作業系統會以不同方式配置 IP 位址，但通常稱為「介面別名」。 
