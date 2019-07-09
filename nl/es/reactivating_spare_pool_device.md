---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-03"

keywords: bare metal reactivate spare pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Reactivación de un dispositivo de la agrupación de repuesto
{: #bm-reactivating-spare-pools}

Cuando se añade un dispositivo a la agrupación de repuesto, su estado en la Lista de dispositivos cambia de Activo, indicando que el dispositivo es elegible para interacciones estándar, a Agrupación de repuesto. Los dispositivos que forman parte de la agrupación de repuesto están dedicados a esa funcionalidad y no se pueden utilizar para acciones tradicionales cotidianas como otros dispositivos. Para eliminar un dispositivo de la agrupación de repuesto de modo que pueda volver a su funcionalidad tradicional, hay que reactivarlo.
{:shortdesc}

## Reactivación de un dispositivo de la agrupación de repuesto

1. Acceda al [{{site.data.keyword.cloud}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/){: new_window} utilizando sus credenciales exclusivas.
2. Seleccione **Dispositivos > Agrupaciones de repuesto** desde la barra de navegación para acceder a la pantalla *Agrupación de repuesto*.
3. Seleccione **Acciones > Reactivar dispositivo** para el dispositivo deseado.
4. Pulse **Sí** para reactivar el servidor. Pulse **No** para cancelar la acción.

## Pasos siguientes
Después de iniciar el proceso de reactivación, el dispositivo se lleva fuera de línea, el firmware se actualiza y el dispositivo está disponible para su uso regular. El proceso de reactivación dura aproximadamente una hora. Los dispositivos que se eliminan de la agrupación de repuesto ya no son elegibles para su uso como un método de migración tras error. El dispositivo puede volver a la agrupación de repuesto en cualquier momento volviendo a añadir el dispositivo a la agrupación de repuesto. Para obtener más información, consulte [Adición de un dispositivo a la agrupación de repuesto](/docs/bare-metal?topic=bare-metal-adding-spare-pools#adding-spare-pools).
