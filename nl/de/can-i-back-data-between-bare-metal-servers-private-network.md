---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Backup und Wiederherstellung

{{site.data.keyword.Bluemix_notm}} bietet eine Vielzahl skalierbarer [Backup- und Speicherlösungen](https://www.softlayer.com/cloud-storage), um Ihre Backup-Anforderungen zu erfüllen. Wir führen jedoch keine Gesamtsicherung von Kundeneinheiten durch. Ein Benutzer, der zu Ihrem Konto gehört, muss alle geplanten und einmaligen Backups auf Ihren Einheiten initiieren. 

Wenn Ihrem Konto zwei oder mehrere {{site.data.keyword.baremetal_short}} zugeordnet sind, können die Daten von einer Einheit zu einer anderen Einheit gesichert werden. Es gibt keine Bandbreitenbeschränkung für den Datenverkehr im privaten Netz, sodass Daten jederzeit zwischen den Einheiten übertragen oder gesichert werden können, die ein Konto gemeinsam nutzen.
Es gibt für {{site.data.keyword.baremetal_short}} mehrere Sicherungslösungen, unter anderem folgende:

1. [EVault Backup](/infrastructure/backup/index.html) ist eine Sicherungslösung für Unternehmen, die Backups über mehrere Server hinweg automatisieren kann. Die Daten werden in einem Unternehmens-SAN (Storage Area Network) gespeichert.
* [Network Attached Storage (NAS)](/infrastructure/network-attached-storage/nas.html) ist ein Branchenstandard und bietet für kritische Daten Speicher außerhalb des Servers an. Die Daten werden in einem Unternehmens-SAN (Storage Area Network) gespeichert.
* [R1Soft CDP](/infrastructure/backup/r1soft.html) bietet eine leistungsstarke Disk-to-Disk-Serversicherung mit einem zentralen Management- und Datenrepository an. R1Soft CDP schützt Daten auf Blockebene. Eindeutige Plattenblöcke auf dem Server werden ein einziges Mal über alle Wiederherstellungspunkte hinweg gespeichert, wodurch sich die Speichereffizienz erhöht.
