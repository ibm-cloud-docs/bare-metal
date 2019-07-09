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

# IP アドレスの割り当てとバインド
{: #bm-assigning-and-binding-ip-addresses
次の情報を使用してサーバーの IP アドレスをサーバーに割り当て、必要に応じて、2 次 IP アドレスをサーバーにバインドします。
{: shortdesc}

## サーバー IP アドレスの割り当て
{: #bm-assign-ip-address}

{{site.data.keyword.cloud}} では、次のアドレスでサーバーが構成されます。
プライベート・ネットワークでは IPv4 アドレス。
プライベート・ネットワークでの
低レベル管理アクセスでは IPv4 アドレス。
要求された場合はパブリック IPv4 アドレス。

要求があれば、パブリック・ネットワークで IPv6 アドレスを使用することも可能です。 これらの IP アドレスはすべて、まとめて **1 次 IP アドレス **と呼ばれます。

[{{site.data.keyword.cloud_notm}} コンソール](https://cloud.ibm.com){: external}から ** 2 次サブネット** を購入すると、
サーバーにバインドする IP アドレスを増やすことができます。ユーザーがカスタマー・ポータルから購入し自分で管理する IP アドレスは **2 次 IP アドレス**と呼ばれます。

IP アドレスの取得について詳しくは、「[サブネットおよび IP](https://cloud.ibm.com/docs/infrastructure/subnets/){: external}」を参照してください。


## 2 次 IP アドレスのバインド
{: #bm-bind-secondary-ip-address}

2 次サブネットを購入した後、1 つ以上の IP アドレスを使用するようにオペレーティング・システムを構成する必要があります。 IP アドレスの構成方法は　オペレーティング・システムごとに異なりますが、通常は「インターフェース別名」のセットアップと呼ばれています。
