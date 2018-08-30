---



copyright:
  years: 2014, 2018
lastupdated: "2018-06-21"


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

La agrupación de repuesto es una forma de migración tras error en el que determinados dispositivos son designados como repuestos en caliente y pueden asumir el flujo de trabajo de un dispositivo primario si este falla. Para que un dispositivo sea designado como repuesto en caliente, debe añadirse a la agrupación de repuesto y asociarse a un dispositivo primario. Complete los siguientes pasos para añadir un dispositivo a la agrupación de repuesto:
{:shortdesc}

1. Acceda al [{{site.data.keyword.slportal}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com/){: new_window} utilizando sus credenciales exclusivas.
2. Seleccione **Dispositivos > Agrupaciones de repuesto** desde la barra de navegación para acceder a la pantalla *Agrupación de repuesto*.
3. Pulse el enlace **Añadir a agrupación de repuesto**.
   
   Se rellenará una lista de dispositivos eligibles para añadir a la agrupación de repuesto.
   {:tip}
   
4. Seleccione los dispositivos que se añadirán a la agrupación de repuesto.
5. Pulse **Añadir dispositivos seleccionados**.
6. Pulse **Confirmar** para añadir los dispositivos a la agrupación de repuesto. 

## Pasos siguientes
Después de iniciar la transferencia de un dispositivo a la agrupación de repuesto, el dispositivo se transfiere a la agrupación de repuesto en una hora. Cuando el dispositivo se activa en la agrupación de repuesto, se muestra en la pantalla Agrupación de repuesto y se puede designar como repuesto en caliente para un dispositivo primario.
