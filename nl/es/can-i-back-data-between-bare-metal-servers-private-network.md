---

copyright:
  years: 1994, 2019
lastupdated: "2019-05-02"

keywords: back up, recovery, IBM Cloud Backup, r1soft

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Copia de seguridad y recuperación
{: #sm-back-up-recovery}

{{site.data.keyword.Bluemix_notm}} proporciona una variedad de [soluciones de almacenamiento y copia de seguridad ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/cloud/storage){: new_window} escalables para satisfacer sus necesidades de seguridad. Sin embargo, {{site.data.keyword.Bluemix_notm}} no realiza copias de seguridad de dispositivos de cliente. Algún usuario de la cuenta debe iniciar todas las copias de seguridad planificadas y puntuales en sus dispositivos.

Si existen dos o más {{site.data.keyword.baremetal_short}} en una cuenta, se puede hacer una copia de seguridad de los datos de un dispositivo en otro. No se aplica ningún límite de ancho de banda para el tráfico de red privada, de modo que los datos se pueden transferir o se puede hacer una copia de seguridad de ellos en cualquier momento en cualquier dispositivo que comparta una cuenta. Hay disponibles varias soluciones de copia de seguridad para {{site.data.keyword.baremetal_short}}, incluidas las siguientes soluciones:

* [IBM Cloud Backup](/docs/infrastructure/Backup?topic=Backup-getting-started#getting-started) es una solución de copia de seguridad empresarial que puede automatizar las copias de seguridad en varios servidores. Los datos se almacenan en una SAN (red de área de almacenamiento) empresarial.
* [El almacenamiento adjunto en red (NAS)](/docs/infrastructure/network-attached-storage?topic=network-attached-storage-GettingStarted#GettingStarted) es un estándar de la industria y proporciona almacenamiento fuera del servidor para datos críticos. Los datos se almacenan en una SAN (red de área de almacenamiento) empresarial.
* [R1Soft CDP](/docs/infrastructure/software?topic=software-ordering-r1soft#ordering-r1soft) proporciona copias de seguridad de servidor de disco a disco de alto rendimiento, con gestión central y repositorio de datos. R1Soft CDP protege los datos a nivel de bloque, y los bloques de disco exclusivos del servidor se almacenan solo una vez en todos los puntos de recuperación, lo que aumenta la eficiencia del almacenamiento.
