---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-02"

keywords: provision bare metal, popular servers, {{site.data.keyword.baremetal_short}}, provision

subcollection: bare-metal


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Selección entre los servidores más populares
{: #bm-select-popular-servers}

Los servidores de la lista de Servidores más populares están preconfigurados para satisfacer las necesidades de la mayoría de los casos de uso del cliente, y están listos para ejecutarse en 30 - 40 minutos después de ordenarlos.
1. Abra el [catálogo de {{site.data.keyword.cloud_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/catalog/){: new_window}.   
2. Seleccione el servidor nativo.
3. Pulse Continuar.  Si no ve un botón Continuar, es posible que tenga que iniciar sesión.
2. En la sección {{site.data.keyword.baremetal_short}}, seleccione la información siguiente:
    <table>
    <CAPTION>Tabla 1. Selecciones de servidores nativos</CAPTION>
    <THEAD>
    <TR>
    <th>Campo</th>
    <th>Valor</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Cantidad</td>
    <td>Utilice los iconos + y - para especificar el número de servidores **idénticos** a suministrar. El valor predeterminado es 1.<br>Si desea suministrar varios servidores con especificaciones **diferentes**, deberá suministrarlos por separado.
    <tr>
    <tr>
    <td>Tipo de facturación</td>
    <td>Seleccione Por horas o Mensual
    <tr>
    <td>Nombre de host y dominio</td>
    <td>Estos campos se rellenan de forma predeterminada. Puede cambiarlos.</td>
    </tr>
    <tr>
    <td>Ubicación</td>
    <td>Seleccione la región donde desea que se ubique el servidor. Utilizando la lista desplegable, seleccione el centro de datos de la región. </td>
    </tr>
    <tr>
    <tr>
    <td>Seleccione su servidor</td>
    <td>Seleccione **Servidores populares** y seleccione el servidor que se ajuste a sus necesidades. Estos servidores están preconfigurados y están listos para su uso en 30 - 40 minutos.
    </tr>
    <tr>
    <td>RAM</td>
    <td>Valor predeterminado basado en el servidor que ha seleccionado.</td>
    </tr>
    <tr>
    <td>Claves SSH</td>
    <td>Proporcione una clave pública de la clave SSH, que utilizará para iniciar sesión en el servidor después de que se suministre.</td>
    </tr>
    <tr>
    <td>Imagen <br>(Sistema operativo)</td>
    <td>Seleccione el sistema operativo para el servidor. Las opciones de imagen pueden ser limitadas en función del servidor que haya seleccionado.</td>
    </tr>
    <td>Complementos</td>
    <td>Expanda la sección Complementos para seleccionar las opciones adecuadas o utilice los valores predeterminados./td>
    </tr>
    </TBODY>
    </table>
3. En la sección Discos de almacenamiento, el Disco de almacenamiento ya está seleccionado con la selección Servidores populares. Expanda la sección Complementos si desea añadir IBM Cloud Backup a su servidor.
4. En la sección Interfaz de red, seleccione Velocidades de puerto de enlace ascendente. Expanda la sección Complementos para seleccionar las opciones adecuadas o utilice los valores predeterminados.
4.  Revise el pedido.
4. Si tiene un código promocional para aplicar a su pedido, expanda Aplicar código promocional.  
5.  Revise los acuerdos de servicio de terceros que aparecen en la lista y pulse el recuadro de selección **Acuerdo de servicio de terceros**.
6.  Pulse **Suministro**. Se le redirigirá a una pantalla con el número de su pedido de suministro. Puede imprimir la pantalla, ya que también es su recibo del pedido de suministro.

 Se enviará una serie de correos electrónicos al administrador: Acuse de recibo del pedido de suministro, aprobación y proceso del pedido de suministro y suministro completado.

 El _correo electrónico de suministro completado_ incluye un enlace a la página *Detalles del dispositivo* para que pueda iniciar sesión en {{site.data.keyword.cloud_notm}}. También puede iniciar la sesión directamente en el {{site.data.keyword.slportal}}.


## Pasos siguientes

Una vez suministrado el dispositivo de {{site.data.keyword.baremetal_short}}, puede empezar a gestionarlo. Para obtener más información, consulte [Gestión de {{site.data.keyword.baremetal_short}}](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
