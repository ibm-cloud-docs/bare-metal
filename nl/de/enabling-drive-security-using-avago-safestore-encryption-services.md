---
copyright:
  years: 2014, 2018
lastupdated: "2019-04-22"

subcollection: bare-metal

keywords: Avago SafeStore, encryption
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Laufwerksicherheit mit Avago SafeStore Encryption Services aktivieren
{: #enabling-drive-security-by-using-avago-safestore-encryption-services}

Die Einrichtung der Laufwerksicherheit ermöglicht es Ihnen, den Zugriff auf Daten, die auf entfernten Platten gespeichert sind, ohne einen Sicherheitsschlüssel zu verhindern. Ohne diesen Schlüssel können die auf dem Laufwerk gespeicherten Daten nicht wiederhergestellt werden. {{site.data.keyword.BluSoftlayer_full}} stellt in ausgewählten Rechenzentren SEDs (Self-Encrypting Drives) für die Laufwerke zur Verfügung, die für Bare Metal Server erworben werden können. In den Rechenzentren in den USA werden SATA-Laufwerke mit einer Kapazität von 10 TB angeboten.

## Voraussetzungen
{: #prerequisites-enabling-drive-security-by-using-avago-safestore-encryption-services}

* Bare-Metal-Server mit SED-Laufwerken – 10 TB SATA
* LSI/AVAGO MegaRAID SAS 9361-8i oder vergleichbare LSI/AVAGO RAID-Karten
* Installierte Software für Mega RAID Storage Manager

## Laufwerksicherheit mit MegaRAID Storage Manager (MSM) aktivieren
{: #enabling-drive-security-by-using-megaraid-storage-manager-msm-}

Sie können den Sicherheitsschlüssel und die Sicherheitsdaten mithilfe von MegaRAID Storage Manager auf einer entfernten Platte festlegen. Sie können auch die WebBIOS-Schnittstelle verwenden, die beim Serverstart einen Sicherheitsschlüssel erfordert, um auf das BIOS der MegaRAID-Karte zuzugreifen, um die Sicherheitseinstellung für das Laufwerk zu konfigurieren. Weitere Informationen zu MegaRAID Controller Card SAS 9361-8i finden Sie auf der Broadcom-Site, [MegaRAID SAS 9361-8i ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#documentation).

### Vorinstallierte SED-Laufwerke indetifizieren
{: #identifying-preinstalled-sed-drives}

MegaRAID Storage Manager ist unter den meisten unterstützten Betriebssystemen vorinstalliert. Falls nicht vorhanden, können Sie es manuell von der Broadcom-Site installieren. Weitere Informationen finden Sie unter [MegaRAID SAS 9361-8i-Downloads](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#downloads).

Sie können MegaRAID Storage Manager mit den Systemberechtigungsnachweisen öffnen. Im Beispiel wird eine Windows-Umgebung verwendet und MSM ist vorinstalliert.

Wenn Sie MSM müssen Sie den **Benutzernamen** und das **Kennwort** des privilegierten Benutzers (Administrator) angeben.

Klicken Sie auf die Registerkarte **Physisch** und dann auf die Laufwerke, die im System verfügbar sind. Das Teilfenster **Eigenschaften** enthält den Abschnitt mit den
**Eigenschaften für die Laufwerksicherheit**, der das Feld für die **Unterstützung der vollständigen Plattenverschlüsselung** enthält, das auf **Ja** gesetzt ist. Im verwendeten Beispiel werden zwei Nicht-SED-Platten und vier SED-Platten verwendet.

### Laufwerksicherheit im Controller aktivieren
{: #enabling-drive-security-at-the-controller}

1. Zum Aktivieren der Laufwerksicherheit klicken Sie mit der rechten Maustaste auf der Registerkarte **Physisch** auf **Controller 0 :AVAGO MegaRAID SAS 9361-8i** und wählen Sie **Laufwerksicherheit aktivieren** aus.
  * Sie können jetzt die **Sicherheitsschlüssel-ID** und den **Sicherheitsschlüssel** eingeben. Wenn Sie über mehrere Sicherheitsschlüssel verfügen, kann eine Sicherheitsschlüssel-ID hilfreich sein, um den benötigten Sicherheitsschlüssel zu identifizieren. Sie müssen den Sicherheitsschlüssel an einem sicheren Ort notieren. Der Sicherheitsschlüssel ist erforderlich, wenn Sie Laufwerke neu konfigurieren, wie z. B. beim Entfernen oder Wiedereinbau eines Laufwerks. Ohne den Sicherheitsschlüssel ist es nicht möglich, Daten abzurufen, die auf einem Datenträger gespeichert sind, der auf der Basis der SEDs erstellt wurde. Ein verlorener Sicherheitsschlüssel kann nicht mehr abgerufen werden. Es kann auch ein Kennwort zur Startzeit festgelegt werden. Das System wird dann angehalten, bis das festgelegte Kennwort eingegebn wird. Das Kennwort zur Startzeit ist optional. Wenn es allerdings festgelegt ist, müssen Sie sich bei jedem Neustart des Systems bei IPMI anmelden und das Startkennwort eingeben. Blättern Sie nach unten und aktivieren Sie das Kontrollkästchen **Ich habe die Sicherheitseinstellungen für zukünftige Bedarfsfälle aufgezeichnet** und klicken Sie auf **Ja**, um die Laufwerksicherheit zu aktivieren.
  * Wenn die Laufwerksicherheit aktiviert ist, wird ein gelbes Schlüsselsymbol für **Controller 0 AVAGO MegaRAID SAS 9361-8i** angezeigt.
2. Erstellen Sie jetzt mithilfe der SEDs einen sicheren Datenträger. Klicken Sie mit der rechten Maustaste auf der Registerkarte **Logisch** auf **Controller0** und wählen Sie Folgendes aus:  
**Virtuelles Laufwerk erstellen**.
3. Wählen Sie die Option **Erweitert** aus. In der Anzeige muss die **RAID-Stufe** und **Vollständige Plattenverschlüsselung (FDE)** als
**Methode für die Laufwerksicherheit** angegeben werden. Wählen Sie die erforderlichen FDE-Laufwerke aus und klicken Sie auf **Hinzufügen** > **Laufwerkgruppe erstellen** > **Weiter**.
4. Überprüfen Sie die Einstellungen des virtuellen Laufwerks und nehmen Sie erforderliche Änderungen vor. Die vorgeschlagene Einstellung für die **Leserichtlinie** ist **Immer vorauslesen**. Die vorgeschlagene Einstellung für die **Schreibrichtlinie** ist **Zurückschreiben**. Klicken Sie auf **Virtuelles Laufwerk erstellen**. Akzeptieren Sie die Auswirkungen der Richtlinie zum Zurückschreiben aufgrund von BBU, indem Sie auf **Ja** klicken. Klicken Sie auf **Weiter** und überprüfen Sie die Zusammenfassungsanzeige. Klicken Sie auf **Fertigstellen**.
5. Um zu bestätigen, dass die virtuelle Platte gesichert wurde, klicken Sie auf die Registerkarte **Logisch** und das erstellte virtuelle Laufwerk. In den **Eigenschaften der Laufwerksicherheit** sehen Sie, dass das Feld **Gesichert** mit **Ja** markiert ist.

Wenn der Server bereits mit RAID-Datenträgern geliefert wurde, die mithilfe von SED-Laufwerken erstellt wurden, können Sie den Datenträger sichern, indem Sie die folgenden Schritte ausführen.

Klicken Sie auf der Registerkarte **Logisch** mit der rechten Maustaste auf **Laufwerkgruppe** und wählen Sie **Mit FDE sichern** aus. Wenn Sie für einen Datenträger FDE- und Nicht-FDE-Laufwerke gemischt verwendet haben, ist diese Option nicht sichtbar.


Wenn Sie die Laufwerksicherheit entfernen wollen, müssen Sie zuerst die gesicherten virtuellen Platten löschen und mit der rechten Maustaste auf Controller 0 klicken und **Laufwerksicherheit inaktivieren** auswählen. Mit dieser Funktion werden die gespeicherten Daten auf sichere Weise gelöscht und die Laufwerksicherheit wird entfernt.

Sie können die Laufwerksicherheit auch mithilfe von webBIOS und durch Anmeldung über die IPMI zur Startzeit einrichten und auf das RAID-BIOS zugreifen. <!--For more information, see **Avago SafeStore Encryption Services** in the **12 Gb/s MegaRAID SAS Software User Guide**.-->
