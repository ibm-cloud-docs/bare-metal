---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Preguntas frecuentes: servidores nativos

## ¿Por qué mi BIOS solicita una contraseña?

Actualmente, {{site.data.keyword.cloud}} no le proporciona acceso directo a su BIOS. Esto se debe a varias razones, pero no significa que no pueda realizar cambios en el BIOS. Si necesita modificar algún valor en el BIOS, incluido el orden de arranque, cree una incidencia en Soporte > Añadir incidencia a través del [Portal del cliente](control.softlayer.com) y solicite los cambios específicos que necesite.

\*\*NOTA\*\* Será necesario un reinicio del servidor para hacerlo, debe estar listo para aprobar un reinicio o indicar el marco de tiempo en el que desea que se realice el cambio.

## ¿Proporcionan recargas de sistema operativo gratuitas?

Las recargas automáticas de SO son gratuitas y se pueden realizar desde el [Portal del cliente](control.softlayer.com). Se incluyen las recargas personalizadas de SO (cambio de sistemas operativos, adición/eliminación de paneles de control/edición de particiones, etcétera). Para ver más información sobre cómo realizar una recarga de SO, consulte el [Procedimiento de recarga de SO](../vsi/vsi_perform_os_reload.html).


## La unidad primaria en mi servidor nativo aparece como /dev/sdb. ¿Qué ocurre?

Puede deberse a que el disco virtual de IPMI ocupe la ranura /dev/sda. Se puede inhabilitar de forma segura conectándose a IPMIView y navegando al separador de soporte virtual. Seleccione **Opciones > Inhabilitar** y pulse el botón **Aplicar** para realizar el cambio. La próxima vez que se reinicie el dispositivo de {{site.data.keyword.baremetal_short}}, la unidad primaria se mostrará como /dev/sda.


## ¿Por qué no es correcta la velocidad de la CPU?

Si inicia la sesión en un servidor para comprobar la información de la CPU y observa que la velocidad de los procesadores no es correcta, esta discrepancia se puede deber a la tecnología Intel SpeedStep mejorada (EIST). EIST es el nombre de la tecnología de escalado de frecuencia dinámica de Intel.  Esta tecnología también se denomina *CPU throttling* o *bus slewing* en sistemas más antiguos. En algunos sistemas AMD, hay tecnologías similares denominadas *Cool'N'Quiet* o *PowerNow!*.  Aunque estas tecnologías no son iguales, tienen el mismo objetivo, que es reducir el consumo de energía y la producción de calor cuando no hay un uso exhaustivo del procesador reduciendo la velocidad de la CPU.  Cuando el servidor vuelve a estar cargado, se aumenta la velocidad de reloj según sea necesario.

Si desea saber si el procesador Intel del servidor es compatible con SpeedStep, en el portal del cliente: 
1. Pulse **Dispositivos**.
* Identifique el servidor en la lista.
* Pulse el nombre del servidor para ver los **Detalles del dispositivo**.
* Localice la subsección titulada **Hardware** para encontrar el número de la velocidad de CPU de los procesadores del servidor.
* Con el número de modelo de procesador del servidor, vaya a [Intel Processor Finder](http://processorfinder.intel.com/) y utilice ese número para buscar más información sobre el procesador y saber si es compatible con la tecnología Intel SpeedStep mejorada.

EIST es una tecnología establecida. No debería tener ningún motivo para desactivar EIST. Sin embargo, si decide que no desea utilizar esta característica, abra una incidencia con el equipo de soporte para inhabilitarla.  Para inhabilitar esta característica, se reiniciará el servidor.


## ¿Qué pasa si el firmware de mi servidor nativo está obsoleto?

Al igual que con las actualizaciones de software, es importante mantener actualizado el firmware para garantizar la estabilidad y la compatibilidad óptimas del dispositivo. Si el firmware de un dispositivo de {{site.data.keyword.baremetal_short}} está obsoleto, puede que se inicie una actualización de firmware durante el proceso de [Recarga de SO](../infrastructure/software/vsi_reload_os.html) en el [Portal del cliente](https://control.softlayer.com).

También puede actualizar el firmware seleccionando el servidor nativo en la lista de dispositivos y pulsando **Actualizar firmware** en el menú de acciones desplegable.
