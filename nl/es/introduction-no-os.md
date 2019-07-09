---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: bare metal, no os, no operating system

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# La opción sin SO
{: #bm-no-os}

**Sin sistema operativo** es una opción para solicitar {{site.data.keyword.baremetal_long}} sin sistema operativo.

## Pedido de {{site.data.keyword.baremetal_short}} sin sistema operativo
{: #ordering-no-os}

1. Utilice los pasos que se describen en [Creación de un servidor nativo personalizado](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server) para solicitar el servidor.
2. Seleccione **Sin sistema operativo** en **Imagen**.
3. Complete el pedido del servidor. 

## Cómo cambiar a Sin sistema operativo
{: #changing-to-no-os}

UN servidor se puede reconfigurar para que no tenga operativo. La reconfiguración se realiza a través de una recarga del sistema operativo. Para obtener información, consulte [Recarga del SO](/docs/infrastructure/software?topic=software-reloading-the-os).

1. Pulse **Dispositivos** > **Lista de dispositivos**.
2. Seleccione el servidor que desea reconfigurar sin sistema operativo.
3. Pulse **Recarga de SO** y especifique la información aplicable.

## Instalación de un sistema operativo en un servidor sin sistema operativo
{: #installing-os-on-no-os-server}

Hay dos métodos para instalar sistemas operativos en {{site.data.keyword.baremetal_short}} sin sistema operativo.

### Opción 1: servidor PXE (Entorno de ejecución de prearranque)
{: #option-1}

{{site.data.keyword.baremetal_short}} sin sistemas operativos se puede configurar para arrancar y cargar un SO desde una configuración de PXE.<!--(see [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) for more information)--> Despliegue {{site.data.keyword.baremetal_short}} en un entorno de red con una configuración de PXE (normalmente, esto implica ejecutar un daemon DHCP y TFTP) y configure el BIOS de los nuevos servidores para que se arranque desde el adaptador de red. Para que la opción sin sistema operativo funcione correctamente, la configuración de PXE debe estar en la misma VLAN que el {{site.data.keyword.baremetal_short}}, o bien es necesario utilizar reenvío de DHCP.

Para que esta opción funcione, puede que sea necesario abrir una incidencia de soporte para solicitar que los puertos de conmutador se reagrupen en modalidad básica. Esto se debe a que el protocolo PXE no requiere compatibilidad con agregación de enlaces (LACP), <!--see [Link Aggregation](http://en.wikipedia.org/wiki/Link_aggregation))--> que ahora es una función estándar para proporcionar redundancia. Otra opción es solicitar el servidor con enlaces ascendentes desvinculados (sin agregación de enlaces) y luego, una vez instalado el SO, cambiarlos a enlaces ascendentes redundantes.
{: note}

### Opción 2: dispositivo IPMI
{: #option-2}

Puede instalar sistemas operativos en {{site.data.keyword.baremetal_short}} sin sistema operativo arrancando desde una ISO a través del dispositivo IPMI incluido. Para obtener más información sobre cómo arrancar desde una ISO, consulte [Montaje de una ISO en un servidor nativo](/docs/bare-metal?topic=bare-metal-mounting-an-iso-on-a-bare-metal-server).
