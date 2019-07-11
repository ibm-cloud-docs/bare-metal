---

copyright:
  years: 1994, 2019
lastupdated: "2019-05-02"

keywords: back up, recovery, IBM Cloud Backup, r1soft

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Sicherung und Wiederherstellung
{: #sm-back-up-recovery}

{{site.data.keyword.Bluemix_notm}} bietet eine Vielzahl skalierbarer [Sicherungs- und Speicherlösungen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/cloud/storage){: new_window}, um Ihre Sicherungsanforderungen zu erfüllen. {{site.data.keyword.Bluemix_notm}} führt jedoch keine Sicherungen von Kundeneinheiten aus. Ein Benutzer, der zu Ihrem Konto gehört, muss alle geplanten und einmaligen Sicherungen auf Ihren Einheiten einleiten.

Wenn Ihrem Konto zwei oder mehr {{site.data.keyword.baremetal_short}} zugeordnet sind, können die Daten von einer Einheit auf einer anderen Einheit gesichert werden. Es wird keine Bandbreitenbeschränkung für den Datenverkehr im privaten Netz erzwungen, sodass Daten jederzeit zwischen den Einheiten übertragen oder gesichert werden können, die ein Konto gemeinsam nutzen. Für {{site.data.keyword.baremetal_short}} sind mehrere Sicherungslösungen verfügbar, darunter die folgenden:

* [IBM Cloud Backup](/docs/infrastructure/Backup?topic=Backup-getting-started#getting-started) ist eine Sicherungslösung für Unternehmen, die Sicherungen über mehrere Server hinweg automatisieren kann. Die Daten werden in einem Unternehmens-SAN (Storage Area Network) gespeichert.
* [Network Attached Storage (NAS)](/docs/infrastructure/network-attached-storage?topic=network-attached-storage-GettingStarted#GettingStarted) ist ein Branchenstandard und bietet für kritische Daten Speicher außerhalb des Servers an. Die Daten werden in einem Unternehmens-SAN (Storage Area Network) gespeichert.
* [R1Soft CDP](/docs/infrastructure/software?topic=software-ordering-r1soft#ordering-r1soft) bietet eine leistungsfähige Lösung für die Serversicherung von Platte auf Platte mit zentralem Management- und Datenrepository. R1Soft CDP schützt Daten auf Blockebene. Eindeutige Plattenblöcke auf dem Server werden ein einziges Mal über alle Wiederherstellungspunkte hinweg gespeichert, wodurch sich die Speichereffizienz erhöht.
