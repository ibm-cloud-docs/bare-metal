---
copyright:
  years: 1994, 2018
lastupdated: "2018-5-10"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID-Controller-Befehle

Sie verwenden das Adapatec-Befehlszeilendienstprogramm (Command Line Utility) zum Ausführen von RAID-Controller-Befehlen.
Im Folgenden sind die RAID-Controller-Befehle beschrieben, die am häufigsten verwendet werden.
{:shortdesc}

**Hinweis:** Die Pfade zum Ausführen von storcli-Befehlen unterscheiden sich unter Windows und VMware. Entnehmen Sie den folgenden Beispielen den korrekten Befehlspfad. 

Windows (verwenden Sie CMD)
`C:\Program Files (x86)\MegaRAID Storage Manager>`      
oder
`C:\Program Files\LSIStorCli>`

VMware (Sie müssen storcli installieren, bevor Sie storcli-Befehle ausführen können)
`/opt/lsi/storcli/`

## Gängige RAID-Controller-Befehle

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_ listet den Typ der Operation, die Nummer des logischen Laufwerks, die Größe des logischen Laufwerks und den Fortschritt der Operation auf. Auch der Status von Hintergrundbefehlen wird angezeigt, beispielsweise die folgenden Elemente: 
<ul>
  <li> Letzte Neuerstellung
  <li> Synchronisierung
  <li> Migration des logischen Laufwerks
  <li> Komprimierung/Erweiterung
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1</b></code> <br>
_GETCONFIG_ listet Informationen zu Controllern, logischen Laufwerken und physischen Laufwerken auf. Es werden Informationen wie die folgenden angezeigt: 
<ul>
  <li> Controllertyp
  <li> Version des BIOS, des Bootblocks, des Einheitentreibers und der Firmware
  <li> Physischer Einheitentyp, Einheiten-ID, Vorhandensein von PFA
  <li> Physischer Einheitenstatus
  <li> Gehäuseinformationen: Lüfter, Netzteil und Temperatur
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular</code></b>
Mit _GETLOGS_ erhalten Sie Zugriff auf die Status- und Ereignisprotokolle eines Controllers. Mit _DEVICE xxx_ wird ein Protokoll aller Einheitenfehler angezeigt, die vom Controller erkannt werden. 

Das folgende Beispiel zeigt die Ausgabe des Befehls _GETLOGS_: 
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
Mit diesem Befehl können Sie die einzelnen Laufwerke und mögliche Laufwerkfehler anzeigen.
Das folgende Beispiel zeigt die Ausgabe: 
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
Mit diesem Befehl wird der Neuerstellungsstatus aller Laufwerke und die geschätzte Dauer der Neuerstellung angezeigt. Wenn Sie den Befehl ausführen, wird die folgende Ausgabe angezeigt: 
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

<b>RAID-Alert "Spam"</b>
Ändern Sie den Abschnitt "global" der Standardkonfiguration (/opt/lsi/mrmonitor/MegaMonitor/config-current.xml): 
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
Geänderte Version des Abschnitts: 
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
**Hinweis:** Entfernen Sie den Tag "do-email" für die Stufe "WARNING". Alternativ können Sie die Sicherheitsstufe in "INFO" ändern. 

## Häufig auftretende Laufwerkfehler

Die Laufwerkfehler, die am häufigsten auftreten, sind SMART-Fehler, Hardwarefehler und Datenträgerfehler. Diese Fehler werden angezeigt, wenn ein Laufwerk defekt ist. Daher müssen Sie das Laufwerk so schnell wie möglich austauschen. 

Abgebrochene Befehle sind nicht ungewöhnlich, sondern ein weiterer häufig auftretender Fehler. Öffnen Sie ein Support-Ticket, wenn die Anzahl der abgebrochenen Befehle deutlich zunimmt (z. B. auf 100).   

Verbindungsfehler können darauf hinweisen, dass ein Kabel neu eingesteckt oder ausgetauscht werden muss. 

## Support-Ticket-Informationen

<b>Adaptec-RAID-Karten</b>
Stellen Sie sicher, dass Sie die vollständige Ausgabe des Befehls `arcconf getconfig 1/arcconf getlogs 1 device tabular` angeben, wenn Sie ein Support-Ticket erstellen. Mithilfe dieser Informationen kann das Support-Team Probleme bei Laufwerkreihenfolge, Array-Zugehörigkeit, Array-Geometrie und Verkabelung ermitteln. Diese Informationen sind für die Wiederherstellung einer verloren gegangenen RAID-Konfiguration von entscheidender Bedeutung. Wenn Sie bei der Anfangsaktualisierung die Zustimmung zum Neustart/Ausschalten erteilen oder einen Austausch während des Betriebs anfordern, können Sie den Support-Ticket-Prozess beschleunigen. 

<b>LSI-RAID-Karten</b>
Verwenden Sie die folgenden Befehle, um die Protokolldateien für LSI-RAID-Karten abzurufen. Sie müssen die vollständige Ausgabe dieser Protokolldateien in Ihr Support-Ticket aufnehmen. 
```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```

**Hinweis**: Stellen Sie sicher, dass Sie alle bearbeiteten Daten sichern, bevor die Fehlerbehebung ausgeführt wird. 
