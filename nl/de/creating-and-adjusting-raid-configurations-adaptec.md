---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Adaptec-RAID-Konfigurationen erstellen und anpassen

Mit dem Adaptec-RAID-Bios können Sie Ihre RAID-Einrichtung konfigurieren und verwalten. Verwenden Sie dieses BIOS, wenn Sie die Option [Ohne Betriebssystem](introduction-no-os.html) nutzen und eine bestimmte Laufwerkkonfiguration einrichten möchten.

## Auf die IPMI-Einheit für die Interaktion mit dem RAID-BIOS zugreifen

Unabhängig davon, ob Ihre Maschine einen Adaptec-Controller oder einen LSI-Controller hat, müssen Sie mit IPMI auf den Server zugreifen, damit eine Interaktion mit dem RAID-BIOS stattfindet. Um mit IPMI zu interagieren, muss zunächst eine Verbindung zum Adaptec {{site.data.keyword.IBM&reg; Cloud}}-VPN hergestellt werden.
1. Melden Sie sich beim VPN entweder über [SSL](/infrastructure/vpn/ssl-vpn-connections.html) oder PPTP an. Weitere Informationen dazu finden Sie auf der [VPN-Themenseite](/infrastructure/vpn/index.html).
* Rufen Sie die Einheitenliste im [Kundenportal](https://control.softlayer.com/) auf. Weitere Informationen finden Sie unter [Einheitenliste aufrufen](/vsi/vsi_managing.html).
* Klicken Sie auf die Einheit, auf die Sie zugreifen möchten.
* Wählen Sie die Registerkarte "Fernverwaltung" aus, um die IPMI-Zugriffsdetails für Ihre Server zu suchen.
* Geben Sie die IP-Adresse Ihrer IPMI-Einheit in den Browser ein und melden Sie sich an.
* Um mit der fernen Konsole zu interagieren, klicken Sie auf "Fernbedienung > Konsolenumleitung".

## RAID-Arrays erstellen

Drücken Sie während des Bootprozesses STRG+A, um das RAID-BIOS aufzurufen.

Um nun Ihr RAID zu konfigurieren, rufen Sie "Logische Einheitenkonfiguration" (erste Option) auf. Dadurch wird die Topologie geprüft und ein Menü angezeigt, in dem Sie Arrays verwalten oder erstellen sowie weitere Verwaltungsaufgaben für Laufwerke abschließen können.

Im folgenden Beispiel wird dargestellt, wie ein Array erstellt wird. Es wird eine Liste mit verfügbaren Laufwerken angezeigt, die beim Erstellen Ihres RAID-Arrays verwendet werden können.

1. Um Laufwerke auszuwählen, drücken Sie die LEERTASTE, um das Kontrollkästchen *Ausgewählte Laufwerke* zu füllen.
* Sobald Sie alle Laufwerke ausgewählt haben, die Sie für Ihr Array verwenden möchten, drücken Sie die LEERTASTE, um den Schritt der RAID-Konfiguration aufzurufen.
* Wählen Sie den gewünschten RAID-Typ aus. Wenn Sie Unterstützung brauchen, um zu bestimmen, welche RAID-Einrichtung Ihren Anforderungen am besten genügt, erhalten Sie Informationen bei den [Häufig gestellten Fragen von Adaptec](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm).
* Stellen Sie während der Konfiguration eine Bezeichnung des Arrays bereit. Es hat sich bewährt, dass die Bezeichnung den RAID-Typ enthält (beispielsweise RAID10-A).
* Drücken Sie die Eingabetaste, um durch die restlichen Einstellungen zu navigieren. Verwenden Sie die Standardwerte.

Wählen Sie nach Abschluss der Konfiguration "Fertig" aus und das RAID wird erstellt. Das neue Array wird angezeigt, wenn Sie im Hauptmenü "Arrays verwalten" auswählen. Um das Konfigurationsdienstprogramm zu beenden, drücken Sie so lange die ESC-Taste, bis Sie aufgefordert werden, das Adaptec-BIOS zu beenden.

## Vorhandene Arrays entfernen

Wenn Sie ein Array entfernen möchten, gehen Sie zu "Arrays verwalten > Array auswählen". Wählen Sie das gewünschte Array aus, drücken Sie "Löschen" und bestätigen Sie.

## Beispielkonfigurationen

1. In einem Server mit insgesamt 6 Laufwerken können Sie 2 SSDs in einem RAID0 für Ihr Betriebssystem und 4 weitere Laufwerke in einem RAID10 für Ihre Ist-Daten einrichten. Damit kann das Betriebssystem des Servers schnell neu geladen werden, ohne dass Ihre Site oder Servicedaten, wenn sie sich auf einem zweiten Array befinden, wiederhergestellt werden müssen.

* Sie können in einem cPanel-Server /var und /home auf separaten SSD-RAID-Arrays haben. Da diese die 2 Ein-/Ausgabe-intensivsten Verzeichnisse auf einem cPanel-Server sind, können Sie die Site-Antwortzeit mit den folgenden Einstellungen verringern:
  * RAID0 (2 SATA-Laufwerke) - /
  * RAID0 (2 SSD-Laufwerke) - /var
  * RAID0 (2 SSD-Laufwerke) - /home
  * RAID10 (4 SATA-Laufwerke) - /backup

* Verwenden Sie ein einzelnes RAID-Array, um mehrere logische Partitionen einzurichten. Verwenden Sie beispielsweise 4-TB-Laufwerke, die in einem RADI1 eingerichtet sind. Sie können das RAID Ihren Bedürfnissen entsprechend partitionieren. Beispiel:
  * Primäre Partition mit 100 GB für Ihr Betriebssystem
  * Sekundäre Sekunde mit 500 GB für Ihre Daten
  * Dritte Partition mit dem verbliebenen Speicherplatz für Ihre Backups
