---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-21"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Aus den gängigsten Servern auswählen
Die Server in der Liste der gängigsten Server sind für die Anforderungen der meisten Anwendungsfälle von Kunden vorkonfiguriert und sind 30-40 Minuten nach der Bestellung betriebsbereit. 
1. Öffnen Sie den [{{site.data.keyword.cloud_notm}}-Katalog](https://console.bluemix.net/catalog/){:target="_blank"}.    
2. Wählen Sie Bare Metal Servers aus. 
3. Klicken Sie auf "Erstellen". 
2. Wählen Sie die folgenden Informationen aus:
    <table>
    <CAPTION>Tabelle 1. Auszuwählende Bare-Metall-Optionen</CAPTION>
    <THEAD>
    <TR>
    <th>Feld</th>
    <th>Wert</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Menge</td>
    <td>Geben Sie mithilfe der Symbole + und - die Anzahl der identischen Server an, die bereitgestellt werden sollen. <br>Wenn Sie mehrere Server mit unterschiedlichen Spezifikationen bereitstellen möchten, müssen Sie diese separat bereitstellen.
    <tr>
    <td>Standort</td>
    <td>Wählen Sie die Region und das Rechenzentrum aus, in der/dem der Server sich befinden soll. </td>
    </tr>
    <tr>
    <tr>
    <td>Hostname und Domäne</td>
    <td>Diese Felder sind mit dem Standardwert belegt. Sie können sie ändern. </td>
    </tr>
    <tr>
    <td>Wählen Sie Ihren Server aus</td>
    <td>Wählen Sie unter **Gängige Server** den Server aus, der Ihren Anforderungen entspricht. Diese Server sind vorkonfiguriert und können in 30 bis 40 Minuten verwendet werden.
    </tr>
    <tr>
    <td>RAM</td>
    <td>Standardwert auf der Basis des Servers, den Sie ausgewählt haben. </td>
    </tr>
    <tr>
    <td>SSH-Schlüssel</td>
    <td>Geben Sie einen öffentlichen Schlüssel Ihres SSH-Schlüssels an, den Sie verwenden, um sich bei Ihrem Server anzumelden, nachdem er bereitgestellt wurde. </td>
    </tr>
    <tr>
    <td>Image <br>(Betriebssystem)</td>
    <td>Wählen Sie das Betriebssystem für die Instanz aus. **Hinweis**: Es wird eine Fehlernachricht angezeigt, wenn ein Konflikt zwischen dem Server und dem Betriebssystem besteht. Ein Beispiel ist die Auswahl von Linux auf einem Microsoft SQL Server. </td>
    </tr>
    <td>Uplink-Port-Geschwindigkeiten</td>
    <td>Bestimmt die Geschwindigkeit der internen und externen Schnittstellen.</td>
    </tr>
    <tr>
    <td>Add-ons</td>
    <td> Wählen Sie die entsprechenden Optionen aus oder verwenden Sie die Standardwerte. </td>
    </tr>
    </TBODY>
    </table>

3.  Wählen Sie im Abschnitt "Bestellübersicht" **Stündlich** oder **Monatlich** für die Abrechnung aus. 
4.  Überprüfen Sie Ihre Bestellung. 
5.  Lesen Sie die Vereinbarungen für Services anderer Anbieter, die aufgelistet werden, und klicken Sie auf das Kontrollkästchen für Servicevereinbarungen Dritter.**** 
6.  Klicken Sie auf **Bereitstellung**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige. Sie ist die Auftragsbestätigung für Ihre Bereitstellungsbestellung.

 Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung. Die Fertigstellungsnachricht enthält einen Link zu Ihrer Seite *Einheitendetails*, sodass Sie sich bei {{site.data.keyword.cloud_notm}} anmelden können. Sie können sich auch direkt beim {{site.data.keyword.slportal}} anmelden.


## Nächste Schritte
Nachdem Ihr {{site.data.keyword.baremetal_short}} bereitgestellt ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [{{site.data.keyword.baremetal_short}} verwalten](../bare-metal/managing.html).
