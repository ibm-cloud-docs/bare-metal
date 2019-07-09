---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-02"

keywords: provision Intel Optane compatible bare metal server, Intel Optane, optane 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Suministro de un servidor nativo compatible con Intel Optane
{: #bm-provision-optane-server}

Para suministrar un servidor nativo con una unidad de Intel Optane:
1. Utilice el procedimiento: [Creación de un servidor nativo personalizado](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server).
* Seleccione las siguientes opciones en el formulario de pedido:

|Sección|Opción a seleccionar
|------|------|
|Región-Centro de datos|Para utilizar la unidad Intel Optane, seleccione uno de los centros de datos siguientes:<br>Europa - AMS03, FRA02, LON02, OSL01<br>América del Norte sur DAL09, DAL10, DAL12<br>Asia-Pacífico - MEL01<br>América del Norte este - MON01, TOR01, WDC04<br>América del Norte oeste - SJC03<br>|
|Servidor|1. Seleccione **Todos los servidores**<br>2. Seleccione *Procesadores duales*<br>3. Seleccione uno de los servidores siguientes<br>-Intel Xeon 4110 con un máximo de 12 unidades<br>-Intel Xeon 5120 con un máximo de 12 unidades<br>-Intel Xeon 6140 con un máximo de 12 unidades<br>-Intel Xeon E5-2620 v4 con soporte para GPU<br>-Intel Xeon E5-2650 v4 con soporte para GPU<br>-Intel Xeon E5-2690 v4 con soporte para GPU<br><br>  **Nota**: Si selecciona E5-2620 v4, E5-2650 v4, o E5-2650 v4, la unidad Intel Optane sustituye a la GPU, por lo que no puede tener una GPU y una unidad de Intel Optane.|
|Sistema operativo|Para los controladores Optane proporcionados por Intel, los siguientes sistemas operativos están certificados por Intel:<br>Windows Server 2016 (todas las ediciones)<br>Windows Server 2012 R2 (todas las ediciones)<br><br>Para controladores de bandeja de entrada, de código abierto y distintos de Intel, la compatibilidad y la funcionalidad están validadas pero no certificadas:<br>Red Hat Enterprise Linux 7.x (64 bits)<br>Red Hat Enterprise Linux 6.x (64 bits).
|Complementos de imagen| Seleccione una unidad Intel Optane para el primero y el segundo componentes de PCIe.|
