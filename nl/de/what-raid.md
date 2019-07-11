---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords: raid, about raid

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# Informationen zu RAID
{: #bm-raid-levels}

RAID (Redundant Array of Independent Disks) erstellt eine einzelne verwendbare Datenplatte, auf der mehrere physische Festplatten für eine höhere Geschwindigkeit und Fehlertoleranz zu einem Array kombiniert werden. Die folgenden drei Konzepte sind bei RAID grundlegend:
* **Spiegelung**: Daten auf mehr als eine Platte kopieren.
* **Striping**: Daten über mehr als eine Platte verteilen. 
* **Fehlerkorrektur** (Fehlertoleranz): Redundante Daten werden gespeichert, damit Probleme erkannt und möglicherweise behoben werden können.

Obwohl es viele verschiedene RAID-Stufen gibt, unterstützt {{site.data.keyword.IBM_notm}} die häufigsten RAID-Typen: 0, 1, 5, 6 und 10. Die verschiedenen RAID-Stufen nutzen eine oder mehrere Verfahren, je nach Systemanforderungen. Der Hauptzweck der Verwendung von RAID besteht darin, die Zuverlässigkeit zu verbessern, indem entweder 3Ware 9550SX Raid SATA- oder Adaptec SA-SCSI RAID-Controller für alle bereitgestellten RAID-Lösungen verwendet werden.

RAID ist keine Sicherungslösung. Stattdessen erstellt RAID eine einzelne verwendbare Datenplatte, auf der mehrere physische Festplatten für eine höhere Geschwindigkeit und Fehlertoleranz zu einem Array kombiniert werden.
{: note}

**RAID 0** (Stripe-Set ohne Parität/nicht redundantes Array) Implementiert ein Datenstriping, bei dem Dateiblöcke auf mehrere Platten in Fragmenten geschrieben und mindestens zwei Laufwerke benötigt werden. Der Vorteil von RAID 0 ist die erheblich höhere Lese-/Schreibgeschwindigkeit. Je mehr Laufwerke im Array vorhanden sind, desto höher ist die Bandbreite. Der Nachteil von RAID 0 ist, dass es keine Fehlertoleranz gibt. Wenn ein einziges Laufwerk ausfällt, ist der Array beschädigt. RAID 0 implementiert auch keine Fehlerprüfung. Das heißt, Fehler sind nicht behebbar. Eine allgemein übliche Lösung für die Fehlertoleranz ist ein Laufwerk außerhalb des Arrays, das im Fall eines Hardwarefehlers als Ausweichspeicher verwendet wird.

**RAID 1** (Spiegelung ohne Parität) Implementiert eine Datenspiegelung. Die Daten werden auf 2 oder 4 Platten über einen RAID-Hardware-Controller dupliziert und bieten eine gewisse Fehlertoleranz. Das Array kann wiederhergestellt werden, wenn mindestens ein Laufwerk noch funktionstüchtig ist. Es bietet eine schnellere Leseleistung als ein einzelnes Laufwerk und stellt Laufwerkredundanz bereit, wenn ein Laufwerk ausfällt. Die Schreibgeschwindigkeit ist leicht verringert.

**RAID 5** (Stripe-Set mit dualer verteilter Parität) Implementiert Datenstriping auf Blockebene und verteilt die Parität zwischen den Platten. Die Paritätsinformationen ermöglichen die Wiederherstellung, wenn ein einzelnes Laufwerk ausfällt, da alle folgenden Lesevorgänge anhand der verteilten Parität berechnet werden können. RAID 5 ermöglicht auch eine höhere Lese-/Schreibgeschwindigkeit und die effiziente Nutzung des Plattenspeichers. RAID 5 benötigt mindestens drei Platten.

**RAID 6** (Doppelte Parität) Implementiert Stripes mit doppelter Parität auf jeder Platte und ermöglicht, dass zwei Platten ausfallen können, bevor Daten verloren gehen. Da RAID 6 eine Kapazität von zwei Platteneinheiten hat, die zum Speichern von Paritätsdaten in einer Paritätsgruppe dediziert sind, sind mit RAID 6 umfangreichere E/A-Operationen als mit RAID 5 möglich. Diese umfangreicheren E/A-Operationen können zu einem Leistungsrückgang führen. RAID 6 erfordert mindestens 4 Platten und maximal 18 Platten.

**RAID 10** (RAID 1 + 0) Erstellt mehrere Spiegelserver, in denen Daten als Stripes (Streifen) über mehrere Platten hinweg organisiert und die Stripe-Set-Datenträgergruppen gespiegelt werden. RAID 10 bietet die gleiche Fehlertoleranz wie RAID 1 mit höherer Lese-/Schreibgeschwindigkeit über einen einzelnen RAID 1-Datenträger oder -Laufwerk hinweg. Für die RAID-Stufe 10 müssen mindestens vier Platten implementiert werden.
