---



copyright:
  years: 2017
lastupdated: "2017-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Suministro de servidores nativos

## Antes de empezar
Tiene dos opciones para suministrar {{site.data.keyword.baremetal_long}} públicos. La primera es a través del catálogo de {{site.data.keyword.cloud}} y la segunda a través del {{site.data.keyword.slportal_full}}. El catálogo y el {{site.data.keyword.slportal}} requieren ID de inicio exclusivos. El nombre de usuario y la contraseña del catálogo no funcionarán para iniciar una sesión en el portal y viceversa.
{:shortdesc}

Antes de empezar, asegúrese de que dispone de las credenciales del catálogo de {{site.data.keyword.cloud_notm}} o del {{site.data.keyword.slportal}}. 
  
**Nota:** para el catálogo de {{site.data.keyword.cloud_notm}}, debe tener una cuenta actualizada para pedir {{site.data.keyword.baremetal_short}}. Para obtener más información sobre cómo actualizar la cuenta, consulte [Cambiar a IBMid](https://console.ng.bluemix.net/docs/admin/softlayerlink.html).
  
## Inicio de sesión 
Asegúrese de que está conectado, ya sea a través del catálogo de {{site.data.keyword.cloud_notm}} o del {{site.data.keyword.slportal}}: 

  <table>
   <CAPTION>Tabla 1. Elija una ubicación de inicio de sesión</CAPTION>
   <THEAD>
   <TR>
   <th>Si desea iniciar sesión con...</th>
   <th>Realice lo siguiente:</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Catálogo de IBM Cloud</td>
   <td>
   <ol>
   <li>Abra una nueva ventana del navegador y escriba <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>.</li>
   <li>Pulse el enlace <b>Iniciar sesión</b>. </li>
   <li>Escriba su correo electrónico o IBMid y pulse <b>Continuar</b>.</li>
   <li>Escriba su contraseña y pulse <b>Iniciar sesión</b>.</li>
   <li>Seleccione <b>Infraestructura</b> > <b>Cálculo</b>.</li>
   <li>Pulse el mosaico <b>{{site.data.keyword.baremetal_short}}</b>.</li>
   <li>Pulse <b>Crear</b>. Se abrirá la página principal del {{site.data.keyword.slportal}}.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Portal del cliente</td>
   <td>
   <ol>
   <li>Abra una nueva ventana del navegador y escriba <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Escriba su nombre de usuario y contraseña y pulse <b>Iniciar sesión</b>. O bien, pulse <b>Iniciar sesión con ID de IBM</b>. A continuación, escriba su correo electrónico o IBMid y pulse <b>Continuar</b>. Escriba su contraseña y pulse <b>Iniciar sesión</b>. Se abrirá la página principal del {{site.data.keyword.slportal}}.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Suministro de un servidor nativo
{: #ordering-baremetal-server}
Una vez que haya iniciado sesión, puede empezar a suministrar un dispositivo de {{site.data.keyword.baremetal_short}}. Puede suministrar el dispositivo de {{site.data.keyword.baremetal_short}} a través del menú **Dispositivos** o del icono **Dispositivos**.

### Suministro de un servidor nativo a través del icono de dispositivos
Para suministrar el dispositivo de {{site.data.keyword.baremetal_short}} mediante el icono *Dispositivos*, siga estos pasos:

1.  En el {{site.data.keyword.slportal}}, localice la sección **Pedido** y pulse **Dispositivos**.
2.  En la página Dispositivos, pulse **Por hora** o **Mensualmente** en {{site.data.keyword.baremetal_short}}.
3.  Seleccione el **Centro de datos**, desplácese a través de la página y pulse el enlace **Precio desde** para seleccionar el servidor. 
4.  Rellene la información de la página **Configure el dispositivo de {{site.data.keyword.baremetal_short}}** y pulse el botón **Añadir a pedido**. Consulte [Configuración del dispositivo de {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) para obtener más información sobre cómo configurar el servidor. Una vez verificado el pedido, se le redirigirá a la página de **pago**.
5.  Especifique la **Configuración avanzada del sistema** para el servidor. Consulte [Configuración del dispositivo de {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) para obtener más información sobre cómo hacerlo.
6.  Pulse los recuadros de selección **Términos de servicio de la nube** y **Acuerdo de servicio de terceros**.
7.  Confirme o especifique la información sobre el pago y pulse el botón **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla, ya que también es su recibo del pedido de suministro.

 Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico completo de suministro incluye un enlace con la página *Detalles del dispositivo*, después de iniciar una sesión en {{site.data.keyword.cloud_notm}}. También puede iniciar la sesión directamente en el {{site.data.keyword.slportal}}.

### Suministro de un servidor nativo a través del menú Dispositivos
{: #ordering-baremetal-devices-menu}

También puede suministrar el dispositivo de {{site.data.keyword.baremetal_short}} a través del menú *Dispositivos* en la página principal del {{site.data.keyword.slportal}}. 

1. Pulse **Dispositivos > Lista de dispositivos**. La página Dispositivos muestra todos los tipos de dispositivos (host dedicados, servidores virtuales, servidores nativos y controladores de distribución de aplicaciones NetScaler) de su cuenta.
2. Pulse el enlace **Pedir dispositivos** en la esquina superior derecha.
3. En la página Pedir servicios y productos de SoftLayer, pulse **Por hora** o **Mensualmente** en {{site.data.keyword.baremetal_short}}.
4. Seleccione el **Centro de datos**, desplácese a través de la página y pulse el enlace **Precio desde** para seleccionar el servidor. 
5.  Rellene la información de la página **Configure el dispositivo de {{site.data.keyword.baremetal_short}}** y pulse el botón **Añadir a pedido**. Consulte [Configuración del dispositivo de {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) para obtener más información sobre cómo configurar el servidor. Una vez verificado el pedido, se le redirigirá a la página de **pago**.
6.  Especifique la **Configuración avanzada del sistema** para el servidor. Consulte [Configuración del dispositivo de {{site.data.keyword.baremetal_short}}](.../bare-metal/configuring.md) para obtener más información sobre cómo hacerlo.
7. Pulse los recuadros de selección **Términos de servicio de la nube** y **Acuerdo de servicio de terceros**.
8. Confirme o especifique la información sobre el pago y pulse el botón **Enviar pedido**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla, ya que también es su recibo del pedido de suministro.

Se enviará una serie de correos electrónicos al administrador: acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado. El correo electrónico completo de suministro incluye un enlace con la página *Detalles del dispositivo*, después de iniciar una sesión en {{site.data.keyword.cloud_notm}}. También puede iniciar la sesión directamente en el {{site.data.keyword.slportal}}.

### Pasos siguientes
Una vez suministrado el dispositivo de {{site.data.keyword.baremetal_short}}, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión de {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
