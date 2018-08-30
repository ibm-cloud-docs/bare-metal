---



copyright:
  years: 2017, 2018
lastupdated: "2018-07-06"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Angepassten Bare-Metal-Server erstellen
{: #ordering-baremetal-server}

Führen Sie die folgenden Schritte aus, um einen angepassten {{site.data.keyword.baremetal_short}} zu erstellen. 

1. Öffnen Sie den [{{site.data.keyword.cloud_notm}}-Katalog](https://console.bluemix.net/catalog/){:target="_blank"}.    
2. Wählen Sie Bare Metal Servers aus. 
3. Klicken Sie auf "Erstellen". 
4. Unterhalb der Serverliste finden Sie den Text **Haben Sie Interesse an weiteren Konfigurationsoptionen? Hier klicken**. Wählen Sie diese Option aus. Das Formular für angepassten Server wird angezeigt. 
1. Wählen Sie den Standort des Rechenzentrums für Ihren Server aus. 
* Wählen Sie einen Server aus den drei Serverkategorien aus, indem Sie auf den Link **Beginnend bei** für den Preis klicken. 
  * Von SAP zertifizierte Server (Weitere Informationen zur Bereitstellung eines von SAP zertifizierten Servers finden Sie unter [Von SAP zertifizierte {{site.data.keyword.cloud_notm}}-Infrastruktur](/docs/bare-metal/bare-metal-sap-applications.html).) 
  * Multi-Core-Server mit Einzelprozessor
  * Multi-Core-Server mit Dualprozessor

* Wählen Sie aus den Konfigurationsoptionen aus. **Rechenzentrum**, **RAM** und **Betriebssystem** sind erforderliche Felder. Alle anderen Felder sind optional. Weitere Informationen zu den optionalen Feldern finden Sie unter **[Weitere Serverkonfigurationsoptionen](#addl-server-options)**. 

    **Hinweis**: Es wird eine Fehlernachricht angezeigt, wenn ein Konflikt zwischen dem Server und dem Betriebssystem besteht. Ein Beispiel ist die Auswahl von Linux auf einem Microsoft SQL Server.
* Klicken Sie auf **Zur Bestellung hinzufügen**. Die Kassenseite wird angezeigt. 

  Von der Kassenseite aus können Sie zur Konfigurationsseite zurückkehren, indem Sie auf eine der Optionen für die Rekonfiguration klicken. 
* Geben Sie im Abschnitt für die erweiterte Systemkonfiguration weitere Konfigurationsoptionen an. Weitere Informationen finden Sie unter **[Erweiterte Systemkonfiguration](#adv-system-config)**. 

*   Klicken Sie auf die Kontrollkästchen für Cloud-Service-Bedingungen**** und für Servicevereinbarungen Dritter****.
*   Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf die Schaltfläche **Bestellung abschicken**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige. Sie ist die Auftragsbestätigung für Ihre Bereitstellungsbestellung.

  Sie können diese Bestellung auch ohne Einkauf speichern, indem Sie auf **Als Angebot speichern** klicken. 

 Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der Fertigstellungsnachricht gelangen Sie direkt zu Ihrer Seite *Einheitendetails*, nachdem Sie sich bei {{site.data.keyword.cloud_notm}} angemeldet haben. Sie können sich auch direkt beim {{site.data.keyword.slportal}} anmelden.

 ## Weitere Serverkonfigurationsoptionen
 {: #addl-server-options}

 Wenn Sie Ihren Bare-Metal-Server bereitstellen, sind weitere Optionen verfügbar, z. B. öffentliche Bandbreite, Uplink-Port-Geschwindigkeiten, öffentliche sekundäre IP-Adressen und mehr. In Tabelle 1 sind die weiteren Optionen beschrieben. 


 | **Feld** | **Beschreibung** |
 |-------------------|---------------|
 |Serversicherheit|Beispielsweise Trusted Execution Technology (Intel TXT)|
 |Software Guard Extensions|Höhere Sicherheit für sensiblen Code und Daten (Intel SGX). <br><br>Siehe [Bare-Metal-Server mit Intel SGX bereitstellen](../bare-metal/bare-metal-provision-SGX.html). |
 |RAM|Wählen Sie die RAM-Größe aus, die Ihre Serveranforderungen erfüllt. |
 |Betriebssystem |Wählen Sie CentOS, FreeBSD, Microsoft, Red Hat, Ubuntu oder "Andere" aus. |
 |Festplatten |Verwenden Sie das Tool in der Benutzerschnittstelle zum Einrichten Ihrer Festplatten, das die Felder auf der Basis Ihrer Auswahl für das Betriebssystem vorab ausfüllt. <br><br> Sie können auch ein Intel Optane SSD-Laufwerk verwenden. Siehe [Intel Optane SSD DC P4800X bereitstellen](../bare-metal/bm-provision_ssd.html).
 |Öffentliche Bandbreite |Bestimmt das Datenvolumen, das in einem Monat über die öffentliche Schnittstelle übertragen werden kann. In Testumgebungen, bei denen Installationsdaten über diese Schnittstelle übertragen werden müssen, müssen die Werte so angepasst werden, dass sie das ursprünglich übertragene Datenvolumen übersteigen. Beachten Sie, dass das [{{site.data.keyword.cloud_notm}} Content Delivery Network](https://www.ibm.com/cloud/cdn) ein anfängliches Datenvolumen an eines der {{site.data.keyword.cloud_notm}}-Rechenzentren sendet. Alle {{site.data.keyword.baremetal_short}} können auf eine uneingeschränkte (unbegrenzte) Bandbreite aktualisiert werden. Alle uneingeschränkten Einheiten sind private, dedizierte Ports.|
 |Uplink-Port-Geschwindigkeiten |Bestimmt die Geschwindigkeit der internen und externen Schnittstellen. |
 |Sekundäre öffentliche IP-Adressen |Weist Ihrem Server weitere IP-Adressen zu. Sie benötigen je nach Szenario möglicherweise weitere IP-Adressen, die Ihrem Server zugewiesen werden. Weitere IPv4-Adressen sind in den Mengen 1, 2, 4, 8, 16 oder 32 verfügbar. |
 |Primäre IPv6-Adressen |Werden den internen sowie externen Schnittstellen Ihres Servers zugewiesen. |
 |Statische öffentliche IPv6-Adressen |Weist weitere IPv6-Adressen aus einem /64-Block zu. |
 |Betriebssystem-Add-ons|Wählen Sie Optionen wie VMware, Sicherungslösungen, Steuerkonsole, Datenbank, Hardware- & Software-Firewalls, Viren- & Spywareschutz, Angriffserkennung & -schutz aus. <br><br>Es wird dringend empfohlen, dass sich die für die Sicherheit verantwortliche Unternehmensabteilung mit dem {{site.data.keyword.cloud_notm}}-Support abstimmt, um die Details dieser Optionen zu besprechen.  |EVault |Ein agentenbasiertes Sicherungstool, das auf Ihrem Server installiert werden kann, um Sicherungen zwischen Servern zu replizieren. |
 |Service-Add-ons|Wählen Sie alle Service-Add-ons aus, wie z. B. Überwachung, automatische Antwort und Versicherung. |
 {: caption="Tabelle 1. Weitere Serveroptionen" caption-side="top"}

## Erweiterte Systemkonfiguration
{: #adv-system-config}

Mit den Feldern unter **Erweiterte Systemkonfiguration** wird der Bereitstellungsprozess abgeschlossen. 

| **Feld** | **Beschreibung** |
|---|---|
| Hostname | Ein permanenter oder temporärer Name für Ihren Server, beispielsweise _server1_. **Hinweis**: Wenn Sie einen von SAP zertifizierten Server bereitstellen, muss der SAP-Hostname aus maximal 13 alphanumerischen Zeichen bestehen. Weitere Informationen zu SAP-Hostnamen finden Sie unter [SAP Notes 611361](https://launchpad.support.sap.com/#/notes/2611361) und [129997](https://launchpad.support.sap.com/#/notes/129997). Erfordert eine SAP-S-Benutzer-ID. |
| Domäne | Name der Unterdomäne, die nicht mit dem Internetdomänennamen identisch sein darf, beispielsweise _test.acme.com_. |
| VLAN-Auswahl | Wenn sich in Ihrem Konto ein VLAN befindet, weil Sie bereits mindestens einen Server bestellt haben, können Sie den neuen Server diesem VLAN hinzufügen. |
| Bereitstellungsscript | Sie können ein Script zur Verfügung stellen, mit dem bestimmte Schritte nach der Bereitstellung automatisiert werden. |
| SSH-Schlüssel | Sie können den öffentlichen Schlüssel Ihres SSH-Schlüssels bereitstellen, mit dem Sie sich bei Ihrem Server anmelden können, nachdem er bereitgestellt wurde. |
{: caption="Tabelle 2. Erweiterte Systemkonfiguration" caption-side="top"}

 Wenn Sie weitere Informationen wünschen, wenden Sie sich an den {{site.data.keyword.cloud_notm}}-Support. 

 **HINWEIS:** Sie können sekundäre Teilnetze mit Ihren Recheneinheiten bestellen. Wenn Sie sekundäre Teilnetze bestellen, werden sie jedoch zurückgefordert, wenn die Recheneinheit zurückgefordert wird. Wenn Sie das sekundäre Teilnetz separat bestellen (d. h. nicht als Add-on-Option einer Recheneinheit), können Sie das Teilnetz behalten, bis Sie es explizit stornieren. Diese Unterscheidung ist wichtig, damit Sie nicht versehentlich einige IP-Adressen verlieren, wenn eine Recheneinheit zurückgefordert wird. 

## Nächste Schritte
Nachdem Ihr {{site.data.keyword.baremetal_short}} bereitgestellt ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [{{site.data.keyword.baremetal_short}} verwalten](../bare-metal/managing.html).
