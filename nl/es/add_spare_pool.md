---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

keywords: bare metal, spare pools

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Adición de agrupaciones de repuesto
{: #adding-spare-pools}

El uso de agrupaciones de repuesto es una forma de mantener determinados dispositivos que se han designado como repuestos y tener la capacidad de asumir el flujo de trabajo de un dispositivo primario o actuar como un nuevo dispositivo en la flota del cliente. Para que un dispositivo sea designado como repuesto, debe añadirse a la agrupación de repuesto y asociarse a un dispositivo primario. Siga los pasos siguientes para añadir un dispositivo a la agrupación de repuesto.
{:shortdesc}

1. Acceda a la [consola de {{site.data.keyword.cloud}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/){: new_window}utilizando sus credenciales exclusivas.
2. Seleccione **Dispositivos > Agrupaciones de repuesto** desde la barra de navegación para acceder a la pantalla *Agrupación de repuesto*.
3. Pulse el enlace **Añadir a agrupación de repuesto**.

   Se rellenará una lista de dispositivos elegibles para añadir a la agrupación de repuesto.
   {:tip}

4. Seleccione los dispositivos que se añadirán a la agrupación de repuesto.
5. Pulse **Añadir dispositivos seleccionados**.
6. Pulse **Confirmar** para añadir los dispositivos a la agrupación de repuesto.

## Pasos siguientes
Después de iniciar la transferencia de un dispositivo a la agrupación de repuesto, el dispositivo se transfiere a la agrupación de repuesto en una hora. Cuando el dispositivo se activa en la agrupación de repuesto, se muestra en la pantalla Agrupación de repuesto y se puede designar como repuesto en caliente para un dispositivo primario.
