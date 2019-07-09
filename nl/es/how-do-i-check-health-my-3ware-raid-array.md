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

# Comprobación del estado de la matriz RAID 3ware
{: #bm-check-health-3ware-raid}

Con 3ware, puede utilizar una interfaz de navegador. Sin embargo, a menos que acceda a la interfaz de forma local, puede ser un riesgo de seguridad. Por lo tanto, utilice la interfaz de línea de mandatos.

Puede descargar los programas de utilidad de CLI de 3ware del [Repositorio de plugins de CLI de IBM Cloud
](https://plugins.cloud.ibm.com/ui/repository.html#cf-plugins). Para obtener más información sobre el programa de utilidad de CLI, consulte [Plug-in de CLI de VPN para la CLI cf](https://cloud.ibm.com/docs/cli?topic=cloud-cli-vpn_cli_for_cf).

**Referencia rápida de mandato para herramientas de CLI de 3ware**

Estos dispositivos deben ir seguidos por un número que identifica a los dispositivos que se están consultando.

tw_cli /c0 show (la salida muestra la información necesaria para conocer el estado de la matriz RAID)

./tw_cli /c1 show

Ejemplo:

    Unit  UnitType  Status         %Cmpl  Stripe  Size(GB)  Cache  AVerify  IgnECC

    ------------------------------------------------------------------------------

    u0    RAID-5    OK             -      64K     465.641   OFF    OFF      OFF    

    Port   Status           Unit   Size        Blocks        Serial

    ---------------------------------------------------------------

    p0     OK               u0     233.76 GB   490234752     WD-WCANY1727093

    p1     OK               u0     233.76 GB   490234752     WD-WCANY1622544

    p2     OK               u0     233.76 GB   490234752     WD-WCANY1657267

    p3     NOT-PRESENT      -      -           -             -

*tenga en cuenta lo siguiente:

c = controlador<br/>
El controlador puede ser 0 o 1<br/>
u = unidad<br/>
El número de unidad depende del número de matrices. En la mayoría de los casos es 0.<br/>
p = puerto<br/>
El puerto denota el número de puerto. En la mayoría de los casos, es 0-4.
