---

copyright:
  years: 2017, 2019
lastupdated: "2018-07-10"

keywords: raid, adaptec, ipmi, raid bios, raid array, RAID configuration

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Adaptec-RAID-Konfigurationen erstellen und anpassen
{: #bm-create-raid-config}

Mit dem Adaptec-RAID-BIOS können Sie Ihre RAID-Einrichtung konfigurieren und verwalten. Verwenden Sie dieses BIOS, wenn Sie unsere Option [Ohne Betriebssystem](/docs/bare-metal?topic=bare-metal-the-no-os-option) verwenden und eine bestimmte Laufwerkkonfiguration einrichten möchten.

## Auf die IPMI-Einheit für die Interaktion mit dem RAID-BIOS zugreifen
{: #bm-access-ipmi}

Unabhängig davon, ob Ihre Maschine mit einem Adaptec-Controller oder einem LSI-Controller ausgestattet ist, müssen Sie auf den Server zugreifen, der IPMI für die Interaktion mit dem RAID-BIOS verwendet. Um mit IPMI zu interagieren, müssen Sie zunächst eine Verbindung zum Adaptec {{site.data.keyword.cloud}}-VPN herstellen.
1. Melden Sie sich beim VPN entweder über [SSL](/docs/infrastructure/iaas-vpn?topic=VPN-setup-ssl-vpn-connections#setup-ssl-vpn-connections) oder PPTP an.
* Greifen Sie auf die Einheitenliste im [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/){: new_window} zu. Weitere Informationen finden Sie unter [Einheitenliste aufrufen](/docs/infrastructure/vsi?topic=virtual-servers-managing-virtual-servers).
* Klicken Sie auf die Einheit, auf die Sie zugreifen möchten.
* Wählen Sie die Registerkarte "Fernverwaltung" aus, um die IPMI-Zugriffsdetails für Ihren Server zu suchen.
* Geben Sie die IP-Adresse Ihrer IPMI-Einheit in den Browser ein und melden Sie sich an.
* Um mit der fernen Konsole zu interagieren, klicken Sie auf **Fernbedienung > Konsolenumleitung**.

## RAID-Arrays erstellen
{: #bm-create-raid-array}

Drücken Sie während des Startprozesses die Tastenkombination  **Strg+A**, um auf das RAID-BIOS zuzugreifen.

Öffnen Sie "Logische Einheitenkonfiguration" (erste Option), um mit der Konfiguration Ihres RAID zu beginnen. Mit dieser Option wird die Topologie Ihrer Laufwerke geprüft und ein Menü angezeigt, über das Sie Arrays verwalten oder erstellen sowie weitere Verwaltungsaufgaben für Laufwerke ausführen können.

Im folgenden Beispiel wird dargestellt, wie ein Array erstellt wird. Es wird eine Liste mit verfügbaren Laufwerken angezeigt, die beim Erstellen Ihres RAID-Arrays verwendet werden können.

1. Zum Auswählen der Laufwerke drücken Sie die LEERTASTE, um das Feld *Ausgewählte Laufwerke* zu füllen.
* Sobald Sie alle Laufwerke ausgewählt haben, die Sie für Ihr Array verwenden möchten, drücken Sie die LEERTASTE, um den Schritt der RAID-Konfiguration aufzurufen.
* Wählen Sie den RAID-Typ aus, den Sie verwenden möchten. Wenn Sie Unterstützung brauchen, um zu bestimmen, welche RAID-Einrichtung Ihren Anforderungen am besten genügt, finden Sie weitere Informationen unter den folgenden [Häufig gestellten Fragen von Adaptec ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm){: new_window}.
* Stellen Sie während der Konfiguration eine Bezeichnung des Arrays bereit. Es hat sich bewährt, dass die Bezeichnung den RAID-Typ enthält (beispielsweise RAID10-A).
* Drücken Sie die **Eingabetaste**, um die restlichen Einstellungen aufzurufen. Verwenden Sie die Standardwerte.

Wählen Sie nach Abschluss der Konfiguration "Fertig" aus. Das RAID wird erstellt. Das neue Array wird angezeigt, wenn Sie im Hauptmenü "Arrays verwalten" auswählen. Um das Konfigurationsdienstprogramm zu beenden, drücken Sie so lange die ESC-Taste, bis Sie aufgefordert werden, das Adaptec-BIOS zu beenden.

## Vorhandene RAID-Arrays entfernen
{: #bm-remove-raid-array}

Wenn Sie ein vorhandenes Array entfernen müssen, rufen Sie **Arrays verwalten** auf, wählen Sie das zu entfernende Array aus, drücken Sie **Löschen** und bestätigen Sie Ihre Anforderung.

## Beispielkonfigurationen
{: #bm-example-config}

1. Auf einem Server mit insgesamt sechs Laufwerken können Sie zwei SSDs in einer RAID-0-Konfiguration für Ihr Betriebssystem und vier weitere Laufwerke in einer RAID-10-Konfiguration für Ihre Daten einrichten. Mit dieser Konfiguration können Sie das Betriebssystem des Servers schnell erneut laden, ohne dass Sie die Site- oder Servicedaten Ihres Standorts wiederherstellen müssen, wenn diese sich auf dem sekundären Array befinden.

* Sie können in einem cPanel-Server /var und /home auf separaten SSD-RAID-Arrays haben. Da diese Verzeichnisse die beiden E/A-intensivsten Verzeichnisse auf einem cPanel-Server sind, können Sie mit den folgenden Einstellungen potenziell die Antwortzeit der Site verringern:
  * RAID0 (2 SATA-Laufwerke) - /
  * RAID0 (2 SSD-Laufwerke) - /var
  * RAID0 (2 SSD-Laufwerke) - /home
  * RAID10 (4 SATA-Laufwerke) - /backup

* Verwenden Sie ein einzelnes RAID-Array, um mehrere logische Partitionen einzurichten. Verwenden Sie beispielsweise zwei 4-TB-Laufwerke in einer RAID-1-Konfiguration. Sie können das RAID gemäß Ihren Anforderungen partitionieren. Beachten Sie das folgende Beispiel:
  * Primäre Partition mit 100 GB für Ihr Betriebssystem
  * Zweite Partition mit 500 GB für Ihre Daten
  * Dritte Partition mit dem verbliebenen Speicherplatz für Sicherungen
