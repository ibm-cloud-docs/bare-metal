---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Ubuntu-Server auf einem Bare-Metal-Server installieren

Wenn Sie ein Betriebssystem verwenden möchten, das nicht von der {{site.data.keyword.IBM&reg; Cloud}} bereitgestellt wird, können Sie die Installation auf Bare-Metal-Servern durchführen, indem Sie angepasste custom ISO-Images (Plattenimages) anhängen. Um ein ISO-Image anzuhängen, wird es auf den Dateispeicher (NAS) hochgeladen, der mit dem Server verbunden ist. Um ein ISO-Image auf ein NAS hochzuladen, hängen Sie das ISO-Image mit IPMI mit der folgenden Vorgehensweise an.
1. Bestellen Sie den Bare-Metal-Server mit der Option **Ohne Betriebssystem**. 
* Sie können auch das freie Betriebssystem (z. B. CentOS) auswählen, das für die Verbindung zum NAS verwendet werden kann.
* Bestellen Sie den NAS-Speicher, um das bootbare ISO-Image zu speichern. Wenn Sie bereits einen Windows-CIFS-Server haben, können Sie ihn für die Freigabe des ISO-Images nutzen. Mit diesem Windows-CIFS-Server erhalten Sie ein traditionelles NAS mit einer Kapazität von 20 GB. Nach der NAS-Bereitstellung wird eine Beschreibung Ihres NAS-Speichers im Kundenportal angezeigt.
* Laden Sie das ISO-Image von "https://www.ubuntu.com/download/server" herunter.
* Laden Sie das ISO-Image auf das NAS oder auf den Windows-CIFS-Server hoch. Sie können das ISO-Image mit FTP auf den NAS-Speicher hochladen.

  Beispielhafte FTP-Prozedur:
  ```
  #ftp <nas address>.service.softlayer.com
  Connected to <nas address>.service.softlayer.com
  220 NAS FTP Service
  User (<nas address>.service.softlayer.com:(none)): <nas username>
  331 Please specify the password.
  Password: <nas password>
  230 Login successful.
  ftp> bin
  200 Switching to Binary mode
  ftp> put <iso imagefile name>.iso
  200 PORT command successful. Consider using PASV.
  150 Ok to send data.
  226 Transfer complete.
  ftp: 3170893824 bytes sent in 253.86 Seconds 12490.77Kbytes/sec.
  ```
  
* Richten Sie eine VPN-Verbindung zu {{site.data.keyword.Bluemix_notm}} mit IPMI ein. Sie können das VPN-Menü über das Support-Menü oder der folgenden URL starten: [VPN-Zugriff](http://www.softlayer.com/VPN-Access)
* Hängen Sie das ISO-Image über das Menü des virtuellen IPMI-Datenträgers an, indem Sie "Mit IPMI über Management-IP verbinden" verwenden.
  1. Zeigen Sie die IPMI-Berechtigungsnachweise an.
  * Protokollieren Sie die IPMI-Ansicht.
  * Öffnen Sie die Registerkarte für den virtuellen Datenträger.
  * Sie benötigen einen Rootbenutzer mit Administratorberechtigungen für IPMI. Wenn die Berechtigungen *Operator* anzeigen, öffnen Sie ein Support-Ticket, um die Berechtigungen zu Administrator zu ändern.
  * Füllen Sie die Verbindungsdetails für das ISO-Image aus.
    Share host = IP-Adresse des NAS<br/Beispiel: 10.3.x.x
    Path to image = Name der ISO-Datei in diesem Format: \NASusername\imagefilesname.iso (i.e. \SLNxxxxxx\SLE-12-SP1-Server-DVD-x86_64-GM-DVD1.iso)
    User = Benutzername des NAS
    Password = Kennwort des NAS
  * Klicken Sie auf die Schaltfläche **Anhängen**.
  * Betätigen Sie die Einheit.
* Klicken Sie auf den KVM Viewer und starten Sie ihn. Öffnen Sie die Seite "Virtueller Speicher" im Menü "Virtueller Datenträger". Wenn das Anhängen Ihres ISO-Images als CD-ROM-Einheit erfolgreich war, wird eine Einheitenbeschreibung im **Verlauf des Verbindungsstatus** angezeigt.
* Fordern Sie mit einem SoftLayer-Ticket an, dass Ihr Server die virtuelle CD-ROM als erste Einheit bootet. Führen Sie diese Anforderung für jeden Server durch. Ändern Sie die Booteinstellung erst nach der Installation des Betriebssystems.
  **Hinweis**: Sie müssen ggf. Unterstützung anfordern, um die Bootreihenfolge im BIOS zu ändern. Dies hängt von Ihrem Server ab. Führen Sie einen Neustart durch, um die Bootreihenfolge zu bestätigen.
* Starten Sie den Server vom KVM Viewer.
* Installieren Sie das Betriebssystem vom angehängten ISO-Image.
* Installieren Sie das Ubuntu-Betriebssystem auf den Bare-Metal-Server vom ISO-Image.
* Konfigurieren Sie die Netzeinstellungen (IP-Adresse/Teilnetz/Gateway/DNS usw.). Bei einer fehlerhaften Konfiguration während der Installation können Sie nur eine Verbindung zu diesem Server über die KVM-Konsole nach dem Neustart herstellen.

* Hängen Sie den virtuellen Datenträger ab. Sie sollten den virtuellen Datenträger über die Registerkarte "Virtueller IPMI-Datenträger" vom Server abhängen.
* Starten Sie den Server neu.
* Nach dem Neustart können Sie über SSH auf den Server zugreifen.
