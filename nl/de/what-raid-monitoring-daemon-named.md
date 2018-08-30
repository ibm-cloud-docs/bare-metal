---
copyright:
  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Name und Position des RAID-Überwachungsdämons
{{site.data.keyword.cloud}} verwendet hauptsächlich Adaptec- und LSI-RAID-Karten mit einigen Ausnahmen für ältere Hardware. In der folgenden Tabelle sind die Positionen des RAID-Managers, die Überwachungspositionen, die Konfigurationen und die RAID-Alerteinstellungen aufgeführt. 

Sie können RAID-Alerts so konfigurieren, dass der Portalüberwachungsprozess umgangen wird, indem Sie den SMTP-Server und das Ziel der Benachrichtigungs-E-Mail in der Konfiguration für eine bestimmte RAID-Karte ändern. Wenn Sie diese Konfigurationen ändern, kann IBM Sie weder über RAID-Probleme informieren noch das Problem bis zur Problemlösung automatisch verfolgen. Ändern Sie die bereitgestellte Konfiguration nur, wenn Sie die Risiken kennen.

<caption>Tabelle 1. RAID-Konfigurationen und -Einstellungen</caption>

||LSI Linux|LSI Windows|Adaptec Linux|Adaptec Windows|
|---|---|---|---|---|
|**Manager-Name**|LSI MegaRAID Storage Manager|LSI MegaRAID Storage Manager|Adaptec Storage Manager|Adaptec Storage Manager|
|**Manager-Position**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Monitorname**|MR_Monitor|MRMonitor|Adaptec Event Manager|Adaptec Event Manager|
|**Monitorposition**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Prozessname**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**Protokollposition**|Standardposition des Nachrichtenprotokolls für das Betriebssystem wie /var/log/messages|Nur grafische Benutzeroberfläche|/usr/StorMan/RaidEvtA.log|Nur grafische Benutzeroberfläche|
|**Zieladresse für Benachrichtigungs-E-Mail**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**Quellenformat für Benachrichtigungs-E-Mail**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**E-Mail-Port**|25|25|25|25|
|**SMTP-Server**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**Alternative Benachrichtigungsoptionen**|Ändern Sie den SMTP-Server in einen lokalen SMTP-Server. Für den lokalen SMTP-Server sind entsprechende Firewallkonfigurationen erforderlich.|Ändern Sie den SMTP-Server in einen lokalen SMTP-Server. Für den lokalen SMTP-Server sind entsprechende Firewallkonfigurationen erforderlich.|Ändern Sie den SMTP-Server in einen lokalen SMTP-Server. Für den lokalen SMTP-Server sind entsprechende Firewallkonfigurationen erforderlich.|Ändern Sie den SMTP-Server in einen lokalen SMTP-Server. Für den lokalen SMTP-Server sind entsprechende Firewallkonfigurationen erforderlich.|
