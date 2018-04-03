---



copyright:
  years: 2016
lastupdated: "2016-01-19"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Einführung in {{site.data.keyword.baremetal_short}}

{{site.data.keyword.baremetal_long}} stellen Ihnen Leistung und Steuerung zur Verfügung. {{site.data.keyword.baremetal_short}} können in Hypervisoren nicht ausgeführt werden, Sie erhalten anderenfalls einen Low-Level-Zugriff auf die Hardwareressourcen. Außerdem können Sie den Server nicht für andere Kunden freigeben!
{:shortdesc}

Sie können beim Erstellen der {{site.data.keyword.baremetal_short}} die Spezifikationen der Prozessoren und der Region an das Betriebssystem und an die Festplatte anpassen.

Gehen Sie wie folgt vor, um {{site.data.keyword.baremetal_short}} bereitzustellen:
  1. Gehen Sie zu **Compute > {{site.data.keyword.baremetal_short}}** und klicken Sie auf **Hinzufügen**.
  2. Wählen Sie den Standort aus, an dem die {{site.data.keyword.baremetal_short}}-Instanz bereitgestellt werden soll. Dies ist ein Rechenzentrum in einer der {{site.data.keyword.Bluemix}}-Regionen.
  3. Wählen Sie die Konfiguration der Server aus. Diese Konfiguration wird auf alle Server angewendet, die für diese Instanz erstellt wurden.
  4. Wählen Sie die Anzahl der Server aus, die für diese Instanz erstellt werden sollen. Geben Sie für jeden Server einen eindeutigen Hostnamen ein.
  5. **Optional:** Geben Sie in einem Script oder in einer Textdatei eine URL an, die Sie für die Konfiguration des Servers definiert haben. Das Bereitstellungsscript muss ein HTTPS-Protokoll verwenden. Das Script wird heruntergeladen und nach der Bereitstellung der Instanz ausgeführt, wenn möglich. Wenn die URL keinem ausführbaren Script zugeordnet wurde, wird das Script nur heruntergeladen.
  6. Wählen Sie das Betriebssystem für die Server aus. Dieses Betriebssystem wird auf alle Server angewendet, die für diese Instanz erstellt wurden.

Innerhalb einer Stunde werden Ihre {{site.data.keyword.baremetal_short}} bereitgestellt und können verwendet werden.
