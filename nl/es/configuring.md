---



copyright:
  years: 2017
lastupdated: "2017-12-05"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuración del servidor nativo

Es una buena idea dedicar el tiempo necesario a decidir la configuración antes de suministrar el dispositivo de {{site.data.keyword.baremetal_long}}. De esta forma, se agiliza y se facilita el proceso de suministro. {:shortdesc}

## Cómo determinar el uso del servidor y medir su tamaño

Su primera tarea consiste en determinar cómo va a utilizar el dispositivo de {{site.data.keyword.baremetal_short}}. Por ejemplo, ¿desea utilizarlo para desarrollo/prueba o producción? ¿Va a probar una experiencia de usuario, procesar algoritmos extensos, realizar copias de seguridad y restauraciones de datos o aumentar la velocidad de latencia?

Después de determinar cómo se va a utilizar el dispositivo de {{site.data.keyword.baremetal_short}}, debe medir su tamaño. La [calculadora de coste total de propiedad de SoftLayer](http://www.softlayer.com/tco/) puede ayudar a determinar qué dispositivo de {{site.data.keyword.baremetal_short}} se ajusta mejor a sus necesidades.

## Selección del servidor

{{site.data.keyword.cloud_notm}} ofrece siete servidores de suministro rápido para asegurarse de que el usuario obtenga el rendimiento que necesita para su carga de trabajo. Estos servidores están disponibles actualmente en el Reino Unido y las regiones del sur de Estados Unidos.

| **Configuración** | **Procesador** | **Memoria** | **Disco duro** | **Velocidad de puerto** |
|-------------------|---------------|------------|----------------|----------------|
| Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 núcleos, 3,50 GHz) |32 GB RAM |1 unidad de disco duro interno |Velocidad de puerto de 100 Mbps como máximo|
|Intel Xeon E5-2620 v3 |Dual Intel Xeon E5-2620 v3 (6 núcleos, 2,40 GHz) |64 GB RAM |2 unidades de disco duro interno |Velocidad de puerto de 100 Mbps como máximo|
|Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 núcleos, 3,50 GHz) |32 GB RAM |2 unidades de disco duro interno |Velocidad de puerto de 100 Mbps como máximo|
|Intel Xeon E5-2650 v3 |Dual Intel Xeon E5-2650 v3 (10 núcleos, 2,30 GHz) |128 GB RAM |1 unidad de disco duro interno |Velocidad de puerto de 100 Mbps como máximo|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 núcleos, 2,60 GHz) |128 GB RAM |2 unidades de disco duro interno |Velocidad de puerto de 100 Mbps como máximo|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 núcleos, 2,60 GHz) |64 GB RAM |4 unidades de disco duro interno |Velocidad de puerto de 1000 Mbps como máximo|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 núcleos, 2,60 GHz) |256 GB RAM |4 unidades de disco duro interno |Velocidad de puerto de 1000 Mbps como máximo|

Además de los siete servidores de suministro rápido, {{site.data.keyword.cloud_notm}} ha ampliado su oferta de {{site.data.keyword.baremetal_short}} para incluir sistemas nativos basados en POWER8. Estos sistemas están creados con el procesador POWER8 de {{site.data.keyword.IBM_notm}} y una plataforma basada en OpenPOWER, que está adaptada específicamente para despliegues de datos basados en la nube, cognitivos y cargas de trabajo web en Linux.

Todos los {{site.data.keyword.baremetal_short}} se pueden actualizar para incluir un ancho de banda sin límite de uso (ilimitado). Todos los dispositivos sin límite de uso están en puertos privados y dedicados.

## Configuración de los servidores nativos

Después de seleccionar el centro de datos, el servidor y la opción de facturación (mensual o por hora), debe decidir cómo configurar el servidor. Algunos campos (servidor, RAM, unidad de procesamiento de gráficos y unidad de procesamiento de gráficos secundaria) de la página **Configure el dispositivo de {{site.data.keyword.baremetal_short}}** tendrán un valor predeterminado en función de la selección de servidor. La tabla siguiente describe los campos en los que puede definir un valor.

| **Campo** | **Descripción** | 
|-------------------|---------------|
|Sistema operativo |Seleccione entre CentOS, FreeBSD, Microsoft, Red Hat, Unbuntu u Otro. |
|Unidades de disco duro |La herramienta de configuración de disco le permite configurar los discos duros rellenando los campos en función de la selección de sistema operativo. |
|Ancho de banda público |Determina la cantidad de datos que se pueden transferir a través de la interfaz pública durante un mes. Para entornos de prueba, que necesitan transferir datos de instalación a través de esta interfaz, los valores deben adaptarse más allá de la cantidad de datos transferidos inicialmente. Puede que desee considerar la [red de entrega de contenidos de {{site.data.keyword.cloud_notm}}](https://www.ibm.com/cloud/cdn) para enviar una carga de datos inicial a uno de los centros de datos de {{site.data.keyword.cloud_notm}}. |
|Velocidades de puerto de enlace ascendente |Determina la velocidad de las interfaces internas y externas. |
|Direcciones IP secundarias públicas |Asigna una dirección IP adicional al servidor. Según el caso, puede necesitar que se asignen más direcciones IP al servidor. Existen direcciones IPv4 adicionales disponibles en cantidades de 1, 2, 4, 8, 16 o 32. |
|Direcciones IPv6 primarias |Asignadas a las interfaces internas y externas del servidor. |
|Direcciones IPv6 estáticas públicas |Asigna direcciones IPv6 adicionales de un bloque /64. |
|Cortafuegos de software y hardware, Protección antivirus y anti spyware y Protección y detección de intrusos |Seleccione las opciones apropiadas si el servidor tendrá contacto con Internet. Se recomienda encarecidamente que su departamento de seguridad corporativa se ponga de acuerdo con el soporte de {{site.data.keyword.cloud_notm}} para comentar los detalles de estas opciones. |
|Evault |Una herramienta de copia de seguridad basada en agente que se puede instalar en el servidor para replicar copias de seguridad entre servidores. |

Consulte la herramienta [Design Decision Tool](http://knowledgelayer.softlayer.com/learning/softlayer-design-decision-tool) o el soporte de {{site.data.keyword.cloud_notm}} para obtener más información.


## Configuración avanzada del sistema

La configuración avanzada del sistema se realiza después de pulsar el botón **Añadir a pedido** y ser redirigido a la página de pago. La tabla siguiente describe los campos de configuración avanzada del sistema.

| **Campo** | **Descripción** | 
|-------------------|---------------|
|Nombre de host |Un nombre permanente o temporal para el servidor, por ejemplo, _server1_. |
|Dominio |Nombre del subdominio, que no debería estar en conflicto con un nombre de dominio de Internet, por ejemplo, _test.acme.com_. |
|Selección de VLAN |Si hay una VLAN bajo su cuenta porque ya ha solicitado al menos un servidor, puede añadir el nuevo servidor a la VLAN. |
|Script de suministro |Puede proporcionar un script que le permita automatizar algunos pasos una vez que el servidor se haya suministrado. |
|Claves SSH |Puede proporcionar una clave pública para la clave SSH, que le permitirá iniciar sesión en el servidor una vez que se haya suministrado. |
