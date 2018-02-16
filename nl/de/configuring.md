---



copyright:
  years: 2017
lastupdated: "2017-12-05"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Ihre Bare-Metal-Server konfigurieren

Es ist ratsam, sich vor der Bereitstellung der {{site.data.keyword.baremetal_long}} Gedanken über die Konfiguration zu machen. Dadurch läuft die Bereitstellung schneller und reibungsloser ab. {:shortdesc}

## Nutzung und Größe des Servers bestimmen

Die erste Aufgabe ist es zu bestimmen, wie Ihre {{site.data.keyword.baremetal_short}} genutzt werden sollen. Benötigen Sie sie beispielsweise für Entwicklung/Tests oder für die Produktion? Testen Sie die Benutzererfahrung, die Verarbeitung langer Algorithmen, die Sicherung und Wiederherstellung von Daten oder die Erhöhung der Latenz (Geschwindigkeit)?

Nachdem Sie bestimmt haben, wie die {{site.data.keyword.baremetal_short}} genutzt werden sollen, legen Sie die Größe fest. Der [SoftLayer-Rechner für die Gesamtbetriebskosten](http://www.softlayer.com/tco/) unterstützt Sie dabei, wie {{site.data.keyword.baremetal_short}} Ihre Bedürfnisse bestmöglich erfüllen können.

## Ihren Server auswählen

{{site.data.keyword.cloud_notm}} bietet sieben Server für die schnelle Bereitstellung, um sicherzustellen, dass Sie die Leistung erhalten, die Sie für Ihre Workload benötigen. Diese Server stehen zurzeit im Vereinigten Königreich und in den Vereinigten Staaten (Süden) zur Verfügung.

| **Konfiguration** | **Prozessor** | **Speicher** | **Festplattenlaufwerk** | **Portgeschwindigkeit** |
|-------------------|---------------|------------|----------------|----------------|
| Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 Kerne, 3,50 GHz) |32 GB RAM |1 internes Festplattenlaufwerk |100 MB/s maximale Portgeschwindigkeit|
|Intel Xeon E5-2620 v3 |Dual Intel Xeon E5-2620 v3 (6 Kerne, 2,40 GHz) |64 GB RAM |2 interne Festplattenlaufwerke |100 MB/s maximale Portgeschwindigkeit|
|Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 Kerne, 3,50 GHz) |32 GB RAM |2 interne Festplattenlaufwerke |100 MB/s maximale Portgeschwindigkeit|
|Intel Xeon E5-2650 v3 |Dual Intel Xeon E5-2650 v3 (10 Kerne, 2,30 GHz) |128 GB RAM |1 internes Festplattenlaufwerk |100 MB/s maximale Portgeschwindigkeit|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 Kerne, 2,60 GHz) |128 GB RAM |2 interne Festplattenlaufwerke |100 MB/s maximale Portgeschwindigkeit|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 Kerne, 2,60 GHz) |64 GB RAM |4 interne Festplattenlaufwerke |1000 MB/s maximale Portgeschwindigkeit|
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 Kerne, 2,60 GHz) |256 GB RAM |4 interne Festplattenlaufwerke |1000 MB/s maximale Portgeschwindigkeit|

Neben den sieben Servern für die schnelle Bereitstellung erweiterte {{site.data.keyword.cloud_notm}} sein {{site.data.keyword.baremetal_short}}-Angebot und enthält jetzt POWER8-basierte Bare-Metal-Systeme. Diese Systeme enthalten den {{site.data.keyword.IBM_notm}}-POWER8-Prozessor und eine OpenPOWER-basierte Plattform, die speziell für cloudbasierte Bereitstellungen von Daten und kognitiven wie webbasierten Workloads unter Linux optimiert wurde.

Alle {{site.data.keyword.baremetal_short}} können auf eine uneingeschränkte (unbegrenzte) Bandbreite aktualisiert werden. Alle uneingeschränkten Einheiten sind private, dedizierte Ports.

## Ihre Bare-Metal-Server einrichten

