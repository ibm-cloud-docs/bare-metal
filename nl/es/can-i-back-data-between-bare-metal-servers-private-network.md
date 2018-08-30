---

copyright:
  years: 1994, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Copia de seguridad y recuperación

{{site.data.keyword.Bluemix_notm}} proporciona una variedad de [soluciones de almacenamiento y copia de seguridad](https://www.softlayer.com/cloud-storage) escalables para satisfacer sus necesidades de seguridad. Sin embargo, {{site.data.keyword.Bluemix_notm}} no realiza copias de seguridad de dispositivos de cliente. Algún usuario de la cuenta debe iniciar todas las copias de seguridad planificadas y puntuales en sus dispositivos.

Si existen dos o más {{site.data.keyword.baremetal_short}} en una cuenta, se puede hacer una copia de seguridad de los datos de un dispositivo en otro. No se aplica ningún límite de ancho de banda para el tráfico de red privada, de modo que los datos se pueden transferir o se puede hacer una copia de seguridad de ellos en cualquier momento en cualquier dispositivo que comparta una cuenta. Hay disponibles varias soluciones de copia de seguridad para {{site.data.keyword.baremetal_short}}, incluidas las siguientes soluciones:

1. [La copia de seguridad de Evault](../infrastructure/backup/index.html) es una solución de copia de seguridad empresarial que puede automatizar las copias de seguridad en varios servidores. Los datos se almacenan en una SAN (red de área de almacenamiento) empresarial.
* [El almacenamiento adjunto en red (NAS)](../infrastructure/network-attached-storage/nas.html) es un estándar de la industria y proporciona almacenamiento fuera del servidor para datos críticos. Los datos se almacenan en una SAN (red de área de almacenamiento) empresarial.
* [R1Soft CDP](../infrastructure/backup/r1soft.html) proporciona copias de seguridad de servidor de disco a disco de alto rendimiento, con gestión central y repositorio de datos. R1Soft CDP protege los datos a nivel de bloque, y los bloques de disco exclusivos del servidor se almacenan solo una vez en todos los puntos de recuperación, lo que aumenta la eficiencia del almacenamiento.
