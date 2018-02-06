---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Ist RAID die einzige Sicherungslösung, die erforderlich ist? Ist das überhaupt eine Backuplösung?

RAID ist keine Backuplösung. RAID erstellt eine einzelne verwendbare Datenplatte, auf der mehrere physische Festplatten für eine höhere Geschwindigkeit und/oder Fehlertoleranz zu einem Array kombiniert werden. 

SoftLayer stellt einige Sicherungslösungen bereit:

1. [EVault Backup](/infrastructure/backup/index.html) ist eine Sicherungslösung für Unternehmen, die Backups über mehrere Server hinweg automatisieren kann. Die Daten werden in einem Unternehmens-SAN (Storage Area Network) gespeichert.
* [Network Attached Storage (NAS)](/infrastructure/network-attached-storage/nas.html) ist ein Branchenstandard und bietet für kritische Daten Speicher außerhalb des Servers an. Die Daten werden in einem Unternehmens-SAN (Storage Area Network) gespeichert.
* [R1Soft CDP](/infrastructure/backup/r1soft.html) bietet eine leistungsstarke Disk-to-Disk-Serversicherung mit einem zentralen Management- und Datenrepository an. R1Soft CDP schützt Daten auf Blockebene. Eindeutige Plattenblöcke auf dem Server werden ein einziges Mal über alle Wiederherstellungspunkte hinweg gespeichert, wodurch sich die Speichereffizienz erhöht.
