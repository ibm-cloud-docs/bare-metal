---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# ¿Por qué no es correcta la velocidad de la CPU?

Si inicia la sesión en un servidor para comprobar la información de la CPU y observa que la velocidad de los procesadores no es correcta, esta discrepancia se puede deber a la tecnología Intel SpeedStep mejorada (EIST). EIST es el nombre de la tecnología de escalado de frecuencia dinámica de Intel.  Esta tecnología también se denomina *CPU throttling* o *bus slewing* en sistemas más antiguos.  En algunos sistemas AMD, hay tecnologías similares denominadas *Cool'N'Quiet* o *PowerNow!*.  Aunque estas tecnologías no son iguales, tienen el mismo objetivo, que es reducir el consumo de energía y la producción de calor cuando no hay un uso exhaustivo del procesador reduciendo la velocidad de la CPU.  Cuando el servidor vuelve a estar cargado, se aumenta la velocidad de reloj según sea necesario.

Si desea saber si el procesador Intel del servidor es compatible con SpeedStep, en el portal de clientes: 
1. Pulse **Dispositivos**.
* Identifique el servidor en la lista.
* Pulse el nombre del servidor para ver los **Detalles del dispositivo**.
* Localice la subsección titulada **Hardware** para encontrar el número de la velocidad de CPU de los procesadores del servidor.
* Con el número de modelo de procesador del servidor, vaya a [Intel Processor Finder](http://processorfinder.intel.com/) y utilice ese número para buscar más información sobre el procesador y saber si es compatible con la tecnología Intel SpeedStep mejorada.

EIST es una tecnología establecida. No debería tener ningún motivo para desactivar EIST. Sin embargo, si decide que no desea utilizar esta característica, abra una incidencia con el equipo de soporte para inhabilitarla.  Para inhabilitar esta característica, se reiniciará el servidor.
