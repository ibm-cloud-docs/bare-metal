---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Name und Standort des RAID-Überwachungsdämons
{{site.data.keyword.cloud}} X verwendet primär Adaptec- und LSI-RAID-Karten mit einigen Ausnahmen für traditionelle Hardware. In der folgenden Tabelle sind die RAID-Manager-Standorte, Überwachungsstandorte, Konfigurationen und RAID-Alerteinstellungen aufgeführt.

Sie können RAID-Alerts konfigurieren, um den Portalüberwachungsprozess zu umgehen, indem Sie den SMTP-Server und das Ziel der Benachrichtigungs-E-Mail in der Konfiguration für eine bestimmte RAID-Karte ändern. Wenn diese Konfigurationen geändert werden, kann IBM Sie nicht über RAID-Probleme informieren und kann das Problem nicht bis zur Problemlösung automatisch verfolgen. Ändern Sie die bereitgestellte Konfiguration nur, wenn Sie die Risiken kennen. 

||LSI - Linux|LSI - Windows|Adaptec - Linux|Adaptec - Windows|
|---|---|---|---|---|
|**Manager-Name**|LSI MegaRAID Storage Manager|LSI MegaRAID Storage Manager|Adaptec Storage Manager|Adaptec Storage Manager|
|**Manager-Position**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Monitorname**|MR_Monitor|MRMonitor|Adaptec Event Manager|Adaptec Event Manager|
|**Monitorposition**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Prozessname**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**Protokollposition**|Protokollposition für Standardnachrichten für Betriebssystem, z. B. /var/log/messages|Nur grafische Benutzeroberfläche |/usr/StorMan/RaidEvtA.log|Nur grafische Benutzeroberfläche |
|**Zieladresse für Benachrichtigungs-E-Mail**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**Quellenformat für Benachrichtigungs-E-Mail**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**E-Mail-Port**|25|25|25|25|
|**SMTP-Server**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**Alternative Benachrichtigungsoptionen**|Ändern Sie den SMTP-Server zu einem SMTP-Server. Der lokale SMTP-Server benötigt entsprechende Firewallkonfigurationen.|Ändern Sie den SMTP-Server zu einem SMTP-Server. Der lokale SMTP-Server benötigt entsprechende Firewallkonfigurationen.|Ändern Sie den SMTP-Server zu einem SMTP-Server. Der lokale SMTP-Server benötigt entsprechende Firewallkonfigurationen.|Ändern Sie den SMTP-Server zu einem SMTP-Server. Der lokale SMTP-Server benötigt entsprechende Firewallkonfigurationen.|
