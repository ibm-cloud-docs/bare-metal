---

copyright:
  years: 2016, 2019
lastupdated: "2019-06-19"

keywords: bare metal, bare metal servers, POWER8, SAP-certified, {{site.data.keyword.baremetal_long}}, {{site.data.keyword.baremetal_short}}, available bare metal, cascade lake

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:note: .note}

# Acerca de los servidores nativos
{: #about-bm}

{{site.data.keyword.baremetal_long}} son la piedra angular de la solución de infraestructura como servicio. Ya sea usted un desarrollador de juegos que requiere E/S de alta velocidad o que necesite servidores de alto rendimiento para sus usuarios, {{site.data.keyword.baremetal_short}} puede responder a sus necesidades de cálculo.
{:shortdesc}

{{site.data.keyword.baremetal_short}} es un servidor de un solo arrendatario por hora o mensual que está dedicado a usted; no se comparte en ninguna parte, incluidos los recursos del servidor, con otros clientes. Puede gestionar el servidor, que se suministra sin un hipervisor, y está desplegado en uno o varios centros de datos. Se pueden comunicar varios {{site.data.keyword.baremetal_short}} en la red privada virtual de {{site.data.keyword.cloud_notm}} como si estuvieran en el mismo bastidor.

## Servidores para cada carga de trabajo
{: #servers-every-need}

{{site.data.keyword.cloud_notm}} tiene {{site.data.keyword.baremetal_short}} para que se adapte a cada carga de trabajo. Para obtener más información, consulte [Servidores nativos](https://www.ibm.com/cloud/bare-metal-servers){: external}

### Servidores de suministro rápido
{: #Popular-bm}

{{site.data.keyword.cloud_notm}} ofrece servidores preconfigurados que satisfacen las necesidades de la mayoría de los casos de uso. Estos servidores se consideran "de suministro rápido" porque sus opciones de cálculo (número de núcleos, velocidad, RAM y número de unidades) están preestablecidos. Los servidores preestablecidos están listos para configurar de 30 a 40 minutos después del suministro. 

### Servidores basados en la personalización
{: #custom-based-bm}

Si uno de los servidores de suministro rápido no satisface sus necesidades de carga de trabajo, puede personalizar el {{site.data.keyword.baremetal_short}} para que se adapte a sus necesidades. Los servidores personalizados se suministran entre 2 y 4 horas y ofrecen una mayor variedad de núcleos, velocidades, RAM y unidades. 

### Servidores basados en POWER8 personalizados
{: #bm-power8}

{{site.data.keyword.cloud_notm}} le ofrece la opción de suministrar un servidor nativo basado en POWER8 de IBM. Los servidores POWER8 están creados con el procesador POWER8 y una plataforma basada en OpenPower, que se adapta específicamente a los despliegues basados en la nube para cargas de trabajo de datos, cognitivas y web en Linux. Para obtener más información, consulte [Servidores POWER8](https://www.ibm.com/cloud/bare-metal-servers/power){: external}.

### Servidores dedicados con certificado SAP
{: #bm-SAP-cert}

{{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} están certificados para dar soporte a las cargas de trabajo de SAP HANA y SAP NetWeaver. Para obtener más información, consulte [Infraestructura certificada para SAP](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}.

## Opciones disponibles para servidores nativos <!--test new section - test as each option goes GA-->
{: #options-for-bare-metal-servers}
{{site.data.keyword.cloud_notm}} tiene opciones de {{site.data.keyword.baremetal_short}} que puede personalizar para ajustar a sus necesidades.

### Soporte de CPU Intel Cascade Lake
<!--Need to add which servers are also available for SAP once the certification is done-->
Ahora puede elegir entre las siguientes CPU Intel Cascade Lake al suministrar un servidor nativo:

* Intel Xeon 4210 (10-Core, 2.2 GHz, 85 W)
* Intel Xeon 5218 (16-Core, 2.3 GHz, 125 W)
* Intel Xeon 6248 (20-Core, 2.6 GHz, 150 W)
<!--Intel Xeon 8280M (28-Core, 2.7 GHz, 205 W)--><br>

<br>Los procesadores Cascade Lake actualmente están disponibles en los siguientes centros de datos:

<table style="width:100%">
<CAPTION>Tabla 1. Centros de datos con procesadores Cascade Lake</CAPTION>
 <tr>
   
   <th colspan="6">Centros de datos</th>
 </tr>
 <tr>
   <td>DAL10</td>
   <td>FRA02</td>
   <td>LON04</td>
   <td>SYD01</td>
   <td>TOK02</td>
   <td>WDC04</td>
   
</tr>

<tr>
  <td>DAL12</td>
  <td>FRA04</td>
  <td>LON05</td>
  <td>SYD04</td>
  <td>TOK04</td>
  <td>WDC06</td>
  
</tr>

<tr>
  <td>DAL13</td>
  <td>FRA05</td>
  <td>LON06</td>
  <td>SYD05</td>
  <td>TOK05</td>
  <td>WDC07</td>
</tr>
</table>


### Inventario dinámico
{: #bm-dynamic-inv}

Ahora puede ver qué servidores hay disponibles en qué centro de datos al suministrar un servidor nativo. Pero esta opción sólo está disponible para la oferta por horas. No puede ver la disponibilidad del servidor con la oferta mensual. Para obtener más información sobre cómo suministrar un servidor nativo, consulte [Elegir servidores de suministro rápido](/bare-metal?topic=bare-metal-bm-select-popular-servers).

### Complemento de almacenamiento en bloques y en archivos
{: #bm-block-and-file-add-on}

Si necesita almacenamiento adicional, {{site.data.keyword.IBM_notm}} se lo pone fácil. Ahora puede solicitar almacenamiento en bloques y en archivos (20 - 12.000 GB) al suministrar un servidor nativo. 

El almacenamiento complementario no se conecta automáticamente al servidor nativo. Tiene que conectar el almacenamiento complementario al servidor nativo después realizar los suministros.
{: note} 

<!--The add-on storage shares the data center that your bare metal server is on.-->

Para obtener más información sobre el almacenamiento en bloques y en archivos, consulte los enlaces siguientes.
* [Acerca del almacenamiento en bloques](/docs/infrastructure/BlockStorage?topic=BlockStorage-About)
* [Acerca del almacenamiento en archivos](/docs/infrastructure/FileStorage?topic=FileStorage-about)
