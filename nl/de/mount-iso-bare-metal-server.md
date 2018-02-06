---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Ein ISO-Image an einen Bare-Metal-Server anhängen

## Übersicht

Obwohl die meisten {{site.data.keyword.Bluemix_notm}}-Kunden eines der Standard-Betriebssysteme verwenden, die mit unseren Servern ausgeliefert werden, können Sie angepasste ISO-Images (Plattenimages) an die Server anhängen. Es gibt drei Optionen, angepasste ISO-Images anzuhängen.

Damit die beschriebenen Methoden funktionieren, müssen Sie eine Verbindung zu einem privaten Netz über den SL-VPN-Service (beispielsweise https://vpn.ams01.softlayer.com/) oder über einen anderen Server herstellen, der mit dem Netz bereits verbunden ist.

## Option 1 (bevorzugt): Über IPMI (ISO-Image auf einer CIFS-Freigabe)

Wenn unter {{site.data.keyword.Bluemix_notm}} bereits eine Infrastruktur bereitgestellt wird, können Sie einen bestehenden Server für eine CIFS-Freigabe im internen Netz konfigurieren. Dann kann in diesem Netz ein ISO-Image an einen Bare-Metal-Server angehängt werden.

Dies ist die bevorzugte Methode, ein angepasstes Betriebssystem auf einem Bare-Metal-Server zu installieren, weil es über ein lokales Netz installiert wird. Dies ist die schnellste Methode und das ISO-Image bleibt angehängt, selbst wenn Sie sich abmelden oder von der Managementschnittstelle getrennt werden.

Führen Sie diese Schritte aus, um ein angepasstes Betriebssystem von einer CIFS-Freigabe zu installieren:

1. Stellen Sie sicher, dass Sie das ISO-Image auf der CIFS-Freigabe platziert haben.
* Melden Sie sich bei der IPMI-Managementkonsole an, indem Sie in Ihrem Web-Browser die in "control.softlayer.com" und unter "Einheiten -> Ihr Server (Einheitendetails) -> Fernverwaltung" angegebene IP-Adresse aufrufen. Benutzername und Kennwort sind dort auch angegeben.
* Bewegen Sie den Mauszeiger über **Virtueller Datenträger** und klicken Sie auf **CD-ROM-Image**
* Geben Sie weitere Details an und klicken Sie auf **Speichern und anhängen**.
* Nicht alle Benutzer haben eine Berechtigung für das Server-BIOS. Sie können ggf. ein Ticket öffnen, um Support anzufordern:
  * Rootbenutzer-Administratorberechtigung für IPMI (um den Virtual Media Attach-Modus ändern zu können)
  * Ändern Sie die Bootsequenz als erste Bootoption auf "Virtuelles IPMI-Laufwerk".
* Wenn Sie diese Änderungen vorgenommen haben, gehen Sie zur IPMI-Managementkonsole zurück und gehen Sie zu "Konfiguration -> Ferne Sitzung". Ändern Sie den Attach-Modus auf **Anhängen**. In einigen älteren IPMI-Konsolen können Sie diese Option überspringen.
* Starten Sie den Server neu und booten Sie über den virtuellen Datenträger.


## Option 2: Über IPMIView (ISO-Image auf einer CIFS-Freigabe)

Voraussetzungen:<br/>
* Sie haben ein bootbares ISO-Image.
* Windows-CIFS-Server oder NAS-Speicher zum Speichern des bootbaren ISO-Images.
* ISO-Image wird auf den Dateispeicher (NAS) hochgeladen, der mit dem Server verbunden ist.
* IPMIView wird installiert oder es wird auf die KVM-Konsole zugegriffen. <!--  * http://knowledgelayer.softlayer.com/procedure/download-ipmiview
* http://knowledgelayer.softlayer.com/procedure/access-kvm-console -->
* ISO-Datei ist über "wget" für den Download verfügbar.
* Sie haben SSH-Zugriff mit der Berechtigung zum Zugreifen/Installieren von Paketen und zum Erstellen eines Mounts.


### Linux und Windows
Führen Sie die folgenden Schritte aus, um mit IPMIView ein ISO-Image anzuhängen.
1. Fordern Sie mit einem Support-Ticket an, dass Ihr Server die virtuelle CD-ROM als erste Einheit bootet. Jede Einheit muss über ihre zugehörige CD-ROM gebootet werden. Sie können diese Einstellung zurücksetzen, wenn Sie das Betriebssystem installiert haben. 
* Richten Sie eine VPN-Verbindung zum [VPN](http://www.softlayer.com/VPN-Access) ein. Wenn Sie den Microsoft Internet Explorer verwenden, stellen Sie sicher, dass ".softlayer.com" in der Liste vertrauenswürdiger Sites enthalten und JAVA aktuell ist.
* Kopieren Sie den ISO-Datenträger zum NAS oder Windows-CIFS-Server.
  * Stellen Sie eine Verbindung zur Linux Jumpbox mit SSH her.
  * Hängen Sie die NAS-Freigabe an die Linux Jumpbox an:

        mkdir /mnt/nasmount
        mount -t cifs //NAS_SERVER_NAME_ORIP/SLN#####-2 -o username=SLN#####-2,
        password=NAS_STORAGE_PW,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755 /mnt/nasmount
  * Parameterschlüssel des Mountbefehls:
        NAS_SERVER_NAME_ORIP = Name oder IP des NAS-Speichers.
        /SLN#####-2 = Benutzer- und Ordnername, die mit Ihrem NAS-Speicher verbunden werden.
        NAS_STORAGE_PW = Kennwort Ihres NAS-Speichers.
        /mnt/nasmount = Ordner, um den NAS-Speicher anzuhängen.
  * Ändern Sie das Verzeichnis zu Ihrem neuen NAS-Mount-Ordner.
        cd /mnt/nasmount
  * Laden Sie mit "wget" die ISO-Datei herunter.
        wget http://www.linktoyouriso.com/isofilename.iso
  Es wird eine Bestätigung angezeigt, dass der Download erfolgreich war.
* Laden Sie IPMIview hier herunter:
      http://knowledgelayer.softlayer.com/procedure/download-ipmiview
* Stellen Sie über die Management-IP eine Verbindung zum Server her.
      http://knowledgelayer.softlayer.com/procedure/log-ipmiview
      http://knowledgelayer.softlayer.com/procedure/view-ipmi-credentials
* Öffnen Sie die Registerkarte für den virtuellen Datenträger.
* Vervollständigen Sie die Verbindungsdetails für das CD-ROM-Image.
  *
    * Share host = Die IP-Adresse des NAS-Speichers. Sie können diesen Wert finden, indem Sie den Namen Ihres NAS-Speicherservers pingen. Beispiel: 
    ```
    ping nas501.service.softlayer.com
    ```
    * Share Name = Der Benutzername des NAS-Speichers.
    * Path to image = Der Name der ISO-Datei in diesem Format:
          \NASusername\isoname.iso (wie \SLN123456\centos6.iso)
    * User = Der Benutzername des NAS-Speichers.
    * Password = Das Kennwort des NAS-Speichers.
* Starten Sie den Server neu.
* Öffnen Sie die KVM-Konsolenansicht.
* Folgen Sie den Eingabeaufforderungen, um das BOOTBARE ISO-IMAGE zu booten.
* Installieren Sie das Betriebssystem.
* Hängen Sie den virtuellen Datenträger ab.
* Starten Sie den Server neu.

## Option 3: ISO-Image über den lokalen Computer anhängen
<a name="option3"></a>

Sie können ein ISO-Image über Ihren lokalen Computer mithilfe des Java iKVM Viewer (Konsole) anhängen. Dies ermöglicht das Anhängen eines ISO-Images während einer Verbindung zur Konsole. Die Geschwindigkeit des Installationsprozesses kann von der Uploadgeschwindigkeit und der Latenz Ihrer Internetverbindung sowie der Leistung von Java und des Computers abhängen.

Wenn Sie keine Berechtigung haben, das BIOS eines Servers zu ändern, öffnen Sie ein Ticket, um Support für folgende Änderungen anzufordern:
* Rootbenutzer-Administratorberechtigung für IPMI (um den Virtual Media Attach-Modus ändern zu können).
* Änderung der Bootsequenz als erste Bootoption auf "IPMI Virtual Disk".(Da das ISO-Image noch nicht angehängt wird, sollte der Support erst nur für die Änderung der Booteinheit-Priorität angefordert werden.)


1. Melden Sie sich bei der IPMI-Managementkonsole an, indem Sie in Ihrem Web-Browser die in "control.softlayer.com" angegebene IP-Adresse aufrufen.
* Klicken Sie auf "Einheiten > Ihr Server (Einheitendetails) > Fernverwaltung". Geben Sie den Benutzernamen und das Kennwort an.
* Klicken Sie auf "Konfiguration > Ferne Sitzung" und ändern Sie den Attach-Modus zu **Anhängen**. In einigen älteren IPMI-Konsolen ist diese Option nicht verfügbar und Sie diesen Schritt überspringen.
* Klicken Sie auf "System > Systeminformationen", um auf die Seite mit den Systeminformationen zurückzukehren. Es wird ein Symbol für das Konsolenfenster angezeigt. 
* Klicken Sie auf das Konsolensymbol, um die Konsole zu öffnen. Akzeptieren Sie alle Sicherheitswarnungen.
* Wenn die Konsole verbunden ist, wird ein Anmeldedialog angezeigt.
* Klicken Sie auf "Virtueller Datenträger > Virtueller Speicher".
* Gehen Sie zur Registerkarte **CDROM&ISO** und wählen Sie unter **Logischer Laufwerktyp** die ISO-Datei aus.
* Klicken Sie auf **Image öffnen** und wählen Sie auf Ihrem lokalen Computer die ISO-Datei aus.
* Klicken Sie auf **Plug-in**, um das ISO-Image in das virtuelle CD-ROM-Laufwerk zu legen.
* Klicken Sie auf **OK**.
* Starten Sie den Server neu und verwenden Sie die Option **Vom virtuellen CD-ROM-Laufwerk booten**. Sie müssen möglicherweise die virtuelle Tastatur im iKVM Viewer nutzen, um eine Booteinheit auszuwählen.

## Fehlerbehebung

* Nicht alle Benutzer haben einen Standardzugriff, um virtuelle Datenträger anzuhängen. Wenn Berechtigungsfehler auftreten, wenden Sie sich an den Support, um die IPMI-Rootbenutzerberechtigung aktualisieren zu lassen.
* Wenn bereits ein ISO-Image angehängt wurde, wird eine Fehlernachricht mit dem Text angezeigt, dass **bereits ein Datenträger angehängt wurde**. Sie müssen den vorhandenen Datenträger abhängen und durch ein neues ISO-Image ersetzen. Es können keine zwei ISO-Images gleichzeitig angehängt werden.
* Sie müssen ggf. Unterstützung anfordern, um die Bootreihenfolge im BIOS zu ändern.
* Wenn Sie ein ISO-Image anhängen, verwenden Sie bitte das SSL-VPN (http://vpn.softlayer.com) anstatt das PPTP-VPN. Sobald eine Verbindung zum VPN-Netzwerk hergestellt wurde, könne Sie über die IPMI-Adresse (https://<private-ip-IPMI-management>) auch auf IMPI des System zugreifen.
* Wenn Sie einen Pfad zu einem ISO-Image eingeben, verwenden Sie für den Pfad die Syntax für UNC-Namen (Universal Naming Convention). Beispiel:
  ```
  \\<NAS username>\<isoname>.iso
  ```
