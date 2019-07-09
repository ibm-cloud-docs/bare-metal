---

copyright:
  years: 2018, 2019
lastupdated: "2018-04-02"

keywords: provision, sgx, provision server Intel SGX architecture, Intel SGX architecture

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Suministro de un servidor nativo con arquitectura Intel SGX
{: #bm-server-provision-sgx}

1. Utilice el procedimiento: [Creación de un servidor nativo personalizado](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server).
* Seleccione las siguientes opciones en el formulario de pedido:

|Sección|Opción a seleccionar|
|------|------|
|Servidor|Un solo procesador<br> Intel Xeon E3-1270 v6 con almacenamiento de hasta 4 unidades|
|Imagen|- Windows Server 2016 Standard Edition (64 bits)<br>- Windows Server 2016 Standard Edition (64 bits)<br> - Windows Server 2016 Datacenter Edition (64 bits) <br>- CentOS 7.x (64 bits) <br> - Ubuntu Linux 16.04 LTS Xenial Xerus (64 bits)<br>- CentOS 7.x (64 bits) <br>- Red Hat Enterprise Linux 7.x (64 bits) (licencia por procesador)|
|Complementos de imagen|Software Guard Extensions|
