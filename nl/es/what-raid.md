---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords: raid, about raid

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# Acerca de RAID
{: #bm-raid-levels}

RAID (matriz redundante de discos independientes) crea un único disco de datos que se pueden utilizar, en el que se combinan varios discos físicos en una matriz para mejorar la velocidad y la tolerancia al error. Los siguientes son los tres conceptos clave en RAID:
* **Duplicación**: copiar datos en más de un disco
* **Escritura en bandas**: dividir datos entre varios discos
* **Corrección de errores** (tolerancia a errores): se almacenan los datos redundantes para poder detectar y, posiblemente, solucionar, problemas.

Aunque existen muchos niveles diferentes de RAID, {{site.data.keyword.IBM_notm}} opta por admitir los tipos más comunes de RAID: 0, 1, 5, 6 y 10. Los distintos niveles de RAID utilizan una o varias de las técnicas siguientes, en función de los requisitos del sistema. El objetivo principal de utilizar RAID es mejorar la fiabilidad mediante 3Ware 9550SX Raid SATA o un controlador RAID Adaptec SA-SCSI en todas las soluciones RAID desplegadas.

RAID no es una solución de copia de seguridad. Más bien, RAID crea un único disco de datos que se puede utilizar, en el que se combinan varios discos físicos en una matriz para mejorar la velocidad y la tolerancia a errores.
{: note}

**RAID 0** (conjunto dividido sin paridad / matriz no redundante) implementa fragmentación de datos, donde los bloques de archivos se escriben en varios discos en fragmentos, y se requiere un mínimo de dos discos. La ventaja de un RAID 0 es que la velocidad de lectura/escritura aumenta notablemente. Cuantos más discos haya en la matriz, mayor es el ancho de banda. La desventaja de un RAID 0 es que no tiene tolerancia a errores. Si falla una sola unidad, la matriz se rompe. Además, RAID 0 no aplica la comprobación de errores. Por lo tanto, cualquier error es también irrecuperable. Una solución habitual para la tolerancia al error es tener una unidad fuera de la matriz para utilizarla como almacenamiento de copias de seguridad en caso de error de hardware.

**RAID 1** (conjunto duplicado sin paridad) implementa la duplicación de datos. Los datos se duplican en 2 o 4 discos a través de un controlador raid de hardware y se proporciona algo de tolerancia a errores. La matriz es recuperable si al menos una unidad no falla. Ofrece un mayor rendimiento de lectura que una sola unidad y proporciona redundancia de unidad si se produce un fallo de unidad. La velocidad de escritura se reduce ligeramente.

**RAID 5** (conjunto dividido con paridad dual distribuida) implementa la fragmentación de datos a nivel de bloque y distribuye la paridad entre los discos. La información de paridad permite la recuperación del fallo de cualquier unidad porque las lecturas siguientes se pueden calcular a partir de la paridad distribuida. RAID 5 también permite una mayor velocidad de lectura/escritura y un uso más eficiente del espacio de disco. RAID 5 requiere un mínimo de tres discos.

**RAID 6** (paridad doble) Implementa bandas de doble paridad en cada disco y permite el fallo de hasta dos discos antes de perder ningún dato. Debido a que RAID 6 tiene una capacidad de dos unidades de disco que están dedicadas a almacenar datos de paridad en un conjunto de paridad, se producen más operaciones de E/S con RAID 6 que con RAID 5. Este mayor número de operaciones de E/S pueden reducir el rendimiento. RAID 6 requiere un mínimo de 4 discos y un máximo de 18 discos.

**RAID 10** (RAID 1 + 0) crea varias duplicaciones, en las que los datos se organizan en bandas en varios discos y luego se duplican los conjuntos de discos divididos. RAID 10 ofrece la misma tolerancia al error que RAID 1 con una mayor velocidad de lectura/escritura en un solo volumen Raid 1 o en una sola unidad. Para implementar el nivel 10 de RAID se requieren cuatro discos.
