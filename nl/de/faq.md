---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-16"

keywords: bare metal, faq, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Häufig gestellte Fragen: Bare-Metal-Server
{: #bm-faq}

## Was ist der UEFI-Bootmodus?
{: faq}
Unified Extensible Firmware Interface (UEFI) ist eine Spezifikation für die Softwareschnittstelle zwischen einem Betriebssystem und der Firmware.

Die IBM Cloud-Unterstützung für den BIOS-Bootmodus wird zugunsten von UEFI allmählich eingestellt.

Weitere Informationen zu UEFI finden Sie in der Dokumentation Ihres Hardwareherstellers oder unter [https://uefi.org/](https://uefi.org/).

## Warum fragt das BIOS nach einem Kennwort?
{: faq}

Zurzeit stellt {{site.data.keyword.cloud}} Ihnen aus einer Reihe von Gründen keinen direkten Zugriff auf Ihr BIOS zur Verfügung. Sie können das BIOS jedoch ändern. Wenn Sie eine Einstellung im BIOS einschließlich der Bootreihenfolge ändern müssen, erstellten Sie über das [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/){: new_window} unter "Support > Ticket hinzufügen" ein Ticket und fordern Sie die genauen Änderungen an, die Sie benötigen.

\*\*HINWEIS\*\* Dies erfordert den Neustart Ihres Servers. Sie müssen daher den Neustart genehmigen und/oder einen Zeitrahmen angeben, in dem die Änderung vorgenommen werden soll.

## Bieten Sie kostenloses erneutes Laden des Betriebssystems an?
{: faq}

Das automatisierte erneute Laden des Betriebssystems ist kostenlos und kann über das [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/){: new_window} durchgeführt werden. Dazu gehören angepasste erneute Ladevorgänge des Betriebssystems (Betriebssystem ändern, Steuerkonsolen hinzufügen/entfernen, Partitionen bearbeiten usw.).  Weitere Informationen zum erneuten Laden eines Betriebssystems finden Sie unter [Vorgehensweise zum erneuten Laden des Betriebssystems](/docs/infrastructure/software?topic=software-reloading-the-os).


## Das primäre Laufwerk auf dem Bare-Metal-Server wird als "/dev/sdb" angezeigt. Was ist falsch?
{: faq}

Dies kann daran liegen, dass die virtuelle IPMI-Platte "/dev/sda" verwendet. Sie können diese problemlos inaktivieren, indem Sie eine Verbindung zu IPMIView herstellen und zur Registerkarte für virtuellen Datenträger navigieren. Wählen Sie **Optionen > Inaktivieren** aus und klicken Sie auf die Schaltfläche **Anwenden**, um die Änderung zu übernehmen. Wenn der {{site.data.keyword.baremetal_short}} neu gebootet wird, wird für das primäre Laufwerk "/dev/sda" angezeigt.


## Warum stimmt die CPU-Geschwindigkeit nicht?
{: faq}

Wenn Sie sich bei einem Server anmelden, um die CPU-Informationen zu prüfen, stellen Sie fest, dass die Geschwindigkeit der Prozessoren falsch war. Diese Abweichung kann an Enhanced Intel SpeedStep Technology (EIST) liegen. EIST ist der Intel-Name für die Technologie der dynamischen Skalierungstechnologie.  Diese Technologie heißt auch *CPU-Drosselung* oder in älteren Systemen *Bus Slewing*.  Einige AMD-Systeme verfügen über ähnliche Technologien, die als *Cool'N'Quiet* oder *PowerNow!* bezeichnet werden.  Obwohl diese Technologien nicht gleich sind, verfolgen sie dasselbe Ziel: die Reduzierung des Stromverbrauchs und der Wärmeentwicklung, wenn der Prozessor nicht stark beansprucht ist, indem die CPU-Geschwindigkeit verlangsamt wird.  Wenn der Server wieder eine Last verarbeitet, wird die Taktgeschwindigkeit wieder erhöht.

Wenn Sie wissen möchten, ob der Intel-Prozessor Ihres Servers SpeedStep unterstützt, führen Sie im Kundenportal die folgende Prozedur aus:
1. Klicken Sie auf **Einheiten**.
* Ermitteln Sie Ihren Server in der Liste.
* Klicken Sie auf den Servernamen, um **Einheitendetails** anzuzeigen.
* Suchen Sie den Teilbereich mit dem Namen **Hardware**, um die Modellnummer Ihres Serverprozessors für die CPU-Geschwindigkeit zu suchen.
* Notieren Sie sich die Modellnummer des Serverprozessors. Gehen Sie zum [Intel Processor Finder ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://processorfinder.intel.com/){: new_window} und suchen Sie mit dieser Nummer nach weiteren Informationen zum Prozessor und zur Angabe, ob Enhanced Intel SpeedStep Technology (EIST) unterstützt wird. 

EIST ist eine bewährte Technologie. Es ist nicht üblich, dass Sie EIST inaktivieren müssen. Wenn Sie jedoch entscheiden, dass Sie diese Funktion nicht nutzen möchten, öffnen Sie ein Ticket beim Support-Team, um die Funktion inaktivieren zu lassen.  Um diese Funktion zu inaktivieren, wird der Server neu gestartet.


## Wie gehe ich vor, wenn die Firmware meines Bare-Metal-Servers veraltet ist?
{: faq}

Es ist wichtig, die Firmware aktuell zu halten, um eine optimale Einheitenkompatibilität und Stabilität für Ihren Bare-Metal-Server zu gewährleisten. Wenn eine {{site.data.keyword.baremetal_short}}-Firmwareversion veraltet ist, kann die Firmware kann aktualisiert werden, indem Sie den Bare-Metal-Server in der Einheitenliste auswählen und dann im Aktionsmenü **Firmware aktualisieren** auswählen.

Sie können ein Firmware-Update während des [erneuten Ladens des Betriebssystems](/docs/infrastructure/software?topic=software-reloading-the-os) im [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/){: new_window} initiieren.

## Was geschieht mit Laufwerken in Bare-Metal-Servern, wenn ein Kunde sie nicht mehr benötigt?
{: faq}

Nach der Stornierung wird ein Server automatisch in ein VLAN für Zurückforderung verschoben, wo er eine bestimmte Zeit lang verbleibt. Nach dieser Zeit beginnen die Zurückforderungsprozesse und das Laufwerk wird mit DOD 5220.22-M-Algorithmen bereinigt.  Die Zurückforderung wird mithilfe der Seriennummer des Laufwerks verfolgt. Nach der Fertigstellung wird der Server für die erneute Zuordnung in die Bereitstellung verschoben. Bei einer Laufwerkstörung erfolgt ein manueller Eingriff und die Laufwerke erreichen das Ende des Lebenszyklus.

Der Prozess für das Ende des Lebenszyklus wird eingeleitet, wenn eine Störung vorliegt oder wenn das Alter oder die Größe nicht mehr unterstützt wird. Wenn eine dieser Bedingungen erfüllt ist, werden die Laufwerke wie oben beschrieben bereinigt. Nach der Beendigung des Bereinigungsprozesses wird das Laufwerk durch Zerbrechen, Zerkleinern oder Shreddern physisch vernichtet.  Der Prozess der physischen Vernichtung wird mithilfe der Seriennummer des Laufwerks verfolgt.

## Kann ich sehen, welche Bare-Metal-Server zum Kauf verfügbar sind?
{: faq}

Ja! Sie können jetzt sehen, welche Server in welchem Rechenzentrum verfügbar sind, wenn Sie einen Bare-Metal-Server bereitstellen. Diese Option ist jedoch nur für das Angebot auf Stundenbasis verfügbar. Bei dem Angebot auf Monatsbasis können Sie die Serververfügbarkeit nicht sehen. Weitere Informationen zur Bereitstellung eines Bare-Metal-Servers finden Sie unter [Server mit schneller Bereitstellung auswählen](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers#bm-select-popular-servers).

## Was ist im Lieferumfang meines reservierten Bare-Metal-Servers enthalten?
{: faq}

CPU, RAM, Plattenlaufwerk und RAID sind in der Reservierung für die vertraglich vereinbarte Laufzeit enthalten. Wenn Sie eine größere Netzbandbreite, mehr Speicherkapazität, Betriebssystemsoftware und Software anderer Anbieter benötigen, werden diese Add-ons monatlich berechnet.

## Was geschieht am Ende der Laufzeit meines Vertrags für einen reservierten Bare-Metal-Server?
{: faq}

Ihr Cloud-Service wird über eine monatliche Servicelaufzeit mit den Gebühren fortgesetzt, die beim Ablauf Ihres Vertrags gültig sind.
