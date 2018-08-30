---
copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Acerca de RAID

RAID (matriz redundante de discos independientes) crea un único disco de datos que se pueden utilizar, en el que se combinan varios discos físicos en una matriz para mejorar la velocidad y la tolerancia al error. Los siguientes son los tres conceptos clave en RAID:
* Duplicación: copiar datos en más de un disco
* Escritura en bandas: dividir datos en más de un disco
* Corrección de errores (tolerancia al error): se almacenan los datos redundantes para poder detectar y, posiblemente, solucionar, problemas.

Aunque existen muchos niveles diferentes de RAID, IBM opta por admitir los tipos más comunes de raid: 0, 1, 5 y 10. Los distintos niveles de RAID utilizan una o varias de las técnicas siguientes, en función de los requisitos del sistema. El objetivo principal de utilizar RAID es mejorar la fiabilidad mediante 3Ware 9550SX Raid SATA o un controlador RAID Adaptec SA-SCSI en todas las soluciones RAID desplegadas.

RAID no es una solución de copia de seguridad.  RAID crea un único disco de datos que se pueden utilizar, en el que se combinan varios discos físicos en una matriz para mejorar la velocidad y la tolerancia al error.


**RAID 0** (conjunto dividido sin paridad/matriz no redundante) implementa una fragmentación de datos en la que se escriben los bloques de archivos en varias unidades en fragmentos, y se requiere un mínimo de dos discos. La ventaja de un RAID 0 es que la velocidad de lectura/escritura aumenta notablemente. Cuantos más discos hay en la matriz, mayor es el ancho de banda. La desventaja de un RAID 0 es que no proporciona tolerancia a errores. De ese modo, si falla una sola unidad, se destruye la matriz. Además, un RAID 0 no aplica la comprobación de errores, de forma que cualquier error también es irrecuperable. Una solución habitual para la tolerancia al error es tener una unidad fuera de la matriz para utilizarla como almacenamiento de copias de seguridad en caso de error de hardware.

**RAID 1** (conjunto duplicado sin paridad) implementa la duplicación de datos. Los datos se duplican en 2 o 4 unidades a través de un controlador raid de hardware y se proporciona algo de tolerancia al error. La matriz es recuperable si al menos una unidad no falla. Ofrece un mayor rendimiento de lectura que una sola unidad y proporciona redundancia de unidad si se produce un fallo de unidad. La velocidad de escritura también se reducirá ligeramente.

**RAID 5** (conjunto dividido con paridad dual distribuida) implementa la fragmentación de datos a nivel de bloque y distribuye la paridad entre las unidades. La información de paridad permite la recuperación del fallo de cualquier unidad porque las lecturas siguientes se pueden calcular a partir de la paridad distribuida. Raid 5 también permite una mayor velocidad de lectura/escritura y un uso más eficiente del espacio de disco. RAID 5 requiere un mínimo de tres discos.

**RAID 10** (RAID 1 + 0) crea varias duplicaciones, en las que los datos se organizan en bandas en varios discos y luego se duplican los conjuntos de discos divididos. RAID 10 ofrece la misma tolerancia al error que RAID 1 con una mayor velocidad de lectura/escritura en un solo volumen Raid 1 o en una sola unidad. El nivel 10 de RAID requiere implementar cuatro unidades.
