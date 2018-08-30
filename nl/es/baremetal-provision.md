---



copyright:
  years: 2017, 2018
lastupdated: "2018-07-06"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Creación de un servidor nativo personalizado
{: #ordering-baremetal-server}

Efectúe los pasos siguientes para crear un {{site.data.keyword.baremetal_short}} personalizado.

1. Abra el [catálogo de {{site.data.keyword.cloud_notm}}](https://console.bluemix.net/catalog/){:target="_blank"}.   
2. Seleccione el servidor nativo.
3. Pulse Crear.
4. Debajo de la lista de servidores, busque la sentencia: **¿Está interesado en otras opciones de configuración? Pulse aquí**. Seleccione esta opción. Se visualiza el formulario de servidor personalizado.
1. Seleccione una ubicación del centro de datos para el servidor.
* Seleccione un servidor desde las tres categorías de servidores pulsando el enlace **Precio desde**.
  * Servidores certificados por SAP (Para obtener más información sobre el suministro de un Servidor certificado por SAP, consulte [Infraestructura certificada por SAP de {{site.data.keyword.cloud_notm}}](/docs/bare-metal/bare-metal-sap-applications.html))
  * Servidores de varios núcleos con un solo procesador
  * Servidores de varios núcleos de procesador dual

* Seleccione una de las opciones de configuración. **Centro de datos**, **RAM** y **Sistema operativo** son campos necesarios. Los otros campos son opcionales. Para obtener más información sobre los campos opcionales, consulte las **[Opciones de configuración de servidor adicionales](#addl-server-options)**.

    **Nota**: Se muestra un mensaje de error si existe un conflicto entre el servidor y el sistema operativo. Por ejemplo, si se selecciona Linux en un servidor Microsoft SQL.
* Pulse **Añadir a pedido**. Se muestra la página de pago.

  En la página Extraer, puede volver a la página de configuración pulsando una de las opciones de Reconfigurar.
* En la sección Configuración avanzada del sistema, especifique opciones de configuración adicionales. Para obtener más información, consulte **[Configuración avanzada del sistema](#adv-system-config)**.

*   Pulse los recuadros de selección **Términos de los servicios en la nube** y **Acuerdo de servicio de terceros**.
*   Confirme o especifique la información sobre el pago y pulse **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla, ya que también es su recibo del pedido de suministro.

  También puede guardar este pedido sin adquirirlo pulsando **Guardar como presupuesto**.

 Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico de suministro completado incluye un enlace a la página *Detalles del dispositivo* después de que inicie una sesión en {{site.data.keyword.cloud_notm}}. También puede iniciar la sesión directamente en el {{site.data.keyword.slportal}}.

 ## Opciones de configuración de servidor adicionales
 {: #addl-server-options}

 Tiene opciones adicionales disponibles al suministrar el servidor nativo, por ejemplo el ancho de banda público, las velocidades de puerto de enlace ascendente, las direcciones IP secundarias públicas, etc. La Tabla 1 describe las opciones adicionales.


 | **Campo** | **Descripción** |
 |-------------------|---------------|
 |Seguridad del servidor|Por ejemplo, Trusted Execution Technology (Intel TXT)|
 |Software Guard Extensions|Seguridad aumentada para código y datos confidenciales (Intel SGX). <br><br>Consulte [Suministro de un servidor nativo con Intel SGX](../bare-metal/bare-metal-provision-SGX.html).|
 |RAM|Elija un nivel de RAM que cumpla con sus necesidades de servidor.|
 |Sistema operativo |Seleccione entre CentOS, FreeBSD, Microsoft, Red Hat, Ubuntu u Otro. |
 |Unidades de disco duro |Utilice la herramienta de la interfaz de usuario para configurar los discos duros rellenando los campos en función de la selección del sistema operativo. <br><br> También puede seleccionar para utilizar una unidad Intel Optane SSD. Consulte [Suministro de un Intel Optane SSD DC P4800X](../bare-metal/bm-provision_ssd.html).
 |Ancho de banda público |Determina la cantidad de datos que se pueden transferir a través de la interfaz pública durante un mes. Para entornos de prueba, que necesitan transferir datos de instalación a través de esta interfaz, los valores deben adaptarse más allá de la cantidad de datos transferidos inicialmente. Considere la [red de entrega de contenidos de {{site.data.keyword.cloud_notm}}](https://www.ibm.com/cloud/cdn) para enviar una carga de datos inicial a uno de los centros de datos de {{site.data.keyword.cloud_notm}}. Todos los {{site.data.keyword.baremetal_short}} se pueden actualizar para incluir un ancho de banda sin límite de uso (ilimitado). Todos los dispositivos sin límite de uso están en puertos privados y dedicados.|
 |Velocidades de puerto de enlace ascendente |Determina la velocidad de las interfaces internas y externas. |
 |Direcciones IP secundarias públicas |Asigna más direcciones IP al servidor. Según el caso, puede necesitar que se asignen más direcciones IP al servidor. Existen más direcciones IPv4 disponibles en cantidades de 1, 2, 4, 8, 16 o 32. |
 |Direcciones IPv6 primarias |Asignadas a las interfaces internas y externas del servidor. |
 |Direcciones IPv6 estáticas públicas |Asigna más direcciones IPv6 de un bloque /64. |
 |Complementos de sistema operativo|Seleccione opciones como, por ejemplo, VMware, soluciones de copia de seguridad, panel de control, base de datos, cortafuegos de hardware y software, protección antivirus y de spyware, protección y detección de intrusión. <br><br>Se recomienda encarecidamente que su departamento de seguridad corporativa se ponga de acuerdo con el soporte de {{site.data.keyword.cloud_notm}} para comentar los detalles de estas opciones.
 |Evault |Una herramienta de copia de seguridad basada en agente que se puede instalar en el servidor para replicar copias de seguridad entre servidores. |
 |Complementos de servicio|Seleccione los complementos de servicio como, por ejemplo, la supervisión, la respuesta automática y el seguro.|
 {: caption="Tabla 1. Opciones de servidor adicionales" caption-side="top"}

## Configuración avanzada del sistema
{: #adv-system-config}

Los campos bajo **Configuración avanzada del sistema** completan el proceso de suministro.

| **Campo** | **Descripción** |
|---|---|
| Nombre de host | Un nombre permanente o temporal para el servidor, por ejemplo, _server1_. **Nota**: Si está suministrando un servidor certificado por SAP, el nombre de host de SAP debe estar formado por un máximo de 13 caracteres alfanuméricos. Para obtener más información sobre los nombres de host de SAP, consulte [Notas de SAP 611361](https://launchpad.support.sap.com/#/notes/2611361) y [129997](https://launchpad.support.sap.com/#/notes/129997). Requiere un ID S-user de SAP. |
| Dominio | Nombre del subdominio, que no debería estar en conflicto con un nombre de dominio de Internet, por ejemplo, _test.acme.com_. |
| Selección de VLAN | Si hay una VLAN bajo su cuenta porque ya ha solicitado al menos un servidor, puede añadir el nuevo servidor a la VLAN. |
| Script de suministro | Puede proporcionar un script que le permita automatizar algunos pasos después del suministro. |
| Claves SSH | Puede proporcionar la clave pública de su clave SSH, que le permitirá iniciar sesión en el servidor una vez que se haya suministrado. |
{: caption="Tabla 2. Configuración avanzada del sistema" caption-side="top"}

 Consulte el soporte de {{site.data.keyword.cloud_notm}} para obtener más información.

 **NOTA:** Puede solicitar subredes secundarias con los dispositivos de cálculo. Sin embargo, si solicita subredes secundarias, se reclaman cuando se reclama el dispositivo de cálculo. Si solicita la subred secundaria independientemente (no como una opción de complemento de un pedido de cálculo), puede conservar la subred hasta que la cancele explícitamente. Es importante recordar esta distinción, para que no pierda de forma inadvertida algunas direcciones IP si se reclama un dispositivo de cálculo.

## Pasos siguientes
Una vez suministrado el dispositivo de {{site.data.keyword.baremetal_short}}, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión de {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
