---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Verificando o funcionamento de sua matriz RAID do 3ware

Com o 3ware, é possível usar uma interface do navegador. No entanto, a menos que você acesse a interface localmente, isso pode
ser um risco de segurança. Portanto, use a interface da linha de comandos.

<!--You can download the 3ware CLI utilities the software Library, located in the bottom of Customer Portal.  Please check http://downloads.service.softlayer.com for the latest version (VPN access required to access the downloads page). -->

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
O número da unidade depende de matrizes de número. É 0 na maioria dos casos.<br/>
p = porta<br/>
Port denota o número da porta. Na maioria dos casos, é 0 - 4.
