---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: custom server, {{site.data.keyword.baremetal_short}}, {{site.data.keyword.Bluemix_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# Creación de un servidor nativo personalizado
{: #ordering-baremetal-server}

Efectúe los pasos siguientes para crear un {{site.data.keyword.baremetal_long}} personalizado.

## Suministro a través del catálogo de {{site.data.keyword.cloud_notm}}
{: #provision-through-the-catalog}

Efectúe los pasos siguientes para suministrar un {{site.data.keyword.baremetal_short}} a través de {{site.data.keyword.cloud_notm}}.

1. Abra el [catálogo de {{site.data.keyword.cloud_notm}}](https://cloud.ibm.com/catalog/){: external}.   
2. Seleccione {{site.data.keyword.baremetal_short}} en **Cálculo**.
3. Pulse Continuar.  Si no ve un botón Continuar, es posible que tenga que iniciar sesión.
4. Especifique la **cantidad** de servidores **idénticos** a suministrar. El valor predeterminado es 1. Si desea suministrar varios servidores con especificaciones _diferentes_, deberá suministrarlos por separado.
5. **Nombre de host** es un nombre permanente o temporal para los servidores, por ejemplo, baremetal01. Pulse **Información** para obtener detalles del formato.
6. **Dominio** es la serie de identificación que define el control administrativo dentro de Internet, por ejemplo, Customer-123456.cloud. Pulse **Información** para obtener detalles del formato.
7. **Facturación** es **Por horas** o **Mensual**.
8. Seleccione la **Ubicación**, la región y el centro de datos, donde desea ubicar el servidor.
9. Pulse **Todos los servidores** para ver una lista de procesadores (Single, Dual y Quad) y servidores certificados (SAP y VMware). Seleccione el servidor que mejor se adapte a su carga de trabajo.
10. Seleccione la **RAM**. Para algunos servidores, los valores predeterminados de RAM se basan en el modelo de CPU y no se pueden cambiar. 

Para los servidores certificados de SAP, la RAM y el sistema operativo predeterminado se basan en el servidor seleccionado. La opción de almacenamiento local también se basa en el servidor seleccionado.
{: note}

11. Escriba una clave pública opcional para su **clave SSH**, que puede utilizar para iniciar sesión en el servidor una vez suministrado.
12. Seleccione una **Imagen** (sistema operativo) para el servidor. Las opciones se basan en el servidor que ha seleccionado.
13. Expanda **Complementos** para seleccionar las opciones relacionadas con la configuración del servidor.
14. Los **Discos de almacenamiento** están preconfigurados en función del servidor seleccionado. Expanda **Complementos** para añadir volúmenes de almacenamiento en archivos o en bloques una vez se hayan suministrado los {{site.data.keyword.baremetal_short}}. 
15. En **Interfaz de red**, seleccione las opciones Velocidades de puerto de enlace ascendente y VLAN privada. Expanda **Complementos** para seleccionar las opciones adecuadas o utilice los valores predeterminados.
16. Revise el pedido en el Resumen del pedido.
17. Si tiene algún código promocional, introdúzcalo en **Aplicar código promocional**.
18. Haga clic en los acuerdos de servicio de terceros para ver si hay acuerdos en la lista.
19. Pulse **Crear** para suministrar el servidor. Se le redirigirá a una pantalla con el número de su pedido de suministro, que puede imprimir porque es también su recibo.

Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado.

El correo electrónico de _suministro completado_ incluye un enlace a la página *Detalles del dispositivo* para que pueda iniciar sesión en {{site.data.keyword.cloud_notm}}. También puede iniciar la sesión directamente en el {{site.data.keyword.slportal}}.

También tiene la opción de guardar el pedido como un presupuesto o de añadirlo a una estimación. Cuando guarda un presupuesto, se le envía un enlace a la dirección de correo electrónico asociada a su cuenta. Abra el enlace para ver la información de presupuesto guardada. Otra opción es ir a Gestionar > Facturación y uso y seleccionar Ventas > Presupuestos de dispositivos. Si tiene acceso, puede adquirir la oferta presupuestada pulsando el presupuesto y confirmando el pedido. Al añadir a las estimaciones, el coste propuesto de las configuraciones se añade a la calculadora de precios. Pulse **Información** para obtener más detalles sobre la calculadora de precios.

## Suministro a través del portal de clientes
Efectúe los pasos siguientes para suministrar un {{site.data.keyword.baremetal_short}} a través de {{site.data.keyword.slportal}}.

1. Inicie sesión en [{{site.data.keyword.slportal}}](control.softlayer.com){: external} utilizando sus credenciales exclusivas.
2. Vaya a **Cuenta** > **Realizar un pedido**.
3. Elija **Por horas** o **Mensual**.
3. Seleccione en la lista el centro de datos donde desea que se ubique el {{site.data.keyword.baremetal_short}} y después seleccione el servidor certificado (SAP o VMware) o el procesador (Single, Dual y Quad) pulsando en **PRECIO INICIAL**.
4. Especifique la **cantidad** de servidores _idénticos_ a suministrar. El valor predeterminado es 1. Si desea suministrar varios servidores con especificaciones _diferentes_, deberá suministrarlos por separado.
5. Seleccione la **RAM**. Para algunos servidores, los valores predeterminados de RAM se basan en el modelo de CPU y no se pueden cambiar. 

Para los servidores certificados de SAP, la RAM y el sistema operativo predeterminado se basan en el servidor seleccionado. La opción de almacenamiento local también se basa en el servidor seleccionado.
{: note}

6. Seleccione el sistema operativo.
7. Seleccione las unidades de disco duro y los complementos de sistema adicionales.
8. Pulse **Añadir a pedido** y se le redirigirá a confirmar el pedido.
9. Confirme o edite la información de dominio correspondiente al servidor. **Nombre de host** es un nombre permanente o temporal para los servidores, por ejemplo, baremetal01. 
10. Seleccione **Términos de los servicios en la nube** y el **Acuerdo de servicio de terceros**.
11. Si tiene algún código promocional, introdúzcalo en **Código promocional** y pulse **Aplicar**.
12. Confirme o especifique la información sobre el pago y pulse **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro, que puede imprimir porque es también su recibo. 

Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico completo de suministro incluye un enlace con la página *Detalles del dispositivo*, después de iniciar una sesión en {{site.data.keyword.Bluemix_notm}}. También puede iniciar la sesión directamente en el {{site.data.keyword.slportal}}.

## Pasos siguientes
Una vez suministrado el dispositivo de {{site.data.keyword.baremetal_short}}, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión de {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
