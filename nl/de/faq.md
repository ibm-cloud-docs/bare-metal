---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Häufig gestellte Fragen: Bare-Metal-Server

## Warum fragt das BIOS nach einem Kennwort?

Zurzeit kann {{site.data.keyword.cloud}} aus verschiedenen Gründen Ihnen keinen direkten Zugriff auf Ihr BIOS bereitstellen.. Das bedeutet aber nicht, dass Sie keine Änderungen im BIOS vornehmen können. Wenn Sie etwas im BIOS ändern müssen, unter anderem die Bootreihenfolge, erstellen Sie im [Kundenportal](control.softlayer.com) ein Ticket unter "Support > Ticket hinzufügen" und fordern Sie die erforderlichen Änderungen an.

\*\*HINWEIS\*\* Dazu ist ein Neustart Ihres Servers notwendig. Geben Sie daher einen Neustart frei und/oder legen Sie einen Zeitrahmen fest, in dem die Änderung vorgenommen werden soll.

## Bieten Sie kostenloses erneutes Laden des Betriebssystems an?

Das automatisierte erneute Laden des Betriebssystems ist kostenlos und kann über das [Kundenportal](control.softlayer.com) durchgeführt werden. Dazu gehören angepasste erneute Ladevorgänge des Betriebssystems (Betriebssystem ändern, Steuerkonsolen hinzufügen/entfernen, Partitionen bearbeiten usw.). Ausführliche Informationen zum erneuten Laden eines Betriebssystems finden Sie unter [Vorgehensweise zum erneuten Laden des Betriebssystems](../vsi/vsi_perform_os_reload.html).


## Das primäre Laufwerk auf dem Bare-Metal-Server wird als "/dev/sdb" angezeigt. Was ist falsch?

Dies kann daran liegen, dass die virtuelle IPMI-Platte den "/dev/sda"-Slot belegt. Dies kann sicher inaktiviert werden, in dem Sie eine Verbindung zu IPMIView herstellen und zur Registerkarte "Virtueller Datenträger" navigieren. Wählen Sie **Optionen > Inaktivieren** aus und klicken Sie auf die Schaltfläche **Anwenden**, um die Änderung zu übernehmen. Wenn der {{site.data.keyword.baremetal_short}} neu gebootet wird, wird für das primäre Laufwerk "/dev/sda" angezeigt.


## Warum stimmt die CPU-Geschwindigkeit nicht?

Wenn Sie sich bei einem Server anmelden, um die CPU-Informationen zu prüfen, stellen Sie fest, dass die Geschwindigkeit der Prozessoren falsch war. Diese Abweichung kann an Enhanced Intel SpeedStep Technology (EIST) liegen. EIST ist der Intel-Name für die Technologie der dynamischen Skalierungstechnologie. Diese Technologie heißt auch *CPU-Drosselung* oder in älteren Systemen *Bus Slewing*. In einigen AMD-Systemen gibt es ähnliche Technologien, die *Cool'N'Quiet* oder *PowerNow!* heißen. Obwohl sie nicht alle exakt dieselbe Technologie darstellen, haben Sie doch dasselbe Ziel. Der Stromverbrauch und die Hitzeentwicklung sollen gesenkt werden, wenn der Prozessor nicht stark beansprucht wird, indem die CPU-Geschwindigkeit verlangsamt wird. Wenn der Server wieder eine Last verarbeitet, wird die Taktgeschwindigkeit wieder erhöht. 

Wenn Sie wissen möchte, ob der Intel-Prozessor Ihres Servers SpeedStep unterstützt, besuchen Sie das Kundenportal: 
1. Klicken Sie auf **Einheiten**.
* Ermitteln Sie Ihren Server in der Liste.
* Klicken Sie auf den Servernamen, um **Einheitendetails** anzuzeigen.
* Suchen Sie den Teilbereich mit dem Namen **Hardware**, um die Modellnummer Ihres Serverprozessors für die CPU-Geschwindigkeit zu suchen.
* Notieren Sie sich die Modellnummer des Serverprozessors. Gehen Sie zum [Intel Processor Finder](http://processorfinder.intel.com/) und suchen Sie mit dieser Nummer nach weiteren Informationen zum Prozessor und zur Angabe, ob Enhanced Intel SpeedStep Technology (EIST) unterstützt wird.

EIST ist eine bewährte Technologie. Es gibt keinen Grund, EIST zu inaktivieren. Wenn Sie jedoch entscheiden, dass Sie diese Funktion nicht nutzen möchten, öffnen Sie ein Ticket beim Support-Team, um die Funktion inaktivieren zu lassen. Um diese Funktion zu inaktivieren, muss der Server neu gestartet werden.


## Was passiert, wenn der Bare-Metal-Server veraltete Firmware besitzt?

Wie bei anderen Software-Updates auch ist es wichtig, die Firmware aktuell zu halten, um eine optimale Einheitenkompatibilität und Stabilität zu gewährleisten. Wenn die {{site.data.keyword.baremetal_short}}-Firmware veraltet ist, muss ein Firmware-Update während des [erneuten Ladens des Betriebssystems](../infrastructure/software/vsi_reload_os.html) im [Kundenportal](https://control.softlayer.com) initiiert werden.

Sie können die Firmware auch aktualisieren, indem Sie den Bare-Metal-Server aus der Einheitenliste auswählen und dann aus der Dropdown-Liste des Aktionsmenüs **Firmware aktualisieren** auswählen.
