---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-12"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Comprobación del estado de la matriz RAID 3ware

3ware le permite utilizar una interfaz del navegador. Sin embargo, a menos que acceda a la interfaz de forma local, puede ser un riesgo de seguridad. Por lo tanto, se recomienda utilizar la interfaz de línea de mandatos.

<!--You can download the 3ware CLI utilities the software Library, located in the bottom of Customer Portal.  Please check http://downloads.service.softlayer.com for the latest version (VPN access required to access the downloads page). -->

**Referencia rápida de mandato para herramientas de CLI de 3ware**

Estos dispositivos deben ir seguidos por un número que indique cuál se consulta.

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
El número de unidad depende del número de matrices. En la mayoría de los casos, es 0.<br/>
p = puerto<br/>
El puerto indica el número de puerto. En la mayoría de los casos, es 0-4.
