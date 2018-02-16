---



copyright:
  years: 2017
lastupdated: "2017-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Bare-Metal-Server bereitstellen

## Vorbereitungen
Sie haben zwei Möglichkeiten, um Ihre öffentlichen {{site.data.keyword.baremetal_long}} bereitzustellen. Die erste Möglichkeit ist die Verwendung des {{site.data.keyword.cloud}}-Katalogs und die zweite Möglichkeit ist das {{site.data.keyword.slportal_full}}. Für den Katalog und für das {{site.data.keyword.slportal}} sind eindeutige Anmelde-IDs erforderlich. Sie können sich mit dem Benutzernamen und Kennwort für den Katalog daher nicht beim Portal anmelden und umgekehrt.
{:shortdesc}

Stellen Sie vorab sicher, dass Sie über gültige Berechtigungsnachweise für den {{site.data.keyword.cloud_notm}}-Katalog oder für das {{site.data.keyword.slportal}} verfügen. 
  
**Hinweis:** Sie müssen über ein aktualisiertes Konto für den {{site.data.keyword.cloud_notm}}-Katalog verfügen, um {{site.data.keyword.baremetal_short}} zu bestellen. Weitere Informationen zum Aktualisieren Ihres Kontos finden Sie unter [Zur IBMid wechseln](https://console.ng.bluemix.net/docs/admin/softlayerlink.html).
  
## Anmelden 
Stellen Sie sicher, dass Sie angemeldet sind (entweder beim {{site.data.keyword.cloud_notm}}-Katalog oder beim {{site.data.keyword.slportal}}): 

  <table>
   <CAPTION>Tabelle 1.Anmeldeposition auswählen</CAPTION>
   <THEAD>
   <TR>
   <th>Anmeldung mit...</th>
   <th>Vorgehensweise</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud-Katalog</td>
   <td>
   <ol>
   <li>Öffnen Sie ein neues Browserfenster und geben Sie <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a> ein.</li>
   <li>Klicken Sie auf den Link <b>Anmelden</b>. </li>
   <li>Geben Sie Ihre E-Mail-Adresse oder Ihre IBMid ein und klicken Sie auf <b>Weiter</b>.</li>
   <li>Geben Sie Ihr Kennwort ein und klicken Sie auf <b>Anmelden</b>.</li>
   <li>Wählen Sie <b>Infrastruktur</b> > <b>Compute</b> aus.</li>
   <li>Klicken Sie auf die <b>{{site.data.keyword.baremetal_short}}</b>-Kachel.</li>
   <li>Klicken Sie auf <b>Erstellen</b>. Die Hauptseite des {{site.data.keyword.slportal}}s wird geöffnet.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Kundenportal</td>
   <td>
   <ol>
   <li>Öffnen Sie ein neues Browserfenster und geben Sie <a href="https://control.softlayer.com">https://control.softlayer.com</a> ein.</li>
   <li>Geben Sie Ihren Benutzernamen und Ihr Kennwort ein und klicken Sie auf <b>Anmeldung</b>. Oder klicken Sie auf <b>Melden Sie sich mit der IBMid an</b>. Geben Sie anschließend Ihre E-Mail-Adresse oder Ihre IBMid ein und klicken Sie auf <b>Weiter</b>. Geben Sie Ihr Kennwort ein und klicken Sie auf <b>Anmelden</b>. Die Hauptseite des {{site.data.keyword.slportal}}s wird geöffnet.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Einen Bare-Metal-Server bereitstellen
{: #ordering-baremetal-server}
Nach der Anmeldung können Sie mit der Bereitstellung des {{site.data.keyword.baremetal_short}}s starten. Sie können Ihren {{site.data.keyword.baremetal_short}} über das Menü **Einheiten** oder das Symbol **Einheiten** bereitstellen.

### Einen Bare-Metal-Server über das Symbol "Einheiten" bereitstellen
Führen Sie die folgenden Schritte aus, um Ihre {{site.data.keyword.baremetal_short}} über das Symbol *Einheiten* bereitzustellen:

1.  Suchen Sie im {{site.data.keyword.slportal}} den Abschnitt **Bestellung** und klicken Sie auf **Einheiten**.
2.  Klicken Sie auf der Seite 'Einheiten' auf **Stündlich** oder **Monatlich** unter {{site.data.keyword.baremetal_short}}.
3.  Wählen Sie Ihr **Rechenzentrum** aus, blättern Sie durch die Seite und klicken Sie auf den Link **Startpreis pro**, um Ihren Server auszuwählen. 
4.  Füllen Sie die Seite **Ihren {{site.data.keyword.baremetal_short}} konfigurieren** aus und klicken Sie zum Fortfahren auf die Schaltfläche **Zur Bestellung hinzufügen**. Weitere Informationen, wie Sie Ihren Server konfigurieren können, finden Sie unter [Ihren {{site.data.keyword.baremetal_short}} konfigurieren](../bare-metal/configuring.md). Sobald Ihre Bestellung bestätigt wurde, werden Sie auf die Seite **Checkout** weitergeleitet.
5.  Geben Sie die **Erweiterte Systemkonfiguration** für den Server ein. Weitere Informationen zur Einrichtung finden Sie unter [Ihren {{site.data.keyword.baremetal_short}} konfigurieren](../bare-metal/configuring.md).
6.  Klicken Sie auf die Kontrollkästchen für Cloud-Service-Bedingungen**** und für Servicevereinbarungen Dritter****.
7.  Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf die Schaltfläche **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige. Sie ist die Auftragsbestätigung für Ihre Bereitstellungsbestellung.

 Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der Fertigstellungsnachricht gelangen Sie direkt zu der zugehörigen Seite *Einheitendetails*, nachdem Sie sich bei {{site.data.keyword.cloud_notm}} angemeldet haben. Sie können sich auch direkt beim {{site.data.keyword.slportal}} anmelden.

### Einen Bare-Metal-Server über das Menü "Einheiten" bereitstellen
{: #ordering-baremetal-devices-menu}

Sie können Ihren {{site.data.keyword.baremetal_short}} über das Menü *Einheiten* oder auf der {{site.data.keyword.slportal}}-Hauptseite bereitstellen. 

1. Klicken Sie auf **Einheiten > Einheitenliste**. Auf der Seite 'Einheiten' werden alle Einheitentypen in Ihrem Konto angezeigt (dedizierte Hosts, virtuelle Server, Bare-Metal-Server und NetScaler-Controller für Anwendungsbereitstellung).
2. Klicken Sie auf den Link **Einheiten bestellen** in der rechten oberen Ecke.
3. Klicken Sie auf der Seite für SoftLayer-Produkte und -Services auf **Stündlich** oder **Monatlich** unter {{site.data.keyword.baremetal_short}}.
4. Wählen Sie Ihr **Rechenzentrum** aus, blättern Sie durch die Seite und klicken Sie auf den Link **Startpreis pro**, um Ihren Server auszuwählen. 
5.  Füllen Sie die Seite **Ihren {{site.data.keyword.baremetal_short}} konfigurieren** aus und klicken Sie zum Fortfahren auf die Schaltfläche **Zur Bestellung hinzufügen**. Weitere Informationen, wie Sie Ihren Server konfigurieren können, finden Sie unter [Ihren {{site.data.keyword.baremetal_short}} konfigurieren](../bare-metal/configuring.md). Sobald Ihre Bestellung bestätigt wurde, werden Sie auf die Seite **Checkout** weitergeleitet.
6.  Geben Sie die **Erweiterte Systemkonfiguration** für den Server ein. Weitere Informationen zur Einrichtung finden Sie unter [Ihren {{site.data.keyword.baremetal_short}} konfigurieren](../bare-metal/configuring.md).
7. Klicken Sie auf die Kontrollkästchen für Cloud-Service-Bedingungen**** und für Servicevereinbarungen Dritter****.
8. Bestätigen Sie Ihre Zahlungsinformationen oder geben Sie sie ein und klicken Sie auf die Schaltfläche **Bestellung absenden**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige. Sie ist die Auftragsbestätigung für Ihre Bereitstellungsbestellung.

Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Über einen Link in der Fertigstellungsnachricht gelangen Sie direkt zu der zugehörigen Seite *Einheitendetails*, nachdem Sie sich bei {{site.data.keyword.cloud_notm}} angemeldet haben. Sie können sich auch direkt beim {{site.data.keyword.slportal}} anmelden.

### Nächste Schritte
Nachdem Ihr {{site.data.keyword.baremetal_short}} bereitgestellt ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [{{site.data.keyword.baremetal_short}} verwalten](../bare-metal/managing.html).
