---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-16"

keywords: bare metal, faq, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Preguntas frecuentes: servidores nativos
{: #bm-faq}

## ¿Qué es la modalidad de arranque UEFI?
{: faq}
UEFI (Unified Extensible Firmware Interface) es una especificación de la interfaz de software entre un sistema operativo y un firmware.

El soporte de IBM Cloud para modalidad de arranque BIOS está quedando desfasada en favor de la modalidad de arranque UEFI.

Para obtener más información sobre UEFI, consulte la documentación del fabricante de hardware o vaya a [https://uefi.org/](https://uefi.org/)

## ¿Por qué mi BIOS solicita una contraseña?
{: faq}

Actualmente, {{site.data.keyword.cloud}} no le proporciona acceso directo a su BIOS, por varios motivos. Sin embargo, puede cambiar el BIOS. Si necesita modificar algún valor en el BIOS, incluido el orden de arranque, cree una incidencia en Soporte > Añadir incidencia a través del [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/){: new_window} y solicite los cambios específicos que necesite.

\*\*NOTA\*\* Es necesario un reinicio del servidor para hacerlo, debe estar listo para aprobar un reinicio o indicar el marco de tiempo en el que desea que se realice el cambio.

## ¿Proporcionan recargas de sistema operativo gratuitas?
{: faq}

Las recargas automáticas de SO son gratuitas y se pueden realizar desde el [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/){: new_window}. Se incluyen las recargas personalizadas de SO (cambio de sistemas operativos, adición/eliminación de paneles de control/edición de particiones, etcétera).  Para obtener más información sobre cómo realizar una recarga de SO, consulte el [Procedimiento de recarga de SO](/docs/infrastructure/software?topic=software-reloading-the-os).


## La unidad primaria en mi servidor nativo aparece como /dev/sdb. ¿Qué ocurre?
{: faq}

Puede deberse a que el disco virtual de IPMI ocupe la ranura /dev/sda. Se puede inhabilitar de forma segura conectándose a IPMIView y navegando al separador de soporte virtual. Seleccione **Opciones > Inhabilitar** y pulse el botón **Aplicar** para realizar el cambio. La próxima vez que se reinicie el dispositivo de {{site.data.keyword.baremetal_short}}, la unidad primaria se mostrará como /dev/sda.


## ¿Por qué no es correcta la velocidad de la CPU?
{: faq}

Si inicia la sesión en un servidor para comprobar la información de la CPU y observa que la velocidad de los procesadores no es correcta, esta discrepancia se puede deber a la tecnología Intel SpeedStep mejorada (EIST). EIST es el nombre de la tecnología de escalado de frecuencia dinámica de Intel.  Esta tecnología también se denomina *CPU throttling* o *bus slewing* en sistemas más antiguos.  Algunos sistemas AMD tienen tecnologías similares denominadas *Cool'N'Quiet* o *PowerNow!*.  Aunque estas tecnologías no son iguales, tienen el mismo objetivo, que es reducir el consumo de energía y la producción de calor cuando no hay un uso exhaustivo del procesador reduciendo la velocidad de la CPU.  Cuando el servidor vuelve a estar cargado, se aumenta la velocidad de reloj según sea necesario.

Si desea saber si el procesador Intel del servidor es compatible con SpeedStep, utilice el siguiente procedimiento en el portal de clientes:
1. Pulse **Dispositivos**.
* Identifique el servidor en la lista.
* Pulse el nombre del servidor para ver los **Detalles del dispositivo**.
* Localice la subsección titulada **Hardware** para encontrar el número de la velocidad de CPU de los procesadores del servidor.
* Con el número de modelo de procesador del servidor, vaya a [Intel Processor Finder ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://processorfinder.intel.com/){: new_window} y utilice ese número para buscar más información sobre el procesador y saber si es compatible con la tecnología Intel SpeedStep mejorada.

EIST es una tecnología establecida. No es común que deba desactivar EIST. Sin embargo, si decide que no desea utilizar esta característica, abra una incidencia con el equipo de soporte para inhabilitarla.  Para inhabilitar esta característica, se reinicia el servidor.


## ¿Qué pasa si el firmware de mi servidor nativo está obsoleto?
{: faq}

Es importante mantener actualizado el firmware para garantizar la estabilidad y la compatibilidad óptimas del dispositivo. Si una versión de firmware de {{site.data.keyword.baremetal_short}} está desactualizada, se puede actualizar el firmware seleccionando el servidor nativo en la lista de dispositivos y seleccionando **Actualizar firmware** en el menú Acción.

Puede iniciar una actualización de firmware durante el proceso de [Recarga de sistema operativo](/docs/infrastructure/software?topic=software-reloading-the-os) dentro de [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/){: new_window}.

## ¿Qué sucede con las unidades en servidores nativos cuando un cliente ha terminado con ellos?
{: faq}

Tras la cancelación, un servidor se traslada automáticamente a una VLAN de reclamación para un tiempo de retención establecido. Una vez finalizados, los procesos de reclamación se inician y la unidad se limpia utilizando algoritmos de DOD 5220.22-M.  Se realiza un seguimiento de la reclamación utilizando el número de serie en la unidad. Una vez completado, el servidor se traslada al suministro para la reasignación. Un funcionamiento incorrecto de la unidad solicita la intervención manual y las unidades se establecerán en el final del ciclo de vida.

El final del proceso de vida se inicia cuando hay una función incorrecta o si la antigüedad o el tamaño están más allá del soporte. Una vez que se produzca cualquiera de estas condiciones, las unidades se limpiarán como se describió anteriormente. Una vez finalizado el proceso de limpieza, la unidad se destruye físicamente rompiendo, triturando o destruyendo el dispositivo.  Se realiza un seguimiento del proceso de destrucción física utilizando el número de serie en la unidad.

## ¿Puedo ver qué servidores nativos están disponibles para comprar?
{: faq}

Sí. Ahora puede ver qué servidores hay disponibles en qué centro de datos al suministrar un servidor nativo. Pero esta opción sólo está disponible para la oferta por horas. No puede ver la disponibilidad del servidor con la oferta mensual. Para obtener más información sobre cómo suministrar un servidor nativo, consulte [Elegir servidores de suministro rápido](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers#bm-select-popular-servers).

## ¿Qué se incluye con mi servidor nativo reservado?
{: faq}

En la reserva para el período de tiempo contratado se incluye CPU, RAM, unidad de disco y RAID. Si necesita un mayor ancho de banda de red, una mayor capacidad de almacenamiento, un sistema operativo o software de terceros, estos complementos se cobran mensualmente.

## ¿Qué ocurre al final de mi contrato de servidor nativo?
{: faq}

Cuando caduca el contrato, el servicio en la nube continúa como servicio mensual con la tarifa en vigor.
