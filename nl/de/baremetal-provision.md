---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: custom server, {{site.data.keyword.baremetal_short}}, {{site.data.keyword.Bluemix_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# Angepassten Bare-Metal-Server erstellen
{: #ordering-baremetal-server}

Führen Sie die folgenden Schritte aus, um einen angepassten {{site.data.keyword.baremetal_long}} zu erstellen.

## Bereitstellung über den {{site.data.keyword.cloud_notm}}-Katalog
{: #provision-through-the-catalog}

Führen Sie die folgenden Schritte aus, um Ihren {{site.data.keyword.baremetal_short}} über {{site.data.keyword.cloud_notm}} bereitzustellen.

1. Öffnen Sie den [{{site.data.keyword.cloud_notm}}-Katalog](https://cloud.ibm.com/catalog/){: external}.   
2. Wählen Sie {{site.data.keyword.baremetal_short}} unter **Datenverarbeitung** aus.
3. Klicken Sie auf 'Weiter'. Wenn Sie keine Schaltfläche 'Weiter' sehen, müssen Sie sich möglicherweise anmelden. 
4. Geben Sie die **Menge** **identischer** Server ein, die bereitgestellt werden sollen. Der Standardwert ist 1. Wenn Sie mehrere Server mit _unterschiedlichen_ Spezifikationen bereitstellen möchten, müssen Sie die Server separat bereitstellen.
5. **Hostname** ist ein permanenter oder temporärer Name für Ihren Server, beispielsweise 'baremetal01'. Klicken Sie auf **Informationen**, um Formatierungsspezifikationen anzuzeigen.
6. **Domäne** ist die Identifikationszeichenfolge zum Definieren der administrativen Steuerung im Internet, beispielsweise 'Customer-123456.cloud'. Klicken Sie auf **Informationen**, um Formatierungsspezifikationen anzuzeigen.
7. **Abrechnung** ist entweder **Stündlich** oder **Monatlich**.
8. Wählen Sie den **Standort**, die Region und das Rechenzentrum für den Standort Ihres Servers aus.
9. Klicken Sie auf **Alle Server**, um eine Liste der Prozessoren (Einzelprozessor, Dualprozessor und Quad-Prozessor) und der zertifizierten Server (SAP und VMware) anzuzeigen. Wählen Sie den Server aus, der am besten Ihrer Workload entspricht.
10. Wählen Sie Ihren **RAM** aus. Für einige Server basieren die RAM-Standardwerte auf dem CPU-Modell und können nicht geändert werden. 

Für SAP-zertifizierte Server basieren die Standardwerte für RAM und Betriebssystem auf Ihrer Serverauswahl. Der Standardwert für die Option für Ihren lokalen Speicher basiert auch auf Ihrer Serverauswahl.
{ :note}

11. Geben Sie einen optionalen öffentlichen Schlüssel für Ihren **SSH-Schlüssel** ein, den Sie verwenden können, um sich bei Ihrem Server anzumelden, nachdem er bereitgestellt wurde.
12. Wählen Sie ein **Image** (Betriebssystem) für Ihren Server aus. Ihre Optionen basieren auf dem ausgewählten Server.
13. Erweitern Sie **Add-ons**, um Optionen zur Konfiguration des Servers auszuwählen.
14. Die **Speicherplatten** sind auf der Basis Ihrer Serverauswahl vorkonfiguriert. Erweitern Sie **Add-ons**, um Dateispeicher oder Blockdatenträger hinzuzufügen, nachdem Ihre {{site.data.keyword.baremetal_short}} bereitgestellt wurden. 
15. Wählen Sie unter **Netzschnittstelle** die Optionen für 'Uplink-Port-Geschwindigkeiten' und 'Privates VLAN' aus. Erweitern Sie **Add-ons**, um die entsprechenden Optionen auszuwählen, oder verwenden Sie die Standardwerte.
16. Überprüfen Sie Ihre Bestellung in der Bestellübersicht.
17. Geben Sie alle vorhandenen Werbeaktionscodes unter **Werbeaktionscode anwenden** ein.
18. Klicken Sie auf die Servicevereinbarungen anderer Anbieter, um die vorhandenen Vereinbarungen zu lesen.
19. Klicken Sie auf **Erstellen**, um Ihren Server bereitzustellen. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt, die Sie drucken können, da sie auch Ihr Beleg ist.

Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung.

Die Fertigstellungsnachricht enthält einen Link zu Ihrer Seite *Einheitendetails*, sodass Sie sich bei {{site.data.keyword.cloud_notm}} anmelden können. Sie können sich auch direkt beim {{site.data.keyword.slportal}} anmelden.

Sie haben auch die Option, die Bestellung als Angebot zu speichern oder einer Schätzung hinzufügen. Wenn Sie ein Angebot speichern, wird ein Link an die E-Mail-Adresse gesendet, die Ihrem Konto zugeordnet ist. Öffnen Sie den Link, um die gespeicherten Angebotsinformationen anzuzeigen. Eine weitere Option besteht darin, 'Verwalten' > 'Abrechnung und Nutzung' aufzurufen und 'Vertrieb' > 'Geräteangebote' auszuwählen. Wenn Sie Zugriff haben, können Sie das Angebot kaufen, indem Sie auf das Angebot klicken und die Bestellung bestätigen. Durch Hinzufügen zur Schätzung werden die vorgeschlagenen Kosten der Konfiguration in den Preisrechner platziert. Klicken Sie auf **Informationen**, um weitere Details zum Preisrechner anzuzeigen.

## Bereitstellung über das Kundenportal
Führen Sie die folgenden Schritte aus, um Ihren {{site.data.keyword.baremetal_short}} über {{site.data.keyword.slportal}} bereitzustellen.

1. Melden Sie sich mit Ihren eindeutigen Berechtigungsnachweisen beim [{{site.data.keyword.slportal}}](control.softlayer.com){: external} an.
2. Rufen Sie **Konto** > **Bestellung aufgeben** auf.
3. Wählen Sie **Stündlich** oder **Monatlich** aus.
3. Wählen Sie in der Liste das Rechenzentrum aus, in dem sich Ihr {{site.data.keyword.baremetal_short}} befinden soll, und wählen Sie dann Ihren zertifizierten Server (SAP oder VMware) oder Prozessor (Einzelprozessor, Dualprozessor und Quad-Prozessor) aus, indem Sie auf den **Anfangspreis** klicken.
4. Geben Sie die **Menge** _identischer_ Server ein, die bereitgestellt werden sollen. Der Standardwert ist 1. Wenn Sie mehrere Server mit _unterschiedlichen_ Spezifikationen bereitstellen möchten, müssen Sie die Server separat bereitstellen.
5. Wählen Sie Ihren **RAM** aus. Für einige Server basieren die RAM-Standardwerte auf dem CPU-Modell und können nicht geändert werden. 

Für SAP-zertifizierte Server basieren die Standardwerte für RAM und Betriebssystem auf Ihrer Serverauswahl. Der Standardwert für die Option für Ihren lokalen Speicher basiert auch auf Ihrer Serverauswahl.
{ :note}

6. Wählen sie Ihr Betriebssystem aus.
7. Wählen Sie Ihre Festplatten und zusätzliche System-Add-ons aus.
8. Klicken Sie auf **Zur Bestellung hinzufügen**. Anschließend werden Sie weitergeleitet, um Ihre Bestellung zu bestätigen.
9. Bestätigen Sie die Domäneninformationen für den Server oder bearbeiten Sie sie. **Hostname** ist ein permanenter oder temporärer Name für Ihren Server, beispielsweise 'baremetal01'. 
10. Wählen Sie die Cloud-Service-Bedingungen**** und die Servicevereinbarungen Dritter**** aus.
11. Geben Sie alle vorhandenen Werbeaktionscodes unter **Werbeaktionscode** ein und klicken Sie auf **Anwenden**.
12. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf die Schaltfläche **Bestellung abschicken**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt, die Sie drucken können, da sie auch Ihr Beleg ist. 

Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der Fertigstellungsnachricht gelangen Sie direkt zu Ihrer Seite *Einheitendetails*, nachdem Sie sich bei {{site.data.keyword.Bluemix_notm}} angemeldet haben. Sie können sich auch direkt beim {{site.data.keyword.slportal}} anmelden.

## Nächste Schritte
Nachdem Ihr {{site.data.keyword.baremetal_short}} bereitgestellt ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [{{site.data.keyword.baremetal_short}} verwalten](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
