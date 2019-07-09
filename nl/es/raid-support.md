---

copyright:
  years: 1994, 2019
lastupdated: "2018-5-31"

keywords: raid support, raid help

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Información de incidencia de soporte de RAID
{:# bm-raid-support-ticket}

Si tiene algún problema o pregunta sobre el uso de RAID en el servidor nativo, es posible que encuentre una respuesta en el foro [IBM developerWorks dW Answers](https://developer.ibm.com/answers/topics/ibm-cloud/){:new_window}.
También puede abrir una incidencia de soporte. Para obtener información sobre incidencias de soporte, consulte [Cómo abrir una incidencia de soporte.](https://test.cloud.ibm.com/docs/get-support?topic=get-support-getting-customer-support#open-ticket){:new_window}
{:shortdesc}

<!--During a drive or RAID failure, support tickets are automatically created. You can create a support ticket for other problems.--> Cuando se crea una incidencia de soporte, tiene que proporcionar los archivos de registro de RAID. La información de los archivos de registro de RAID es crítica para la recuperación de una configuración de RAID perdida. Proporcionar los aqrchivos de registro ayuda al equipo de soporte a identificar el orden de la unidad, la pertenencia de matriz, la geometría de matriz y los problemas de cableado. Según el tipo de controlador RAID que utilice, Adaptec o LSI, utilice los mandatos siguientes para obtener archivos de registro de RAID.

**Nota:** Otorgar permiso para reiniciar/apagar en la actualización inicial o solicitar que el disco se intercambie en caliente acelera el proceso de incidencia de soporte.

<b>Tarjetas RAID de Adaptec</b><br>
Utilice el mandato siguiente para obtener los archivos de registro para las tarjetas RAID de Adaptec. Asegúrese de incluir la salida completa de este archivo de registro en la incidencia de soporte.

`arcconf getconfig 1/arcconf getlogs 1 device tabular`.

<b>Tarjetas RAID de LSI</b><br>
Utilice los mandatos siguientes para obtener los archivos de registro para las tarjetas RAID de LSI. Debe incluir la salida completa de estos archivos de registro en la incidencia de soporte.
```/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
**Importante:** Asegúrese de realizar copia de seguridad de cualquier trabajo antes de empezar la resolución de problemas.
