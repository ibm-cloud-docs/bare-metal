---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Suministro de un servidor nativo compatible con Intel Optane
Para suministrar un servidor nativo con una unidad de Intel Optane:
1. Utilice el procedimiento: [Creación de un servidor nativo personalizado](../bare-metal/baremetal-provision.html).
* Seleccione las siguientes opciones en el formulario de pedido:

|Sección|Opción a seleccionar
|------|------|
|Centro de datos|Para utilizar la unidad Intel Optane, seleccione uno de los centros de datos siguientes:<br>AMS03 - Ámsterdam<br>DAL09 - Dallas<br>DAL10 - Dallas<br>DAL12 - Dallas<br>FRA02 - Frankfurt<br>LON02 - Londres<br>MEL01 - Melbourne<br>MON01 - Montreal<br>OSL01 - Oslo<br>SJC03 - San José<br>TOR01 - Toronto<br>WDC04 - Washington, DC|
|Servidor|Los siguientes servidores son compatibles con la unidad Intel Optane<br>Intel Xeon 4110 con un máximo de 12 unidades<br>Intel Xeon 5120 con un máximo de 12 unidades<br>Intel Xeon 6140 con un máximo de 12 unidades<br>Intel Xeon E5-2620 v4 con GPU Support<br>Intel Xeon E5-2650 v4 con GPU Support<br>Intel Xeon E5-2690 v4 con GPU Support<br><br>  **Nota**: Si selecciona E5-2620 v4, E5-2650 v4, o E5-2650 v4, la unidad Intel Optane sustituye a la GPU, por lo que no puede tener una GPU y una unidad de Intel Optane.|
|Componentes PCIe| Seleccione una unidad Intel Optane para el primero y el segundo componentes de PCIe.|
|Sistema operativo|Para los controladores Optane proporcionados por Intel, los siguientes sistemas operativos están certificados por Intel:<br>Windows Server 2016 (todas las ediciones)<br>Windows Server 2012 R2 (todas las ediciones)<br><br>Para controladores de bandeja de entrada, de código abierto y distintos de Intel, la compatibilidad y la funcionalidad están validadas pero no certificadas:<br>Red Hat Enterprise Linux 7.x (64 bits)<br>Red Hat Enterprise Linux 6.x (64 bits).
