---

copyright:
  years: 1994, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Sicherung und Wiederherstellung

{{site.data.keyword.Bluemix_notm}} bietet eine Vielzahl skalierbarer [Sicherungs- und Speicherlösungen](https://www.softlayer.com/cloud-storage), um Ihre Sicherungsanforderungen zu erfüllen. {{site.data.keyword.Bluemix_notm}} führt jedoch keine Sicherungen von Kundeneinheiten aus. Ein Benutzer, der zu Ihrem Konto gehört, muss alle geplanten und einmaligen Sicherungen auf Ihren Einheiten einleiten. 

Wenn Ihrem Konto zwei oder mehr {{site.data.keyword.baremetal_short}} zugeordnet sind, können die Daten von einer Einheit auf einer anderen Einheit gesichert werden. Es wird keine Bandbreitenbeschränkung für den Datenverkehr im privaten Netz erzwungen, sodass Daten jederzeit zwischen den Einheiten übertragen oder gesichert werden können, die ein Konto gemeinsam nutzen. Für {{site.data.keyword.baremetal_short}} sind mehrere Sicherungslösungen verfügbar, darunter die folgenden: 

1. [EVault Backup](../infrastructure/backup/index.html) ist eine Sicherungslösung für Unternehmen, die Sicherungen über mehrere Server hinweg automatisieren kann. Die Daten werden in einem Unternehmens-SAN (Storage Area Network) gespeichert.
* [Network Attached Storage (NAS)](../infrastructure/network-attached-storage/nas.html) ist ein Branchenstandard und bietet für kritische Daten Speicher außerhalb des Servers an. Die Daten werden in einem Unternehmens-SAN (Storage Area Network) gespeichert.
* [R1Soft CDP](../infrastructure/backup/r1soft.html) bietet eine leistungsfähige Lösung für die Serversicherung von Platte auf Platte mit zentralem Management- und Datenrepository. R1Soft CDP schützt Daten auf Blockebene. Eindeutige Plattenblöcke auf dem Server werden ein einziges Mal über alle Wiederherstellungspunkte hinweg gespeichert, wodurch sich die Speichereffizienz erhöht.
