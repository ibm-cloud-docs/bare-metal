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

# Designando e ligando endereços IP
{: #bm-assigning-and-binding-ip-addresses
Use as informações a seguir para designar um endereço IP de servidor ao seu servidor e
ligar um endereço IP secundário ao seu servidor, se necessário.
{: shortdesc}

## Designando endereços IP do servidor
{: #bm-assign-ip-address}

O {{site.data.keyword.cloud}} configura servidores com estes endereços:
Um endereço IPv4 na rede privada
Um endereço IPv4 para acesso de gerenciamento de nível inferior
na rede privada
Um endereço IPv4 público, se solicitado.

Um endereço IPv6 na rede pública estará disponível, se solicitado. Todos esses endereços IP são
referidos coletivamente como **Endereços IP primários**.

Mais endereços IP poderão ser ligados aos servidores após a compra de **Sub-redes
secundárias** por meio da [Console do {{site.data.keyword.cloud_notm}}](https://cloud.ibm.com){: external}. Os endereços IP comprados por meio do Portal do cliente e gerenciados
por você são chamados de **Endereços IP secundários**.

Para obter mais informações sobre a aquisição de endereços IP, consulte [Subnets e IPs](https://cloud.ibm.com/docs/infrastructure/subnets/){: external}.


## Ligando endereços IP Secundários
{: #bm-bind-secondary-ip-address}

Depois de comprar uma sub-rede secundária, é necessário configurar o sistema operacional para usar um ou mais endereços IP. Cada sistema operacional configura os endereços IP de forma diferente, mas geralmente isso é conhecido como configuração de
"aliases de interface".
