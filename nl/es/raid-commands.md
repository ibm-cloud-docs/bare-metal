---

copyright:
  years: 1994, 2019
lastupdated: "2018-07-10"

keywords: raid controller commands, raid commands

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Mandatos de controlador RAID
{: #bm-raid-controller-commands}

Utilice el programa de utilidad de línea de mandatos Adaptec para ejecutar mandatos de controlador RAID.
A continuación se muestran los mandatos de controlador RAID más comunes que se pueden utilizar.
{:shortdesc}

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_ lista el tipo de operación, el número de unidad lógica, el tamaño de unidad lógica
y el progreso de la operación. También puede ver el estado de cualquier mandato en segundo plano que se esté ejecutando, como por ejemplo los elementos siguientes:
<ul>
  <li> Reconstrucción más reciente
  <li> Sincronización
  <li> Migración de unidad lógica
  <li> Compactación/expansión
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1</b></code> <br>
_GETCONFIG_ muestra información sobre los controladores, las unidades lógicas y las unidades físicas. Puede ver información como los elementos siguientes:
<ul>
  <li> Tipo de controlador
  <li> BIOS, bloque de arranque, controlador de dispositivo, y versiones de firmware 
  <li> Tipo de dispositivo físico, ID de dispositivo, presencia de PFA 
  <li> Estado de dispositivo físico 
  <li> Información sobre el alojamiento: ventilador, suministro de energía y temperatura
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular</code></b>
_GETLOGS_ le da acceso a los registros de estado y de sucesos de un controlador. _DEVICE xxx_ muestra un registro de los errores de dispositivos que encuentra el controlador.

Consulte el ejemplo siguiente para obtener la salida que se realiza utilizando el mandato _GETLOGS_:
```
driveErrorEntry
smartError.. ............................ false 
vendorID ................................ WDC
serialNumber ............................ WD-XXX
wwn ..................................... xxxxxxxxxxxxxxxx - CC_FILTER
deviceID ................................ 10
productID ............................... WD1003FB
numParityErrors ......................... 0
linkFailures ............................ 0
hwErrors ................................ 0
abortedCmds ............................. 7
mediumErrors ............................ 20
smartWarning ............................ 0
```

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show all | grep -iE "det|cou|tem|SN|S.M|fir” </code></b><br>
Utilice este mandato para mostrar las unidades específicas y cualquier error de unidad posible que pueda tener. 
El ejemplo siguiente muestra la salida:
```
Drive /c0/e252/s0 - Detailed Information: 
Shield Counter = 0
 Media Error Count = 0
 Other Error Count = 0 
Drive Temperature = 24C (75.20 F) 
Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No 
SN = XXXX 
Firmware Revision = SN04

 Drive /c0/e252/s1 - Detailed Information: 
Shield Counter = 0 
Media Error Count = 0 
Other Error Count = 0 
Drive Temperature = 22C (71.60 F) 
Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No 
SN = xxxx 
Firmware Revision = SN03 

Drive /c0/e252/s2 - Detailed Information:
 Shield Counter = 0 
Media Error Count = 0 
Other Error Count = 0 
Drive Temperature = 21C (69.80 F)
 Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No
 SN = xxxx 
Firmware Revision = SN04

 Drive /c0/e252/s3 - Detailed Information:
 Shield Counter = 0 
Media Error Count = 0
 Other Error Count =
 Drive Temperature = 23C (73.40 F) 
Predictive Failure Count = 0
 S.M.A.R.T alert flagged by drive = No 
SN = xxxx
Firmware Revision = SN03  
```

<!--<code><b>/opt/MegaRAID/storcli/storcli64 /c0 show all | less </code></b>-->
<!--You use this command to view RAID health, size, name, and other important information.-->

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show rebuild</code></b>
Este mandato muestra el estado de reconstrucción de todas las unidades y el tiempo estimado para completar la reconstrucción. Verá esta salida al ejecutar el mandato:
```
---------------------------------------------
Drive-ID Progress% Status Estimated Time Left 
---------------------------------------------
/c0/e252/s0 - Not in progress
 /c0/e252/s1 - Not in progress
 /c0/e252/s2 - Not in progress
 /c0/e252/s3 - Not in progress
--------------------------------------------- 
```

<b>RAID alert "Spam"</b>
Cambie la sección "global" de la configuración predeterminada (/opt/lsi/mrmonitor/MegaMonitor/config-current.xml): 
```<global>
 <severity level="FATAL"> 
<do-systemlog/> 
<do-email/>
 </severity>
<severity level="CRITICAL"> 
<do-email/>
 <do-systemlog/> 
</severity>
 <severity level="WARNING">
 <do-email/> 
<do-systemlog/> 
</severity>
 <severity level="INFO"> <do-systemlog/>
</severity>
 </global> 
```
a esto: 
```
<global> 
<severity level="FATAL"> 
<do-systemlog/> 
<do-email/>
 </severity> 
<severity level="CRITICAL"> 
<do-email/> 
<do-systemlog/> 
</severity> 
<severity level="WARNING"> 
<do-systemlog/> 
</severity> 
<severity level="INFO">
<do-systemlog/>
 </severity> 
</global> 
```
**Nota:** Elimine la etiqueta "do-email" para el nivel "WARNING". De forma alternativa, cambie el nivel de seguridad a "INFO".

## Errores de unidad comunes
{: #bm-common-drive-errors}

Los errores de controlador más comunes son errores inteligentes, errores de hardware y errores de soporte. Verá estos errores si una unidad falla. Por lo tanto, debe sustituir la unidad tan pronto como sea posible.

Aunque no son inusuales, los mandatos terminados anormalmente son otro error común. Pero si los mandatos terminados anormalmente aumentan en número (como por ejemplo 100), abra una incidencia de soporte.  

Los errores de enlace pueden indicar que un cable puede necesitar resetearse o sustituirse.

### Información de incidencia de soporte
{: #bm-raid-support}

**Tarjetas RAID de Adaptec** <br>
Asegúrese de incluir la salida completa de `arcconf getconfig 1/arcconf getlogs 1 device tabular` al crear una incidencia de soporte. Proporcionar esta información ayuda al equipo de soporte a identificar el orden de la unidad, la pertenencia de matriz, la geometría de matriz y los problemas de cableado. Esta información es crítica para la recuperación de una configuración de RAID perdida. Otorgar permiso para reiniciar/apagar en la actualización inicial o solicitarlo para que se intercambien en caliente acelera el proceso de incidencia de soporte. 

**Tarjetas RAID de LSI** <br>
Utilice los mandatos siguientes para obtener los archivos de registro para las tarjetas RAID de LSI. Debe incluir la salida completa de estos archivos de registro con la incidencia de soporte.
```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```

**Nota**: Asegúrese de realizar copia de seguridad de cualquier trabajo antes de terminar la resolución de problemas.
