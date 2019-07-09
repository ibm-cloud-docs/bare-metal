---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-25"

keywords: bare metal, 3ware 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Verificando o funcionamento de sua matriz RAID do 3ware
{: #bm-check-health-3ware-raid}

Com o 3ware, é possível usar uma interface do navegador. No entanto, a menos que você acesse a interface localmente, isso pode
ser um risco de segurança. Portanto, use a interface da linha de comandos.

É possível fazer download dos utilitários da CLI do 3ware usando o [Repositório de plug-ins da CLI do IBM Cloud
](https://plugins.cloud.ibm.com/ui/repository.html#cf-plugins). Para obter mais informações sobre o utilitário da CLI, consulte [Plug-in da CLI VPN para CLI cf](https://cloud.ibm.com/docs/cli?topic=cloud-cli-vpn_cli_for_cf).

**Referência rápida de comando para ferramentas da CLI do 3ware**

Esses dispositivos devem ser seguidos por um número que identifique quais dispositivos estão sendo consultados.

tw_cli /c0 show (A saída mostra as informações necessárias para conhecer o funcionamento da matriz RAID)

./tw_cli /c1 show

Exemplo:

    Unit  UnitType  Status         %Cmpl  Stripe  Size(GB)  Cache  AVerify  IgnECC

    ------------------------------------------------------------------------------

    u0    RAID-5    OK             -      64K     465.641   OFF    OFF      OFF    

    Port   Status           Unit   Size        Blocks        Serial

    ---------------------------------------------------------------

    p0     OK               u0     233.76 GB   490234752     WD-WCANY1727093

    p1     OK               u0     233.76 GB   490234752     WD-WCANY1622544

    p2     OK               u0     233.76 GB   490234752     WD-WCANY1657267

    p3     NOT-PRESENT      -      -           -             -

*observe o seguinte:

c = controlador<br/>
O controlador pode ser 0 ou 1<br/>
u = unidade<br/>
O número da unidade depende das matrizes de número. É 0 na maioria dos casos.<br/>
p = porta<br/>
Porta denota o número da porta. Na maioria dos casos, é 0 - 4.
