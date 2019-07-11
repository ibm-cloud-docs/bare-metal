---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-02"

keywords: provision bare metal, popular servers, {{site.data.keyword.baremetal_short}}, provision

subcollection: bare-metal


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Aus den gängigsten Servern auswählen
{: #bm-select-popular-servers}

Die Server in der Liste der gängigsten Server sind für die Anforderungen der meisten Anwendungsfälle von Kunden vorkonfiguriert und sind 30-40 Minuten nach der Bestellung betriebsbereit.
1. Öffnen Sie den [{{site.data.keyword.cloud_notm}}-Katalog ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/catalog/){: new_window}.   
2. Wählen Sie Bare Metal Servers aus.
3. Klicken Sie auf 'Weiter'. Wenn Sie keine Schaltfläche 'Weiter' sehen, müssen Sie sich möglicherweise anmelden.
2. Wählen Sie im Abschnitt '{{site.data.keyword.baremetal_short}}' die folgenden Informationen aus:
    <table>
    <CAPTION>Tabelle 1. Auszuwählende Bare-Metal-Optionen</CAPTION>
    <THEAD>
    <TR>
    <th>Feld</th>
    <th>Wert</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Menge</td>
    <td>Geben Sie mithilfe der Symbole + und - die Anzahl der **identischen** Server an, die bereitgestellt werden sollen. Der Standardwert ist 1.<br>Wenn Sie mehrere Server mit **unterschiedlichen** Spezifikationen bereitstellen möchten, müssen Sie diese separat bereitstellen.
    <tr>
    <tr>
    <td>Abrechnungstyp</td>
    <td>Wählen Sie 'Stündlich' oder 'Monatlich' aus.
    <tr>
    <td>Hostname und Domäne</td>
    <td>Diese Felder sind mit dem Standardwert belegt. Sie können sie ändern.</td>
    </tr>
    <tr>
    <td>Standort</td>
    <td>Wählen Sie die Region aus, in der sich der Server befinden soll. Wählen Sie in der Dropdown-Liste ein Rechenzentrum in der Region aus.</td>
    </tr>
    <tr>
    <tr>
    <td>Wählen Sie Ihren Server aus</td>
    <td>Wählen Sie **Gängige Server** und anschließend den Server aus, der Ihren Anforderungen entspricht. Diese Server sind vorkonfiguriert und können in 30 bis 40 Minuten verwendet werden.
    </tr>
    <tr>
    <td>RAM</td>
    <td>Standardwert auf der Basis des Servers, den Sie ausgewählt haben.</td>
    </tr>
    <tr>
    <td>SSH-Schlüssel</td>
    <td>Geben Sie einen öffentlichen Schlüssel Ihres SSH-Schlüssels an, den Sie verwenden, um sich bei Ihrem Server anzumelden, nachdem er bereitgestellt wurde.</td>
    </tr>
    <tr>
    <td>Image <br>(Betriebssystem)</td>
    <td>Wählen Sie das Betriebssystem für den System aus. Ihre Image-Optionen können auf der Basis des Servers, den Sie ausgewählt haben, begrenzt  sein.</td>
    </tr>
    <td>Add-ons</td>
    <td>Erweitern Sie den Abschnitt 'Add-ons', um die entsprechenden Optionen auszuwählen, oder verwenden Sie die Standardwerte.</td>
    </tr>
    </TBODY>
    </table>
3. Im Abschnitt 'Speicherplatten' ist die Speicherplatte bereits für Ihre Auswahl in 'Gängige Server' ausgewählt. Erweitern Sie den Abschnitt 'Add-ons', wenn Sie Ihrem Server IBM Cloud Backup hinzufügen wollen.
4. Wählen Sie unter 'Netzschnittstelle' die Uplink-Port-Geschwindigkeiten aus. Erweitern Sie den Abschnitt 'Add-ons', um die entsprechenden Optionen auszuwählen, oder verwenden Sie die Standardwerte.
4.  Überprüfen Sie Ihre Bestellung.
4. Erweiteren Sie 'Werbeaktionscode anwenden', um gegebenenfalls einen Werbeaktionscode auf Ihre Bestellung anzuwenden.  
5.  Lesen Sie die Vereinbarungen für Services anderer Anbieter, die aufgelistet werden, und klicken Sie auf das Kontrollkästchen für Servicevereinbarungen Dritter.****
6.  Klicken Sie auf **Bereitstellung**. Eine Anzeige mit der Nummer Ihrer Bereitstellungsbestellung wird angezeigt. Drucken Sie diese Anzeige. Sie ist die Auftragsbestätigung für Ihre Bereitstellungsbestellung.

 Mehrere E-Mails werden an Ihren Administrator gesendet: die Auftragsbestätigung für die Bereitstellungsbestellung, die Genehmigung und die Bearbeitungsnachricht für die Bereitstellung sowie die Fertigstellungsnachricht für die Bereitstellung.

 Die _Fertigstellungsnachricht_ enthält einen Link zu Ihrer Seite *Einheitendetails*, sodass Sie sich bei {{site.data.keyword.cloud_notm}} anmelden können. Sie können sich auch direkt beim {{site.data.keyword.slportal}} anmelden.


## Nächste Schritte

Nachdem Ihr {{site.data.keyword.baremetal_short}} bereitgestellt ist, können Sie ihn verwalten. Weitere Informationen finden Sie unter [{{site.data.keyword.baremetal_short}} verwalten](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
