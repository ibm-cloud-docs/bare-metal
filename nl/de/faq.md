---

copyright:
  years: 2014, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Häufig gestellte Fragen: Bare-Metal-Server

## Warum fragt das BIOS nach einem Kennwort?

Zurzeit stellt {{site.data.keyword.cloud}} Ihnen aus einer Reihe von Gründen keinen direkten Zugriff auf Ihr BIOS zur Verfügung. Sie können das BIOS jedoch ändern. Wenn Sie eine Einstellung im BIOS einschließlich der Bootreihenfolge ändern müssen, erstellten Sie über das [Kundenportal](https://control.softlayer.com/) unter "Support > Ticket hinzufügen" ein Ticket und fordern Sie die genauen Änderungen an, die Sie benötigen. 

\*\*HINWEIS\*\* Dies erfordert den Neustart Ihres Servers. Sie müssen daher den Neustart genehmigen und/oder einen Zeitrahmen angeben, in dem die Änderung vorgenommen werden soll. 

## Bieten Sie kostenloses erneutes Laden des Betriebssystems an?

Das automatisierte erneute Laden des Betriebssystems ist kostenlos und kann über das [Kundenportal](https://control.softlayer.com/) durchgeführt werden. Dazu gehören angepasste erneute Ladevorgänge des Betriebssystems (Betriebssystem ändern, Steuerkonsolen hinzufügen/entfernen, Partitionen bearbeiten usw.).  Weitere Informationen zum erneuten Laden eines Betriebssystems finden Sie unter [Vorgehensweise zum erneuten Laden des Betriebssystems](../vsi/vsi_perform_os_reload.html). 


## Das primäre Laufwerk auf dem Bare-Metal-Server wird als "/dev/sdb" angezeigt. Was ist falsch?

Dies kann daran liegen, dass die virtuelle IPMI-Platte "/dev/sda" verwendet. Sie können diese problemlos inaktivieren, indem Sie eine Verbindung zu IPMIView herstellen und zur Registerkarte für virtuellen Datenträger navigieren. Wählen Sie **Optionen > Inaktivieren** aus und klicken Sie auf die Schaltfläche **Anwenden**, um die Änderung zu übernehmen. Wenn der {{site.data.keyword.baremetal_short}} neu gebootet wird, wird für das primäre Laufwerk "/dev/sda" angezeigt.


## Warum stimmt die CPU-Geschwindigkeit nicht?

Wenn Sie sich bei einem Server anmelden, um die CPU-Informationen zu prüfen, stellen Sie fest, dass die Geschwindigkeit der Prozessoren falsch war. Diese Abweichung kann an Enhanced Intel SpeedStep Technology (EIST) liegen. EIST ist der Intel-Name für die Technologie der dynamischen Skalierungstechnologie.  Diese Technologie heißt auch *CPU-Drosselung* oder in älteren Systemen *Bus Slewing*.  Einige AMD-Systeme verfügen über ähnliche Technologien, die als *Cool'N'Quiet* oder *PowerNow!* bezeichnet werden. Obwohl diese Technologien nicht gleich sind, verfolgen sie dasselbe Ziel: die Reduzierung des Stromverbrauchs und der Wärmeentwicklung, wenn der Prozessor nicht stark beansprucht ist, indem die CPU-Geschwindigkeit verlangsamt wird. Wenn der Server wieder eine Last verarbeitet, wird die Taktgeschwindigkeit wieder erhöht.

Wenn Sie wissen möchten, ob der Intel-Prozessor Ihres Servers SpeedStep unterstützt, führen Sie im Kundenportal die folgende Prozedur aus: 
1. Klicken Sie auf **Einheiten**.
* Ermitteln Sie Ihren Server in der Liste.
* Klicken Sie auf den Servernamen, um **Einheitendetails** anzuzeigen.
* Suchen Sie den Teilbereich mit dem Namen **Hardware**, um die Modellnummer Ihres Serverprozessors für die CPU-Geschwindigkeit zu suchen.
* Notieren Sie sich die Modellnummer des Serverprozessors. Gehen Sie zum [Intel Processor Finder](http://processorfinder.intel.com/) und suchen Sie mit dieser Nummer nach weiteren Informationen zum Prozessor und zur Angabe, ob Enhanced Intel SpeedStep Technology (EIST) unterstützt wird.

EIST ist eine bewährte Technologie. Es ist nicht üblich, dass Sie EIST inaktivieren müssen. Wenn Sie jedoch entscheiden, dass Sie diese Funktion nicht nutzen möchten, öffnen Sie ein Ticket beim Support-Team, um die Funktion inaktivieren zu lassen.  Um diese Funktion zu inaktivieren, wird der Server neu gestartet. 


## Wie gehe ich vor, wenn die Firmware meines Bare-Metal-Servers veraltet ist? 

Wie bei anderen Software-Updates auch ist es wichtig, die Firmware aktuell zu halten, um eine optimale Einheitenkompatibilität und Stabilität zu gewährleisten. Wenn die {{site.data.keyword.baremetal_short}}-Firmware veraltet ist, muss ein Firmware-Update während des [erneuten Ladens des Betriebssystems](../infrastructure/software/vsi_reload_os.html) im [Kundenportal](https://control.softlayer.com) initiiert werden.

Sie können die Firmware auch aktualisieren, indem Sie den Bare-Metal-Server in der Einheitenliste auswählen und anschließend im Aktionsmenü **Firmware aktualisieren** auswählen. 

## Was geschieht mit Laufwerken in Bare-Metal-Servern, wenn ein Kunde sie nicht mehr benötigt? 

Nach der Stornierung wird ein Server automatisch in ein VLAN für Zurückforderung verschoben, wo er eine bestimmte Zeit lang verbleibt. Nach dieser Zeit beginnen die Zurückforderungsprozesse und das Laufwerk wird mit DOD 5220.22-M-Algorithmen bereinigt. Die Zurückforderung wird mithilfe der Seriennummer des Laufwerks verfolgt. Nach der Fertigstellung wird der Server für die erneute Zuordnung in die Bereitstellung verschoben. Bei einer Laufwerkstörung erfolgt ein manueller Eingriff und die Laufwerke erreichen das Ende des Lebenszyklus. 

Der Prozess für das Ende des Lebenszyklus wird eingeleitet, wenn eine Störung vorliegt oder wenn das Alter oder die Größe nicht mehr unterstützt wird. Wenn eine dieser Bedingungen erfüllt ist, werden die Laufwerke wie oben beschrieben bereinigt. Nach der Beendigung des Bereinigungsprozesses wird das Laufwerk durch Zerbrechen, Zerkleinern oder Shreddern physisch vernichtet. Der Prozess der physischen Vernichtung wird mithilfe der Seriennummer des Laufwerks verfolgt. 
