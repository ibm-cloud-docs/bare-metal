---

copyright:
  years: 2017, 2019
lastupdated: "2018-07-10"

keywords: raid, adaptec, ipmi, raid bios, raid array, RAID configuration

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Creación y ajuste de las configuraciones de RAID de Adaptec
{: #bm-create-raid-config}

El BIOS de RAID de Adaptec permite configurar y gestionar la instalación de RAID. Utilice este BIOS si selecciona la opción [Sin sistema operativo](/docs/bare-metal?topic=bare-metal-the-no-os-option) y desea establecer una configuración de unidad específica.

## Acceso al dispositivo IPMI para interactuar con el BIOS de RAID
{: #bm-access-ipmi}

Independientemente de si la máquina tiene un controlador Adaptec o un controlador LSI, debe acceder al servidor que utiliza IPMI para interactuar con el BIOS de RAID. Para interactuar con IPMI, primero debe conectarse a la VPN de {{site.data.keyword.cloud}} de Adaptec.
1. Inicie sesión en la VPN mediante [SSL](/docs/infrastructure/iaas-vpn?topic=VPN-setup-ssl-vpn-connections#setup-ssl-vpn-connections) o PPTP.
* Acceda a la lista de dispositivos en [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/){: new_window}. Consulte [Acceder a la lista de dispositivos](/docs/infrastructure/vsi?topic=virtual-servers-managing-virtual-servers).
* Pulse el dispositivo al que desea acceder.
* Seleccione el separador Gestión remota para buscar los detalles de acceso de IPMI del servidor.
* Coloque la IP del dispositivo IPMI en el navegador e inicie sesión.
* Para empezar a interactuar con la consola remota, pulse **Remote Control > Console Redirection**.

## Creación de matrices RAID
{: #bm-create-raid-array}

Durante el proceso de inicio, pulse **Ctrl+A** para acceder al BIOS de RAID.

Para empezar a configurar el RAID, abra Logical Device Configuration (primera opción). Esta opción explora la topología de las unidades y se muestra un menú en el que puede gestionar matrices, crear matrices y realizar otras tareas de administración de unidad.

El ejemplo siguiente muestra cómo crear una matriz. Se muestra una lista de unidades disponibles para utilizarlas al crear la matriz RAID.

1. Para seleccionar las unidades, pulse la barra ESPACIADORA para rellenar el recuadro *Selected Drives*.
* Una vez que haya seleccionado todas las unidades que desea utilizar en la matriz, pulse INTRO para ir al paso de configuración de RAID.
* Elija el tipo de RAID que desea utilizar. Si necesita ayuda para determinar qué configuración de RAID es más adecuada para sus necesidades, consulte las siguientes [preguntas frecuentes de Adaptec ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm){: new_window}.
* Proporcione una etiqueta de matriz durante la configuración. Es una buena práctica incluir el tipo de RAID en la etiqueta (por ejemplo: RAID10-A).
* Pulse **Intro** para ir a los demás valores. Utilice los valores predeterminados.

Una vez completada la configuración, seleccione Done y se creará la matriz RAID. Puede ver la nueva matriz seleccionando 'Manage Arrays' en el menú principal. Para salir del programa de configuración, pulse la tecla ESC hasta que aparezca un mensaje para salir del BIOS de Adaptec.

## Eliminación de matrices RAID existentes
{: #bm-remove-raid-array}

Si necesita eliminar una matriz existente, vaya a **Manage Arrays**, seleccione la matriz que desee eliminar, pulse **Delete** y confirme.

## Configuraciones de ejemplo
{: #bm-example-config}

1. En un servidor con un total de seis unidades, puede configurar dos SSD en RAID 0 para el sistema operativo y cuatro unidades más en RAID 10 para los datos reales. Esta configuración se utiliza para recargar rápidamente el sistema operativo del servidor sin restaurar el sitio ni los datos de servicio si se encuentran en la matriz secundaria.

* En un servidor de cPanel, puede tener /var y /home en distintas matrices RAID SSD. Dado que los directorios son los dos directorios de más E/S de un servidor de cPanel, puede reducir el tiempo de respuesta del sitio con los valores siguientes:
  * RAID0 (2 unidades SATA) - /
  * RAID0 (2 unidades SSD) - /var
  * RAID0 (2 unidades SSD) - /home
  * RAID10 (4 unidades SATA) - /backup

* Utilice una matriz RAID única para configurar varias particiones lógicas. Por ejemplo, utilice dos unidades de 4 TB en una matriz RAID 1. Puede particionar la matriz RAID para satisfacer sus necesidades. Consulte el siguiente ejemplo:
  * Partición primaria de 100 GB para el sistema operativo
  * Segunda partición de 500 GB para los datos
  * Tercera partición del espacio restante para las copias de seguridad