Nachdem Sie Ihr Rechenzentrum, den Server und die Fakturierungsoption (monatlich oder stündlich) ausgewählt haben, legen Sie fest, wie Sie Ihren Server konfigurieren möchten. Einige Felder (Server, RAM, Grafikprozessor und sekundärer Grafikprozessor) auf der Seite **Ihre {{site.data.keyword.baremetal_short}} konfigurieren** sind je nachdem, welchen Server Sie ausgewählt haben, standardmäßig ausgefüllt. In der folgenden Tabelle wird beschrieben, für welche Felder Sie einen Wert definieren können.

| **Feld** | **Beschreibung** |
|-------------------|---------------|
|Betriebssystem |Wählen Sie zwischen CentOS, FreeBSD, Microsoft, Red Hat, Ubuntu oder Sonstiges aus. |
|Festplatten |Das Tool zur Datenträgerkonfiguration unterstützt Sie bei der Festplatteneinrichtung, indem die Felder je nach Betriebssystem vorab ausgefüllt sind. |
|Öffentliche Bandbreite |Bestimmt das Datenvolumen, das über die öffentliche Schnittstelle in einem Monat übertragen werden kann. In Testumgebungen, bei denen Installationsdaten über diese Schnittstelle übertragen werden, müssen die Werte so angepasst werden, dass sie das ursprünglich übertragene Datenvolumen übersteigen. Sie könnten mit dem [{{site.data.keyword.cloud_notm}} Content Delivery Network](https://www.ibm.com/cloud/cdn) eine erste Datenlast zu einem der {{site.data.keyword.cloud_notm}}-Rechenzentren ausliefern. |
|Uplink-Port-Geschwindigkeiten |Bestimmt die Geschwindigkeit der internen und externen Schnittstellen. |
|Sekundäre öffentliche IP-Adressen |Weist Ihrem Server eine weitere IP-Adresse zu. Sie benötigen je nach Szenario möglicherweise weitere IP-Adressen, die Ihrem Server zugewiesen werden. Weitere IPv4-Adressen sind in den Mengen 1, 2, 4, 8, 16 oder 32 verfügbar. |
|Primäre IPv6-Adressen |Werden den internen sowie externen Schnittstellen Ihres Servers zugewiesen. |
|Statische öffentliche IPv6-Adressen |Weist weitere IPv6-Adressen eines /64-Blocks zu. |
|Hardware- & Software-Firewalls, Viren- & Spyware-Schutz und Abwehrsystem & Erkennung gegen Angriffe von außen |Wählen Sie die entsprechenden Optionen aus, wenn der Server internetfähig ist. Es wird dringend empfohlen, dass sich die für die Sicherheit verantwortliche Unternehmensabteilung mit dem {{site.data.keyword.cloud_notm}}-Support abstimmt, um die Details dieser Optionen zu besprechen. |
|EVault |Ein agentenbasiertes Sicherungstool, das auf Ihrem Server installiert werden kann, um Backups zwischen Servern zu replizieren. |

Nutzen Sie wenden Sie sich an den {{site.data.keyword.cloud_notm}}-Support, um weitere Informationen zu erhalten.


## Erweiterte Systemkonfiguration

Die erweiterte Systemkonfiguration wird durchgeführt, nachdem Sie auf die Schaltfläche **Zur Bestellung hinzufügen** geklickt haben und zur Checkout-Seite weitergeleitet wurden. In der folgenden Tabelle werden die Felder der erweiterten Systemkonfiguration beschrieben.

| **Feld** | **Beschreibung** |
|-------------------|---------------|
|Hostname |Ein permanenter oder temporärer Name für Ihren Server, beispielsweise _server1_. |
|Domäne |Name der Unterdomäne, die nicht mit dem Internetdomänennamen identisch sein darf, beispielsweise _test.acme.com_. |
|VLAN-Auswahl |Wenn Sie für Ihr Konto ein VLAN haben, weil Sie bereits mindestens einen Server bestellt haben, können Sie diesem VLAN den neuen Server hinzufügen. |
|Bereitstellungsscript |Sie stellen ein Script bereit, mit dem bestimmte Schritte automatisiert werden, nachdem der Server bereitgestellt wurde. |
|SSH-Schlüssel |Sie können einen öffentlichen Schlüssel für Ihren SSH-Schlüssel bereitstellen, mit dem Sie sich bei Ihrem Server anmelden können, nachdem er bereitgestellt wurde. |
