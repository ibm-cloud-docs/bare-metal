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

# RAID-Support-Ticket-Informationen
{:# bm-raid-support-ticket}

Wenn Sie ein Problem oder eine Frage zur Verwendung von RAID auf Ihrem Bare-Metal-Server haben, können Sie Antworten im Forum [IBM developerWorks dW Answers](https://developer.ibm.com/answers/topics/ibm-cloud/){:new_window} finden.
Es ist ebenfalls möglich, ein Support-Ticket zu öffnen. Informationen zu Support-Tickets finden Sie unter [Support-Ticket öffnen.](https://test.cloud.ibm.com/docs/get-support?topic=get-support-getting-customer-support#open-ticket){:new_window}
{:shortdesc}

<!--During a drive or RAID failure, support tickets are automatically created. You can create a support ticket for other problems.--> Beim Erstellen eines Support-Tickets müssen Sie RAID-Protokolldateien bereitstellen. Die Informationen in RAID-Protokolldateien sind für die Wiederherstellung einer verloren gegangenen RAID-Konfiguration von entscheidender Bedeutung.
Mithilfe Ihrer Protokolldateien kann das Support-Team Probleme bei Laufwerkreihenfolge, Array-Zugehörigkeit, Array-Geometrie und Verkabelung ermitteln. Abhängig vom verwendeten RAID-Controller-Typ, Adaptec oder LSI, können Sie RAID-Protokolldateien mit den folgenden Befehlen abrufen. 

**Hinweis:** Wenn Sie bei der Anfangsaktualisierung die Zustimmung zum Neustart/Ausschalten erteilen oder einen Austausch des Laufwerks während des Betriebs anfordern, können Sie den Support-Ticket-Prozess beschleunigen.

<b>Adaptec-RAID-Karten</b><br>
Verwenden Sie den folgenden Befehl, um die Protokolldateien für Adaptec-RAID-Karten abzurufen. Stellen Sie sicher, dass Sie die vollständige Ausgabe dieser Protokolldatei in Ihr Support-Ticket aufnehmen.

`arcconf getconfig 1/arcconf getlogs 1 device tabular`.

<b>LSI-RAID-Karten</b><br>
Verwenden Sie die folgenden Befehle, um die Protokolldateien für LSI-RAID-Karten abzurufen. Sie müssen die vollständige Ausgabe dieser Protokolldateien in Ihr Support-Ticket aufnehmen.
```/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
**Wichtig:** Stellen Sie sicher, dass Sie alle bearbeiteten Daten sichern, bevor die Fehlerbehebung ausgeführt wird.
