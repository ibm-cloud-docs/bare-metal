---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Creación y ajuste de las configuraciones de RAID de Adaptec

El Bios de RAID de Adaptec permite configurar y gestionar la instalación de RAID. Utilice este BIOS si selecciona la opción [Sin sistema operativo](introduction-no-os.html) y desea establecer una configuración de unidad específica.

## Acceso al dispositivo IPMI para interactuar con el Bios de RAID

Independientemente de si la máquina tiene un controlador Adaptec o un controlador LSI, deberá acceder al servidor utilizando IPMI para interactuar con el Bios de RAID. Para interactuar con IPMI, primero debe conectarse a la VPN de {{site.data.keyword.IBM&reg; Cloud}} de Adaptec.
1. Inicie sesión en la VPN mediante [SSL](/infrastructure/vpn/ssl-vpn-connections.html) o PPTP. Consulte la [página sobre el tema VPN](/infrastructure/vpn/index.html).
* Acceda a la lista de dispositivos en el [Portal del cliente](https://control.softlayer.com/). Consulte [Acceder a la lista de dispositivos](/vsi/vsi_managing.html).
* Pulse el dispositivo al que desea acceder.
* Seleccione el separador Gestión remota para buscar los detalles de acceso de IPMI de los servidores.
* Coloque la IP del dispositivo IPMI en el navegador e inicie sesión.
* Para empezar a interactuar con la consola remota, pulse Remote Control > Console Redirection.

## Creación de matrices RAID

Durante el proceso de arranque, pulse Ctrl+A para acceder al BIOS de Raid.

Para empezar a configurar el RAID, vaya a Logical Device Configuration (primera opción). Se explorará la topología de las unidades y se mostrará un menú en el que puede gestionar matrices, crear matrices y realizar otras tareas de administración de unidad.

El ejemplo siguiente muestra cómo crear una matriz. Se muestra una lista de unidades disponibles para utilizarlas al crear la matriz RAID.

1. Para seleccionar las unidades, pulse la barra ESPACIADORA para rellenar el recuadro de *Selected Drives*.
* Una vez que haya seleccionado todas las unidades que desea utilizar en la matriz, pulse INTRO para ir al paso de configuración de RAID.
* Elija el tipo de RAID que desea. Si necesita ayuda para determinar qué RAID es más adecuado para sus necesidades, consulte las siguientes [preguntas frecuentes de Adaptec](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm).
* Proporcione una etiqueta de matriz durante la configuración. Es una buena práctica incluir el tipo de RAID en la etiqueta (por ejemplo: RAID10-A).
* Pulse Intro para navegar a los demás valores. Utilice los valores predeterminados.

Una vez completada la configuración, seleccione Done y se creará la matriz RAID. Puede ver la nueva matriz seleccionando 'Manage Arrays' en el menú principal. Para salir del programa de configuración, pulse la tecla ESC hasta que aparezca un mensaje para salir del BIOS de Adaptec.

## Eliminación de matrices existentes

Si necesita eliminar una matriz existente, vaya a Manage Arrays, seleccione la matriz que desee eliminar, pulse Delete y confirme.

## Configuraciones de ejemplo

1. En un servidor con un total de 6 unidades, puede configurar 2 SSD en un RAID0 para el sistema operativo y 4 unidades adicionales en un RAID10 para los datos reales. De esta forma, puede recargar rápidamente el sistema operativo de los servidores sin restaurar el sitio ni los datos de servicio si se encuentran en la matriz secundaria.

* En un servidor de cPanel, puede tener /var y /home en distintas matrices RAID SSD. Dado que estos son los 2 directorios de más E/S de un servidor de cPanel, puede reducir el tiempo de respuesta del sitio con los valores siguientes:
  * RAID0 (2 unidades SATA) - /
  * RAID0 (2 unidades SSD) - /var
  * RAID0 (2 unidades SSD) - /home
  * RAID10 (4 unidades SATA) - /backup

* Utilice una matriz RAID única para configurar varias particiones lógicas. Por ejemplo, utilice dos unidades de 4 TB configuradas en un RAID1. Puede particionar la RAID para que se ajuste a sus necesidades. Por ejemplo:
  * Partición primaria de 100 GB para el sistema operativo
  * Segunda partición de 500 GB para los datos
  * Tercera partición del espacio restante para las copias de seguridad
