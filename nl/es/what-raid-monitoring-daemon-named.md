---
copyright:
  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Nombre y ubicación del daemon de supervisión de RAID
En el hardware existente, {{site.data.keyword.cloud}} utiliza principalmente tarjetas Adaptec y RAID LSI, con algunas excepciones. La siguiente tabla describe las ubicaciones del gestor de RAID, las ubicaciones del supervisor, las configuraciones y los valores de alerta de RAID.

Puede configurar alertas de RAID para eludir el proceso de supervisión del portal cambiando el servidor SMTP y el destino de correo electrónico de notificación en la configuración de una tarjeta RAID. Si cambia estas configuraciones, IBM no puede notificarle los problemas de RAID ni realizar automáticamente un seguimiento del problema hasta su resolución. No modifique la configuración proporcionada a menos que conozca los riesgos.

<caption>Tabla 1. Configuraciones y valores de RAID</caption>

||LSI en Linux|LSI en Windows|Adaptec en Linux|Adaptec en Windows|
|---|---|---|---|---|
|**Nombre de gestor**|LSI MegaRAID Storage Manager|LSI MegaRAID Storage Manager|Adaptec Storage Manager|Adaptec Storage Manager|
|**Ubicación de gestor**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Nombre de supervisor**|MR_Monitor|MRMonitor|Adaptec Event Manager|Adaptec Event Manager|
|**Ubicación de supervisor**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Nombre de proceso**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**Ubicación de registro**|Ubicación predeterminada de registro de mensajes para el SO, como /var/log/messages|Sólo GUI|/usr/StorMan/RaidEvtA.log|Sólo GUI|
|**Destino de correo electrónico de notificación**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**Formato de origen de correo electrónico de notificación**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**Puerto de correo electrónico**|25|25|25|25|
|**Servidor SMTP**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**Opciones de notificación alternativas**|Cambiar el servidor SMTP a un servidor SMTP local. El servidor SMTP local necesita las configuraciones adecuadas de cortafuegos.|Cambiar el servidor SMTP a un servidor SMTP local. El servidor SMTP local necesita las configuraciones adecuadas de cortafuegos.|Cambiar el servidor SMTP a un servidor SMTP local. El servidor SMTP local necesita las configuraciones adecuadas de cortafuegos.|Cambiar el servidor SMTP a un servidor SMTP local. El servidor SMTP local necesita las configuraciones adecuadas de cortafuegos.|
