---

copyright:
  years: 1994, 2018
lastupdated: "2018-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# サーバー IP アドレスの割り当て

{{site.data.keyword.cloud}} では、サーバーは、プライベート・ネットワークでは IPv4 アドレスで構成されます。この IPv4 アドレスは、プライベート・ネットワークで低レベル管理アクセスに使用するものですが、要求があれば、パブリック IPv4 アドレスで構成されます。
要求があれば、パブリック・ネットワークで IPv6 アドレスを使用することも可能です。これらの IP アドレスはすべて、まとめて **1 次 IP アドレス **と呼ばれます。

[カスタマー・ポータル ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com) から ** 2 次サブネット** を購入すれば、サーバーにバインドする IP アドレスを増やすことができます。ユーザーがカスタマー・ポータルから購入し自分で管理する IP アドレスは **2 次 IP アドレス**と呼ばれます。

IP アドレスの取得について詳しくは、「[サブネットおよび IP](https://console.bluemix.net/docs/infrastructure/subnets/)」を参照してください。


# 2 次 IP アドレスのバインド

2 次サブネットを購入した後、1 つ以上の IP アドレスを使用するようにオペレーティング・システムを構成する必要があります。IP アドレスの構成方法は　オペレーティング・システムごとに異なりますが、通常は「インターフェース別名」のセットアップと呼ばれています。 
