---

copyright:
  years: 1994, 2018
lastupdated: "2018-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Designando endereços IP do servidor

O {{site.data.keyword.cloud}} configura os servidores com um endereço IPv4 na rede
privada, um endereço IPv4 para acesso ao gerenciamento de baixo nível na rede privada e, se solicitado, um endereço IPv4 público.
Um endereço IPv6 na rede pública estará disponível, se solicitado. Todos esses endereços IP são
referidos coletivamente como **Endereços IP primários**.

Mais endereços IP podem ser ligados aos servidores após a compra de **Subnets secundárias** por meio do
[Portal do cliente ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de linkexterno")](https://control.softlayer.com). Os endereços IP comprados por meio do Portal do cliente e gerenciados

por você são chamados de **Endereços IP secundários**.

Para obter mais informações sobre a aquisição de endereços IP, consulte [Subnets e IPs](https://console.bluemix.net/docs/infrastructure/subnets/).


# Ligando endereços IP Secundários

Depois de comprar uma sub-rede secundária, é necessário configurar o sistema operacional para usar um ou mais endereços IP. 
Cada sistema operacional configura os endereços IP de forma diferente, mas geralmente isso é conhecido como configuração de
"aliases de interface". 
