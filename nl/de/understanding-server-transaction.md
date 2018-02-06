---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Eine Servertransaktion verstehen

Wenn ein Server unter {{site.data.keyword.Bluemix_short}} bereitgestellt, ein Betriebssystem geladen oder Software installiert wird, wird eine *Transaktion* ausgeführt. Eine Transaktion ist eine automatisierte Reihe von Schritten, die von den {{site.data.keyword.Bluemix_notm}}-Managementsystemen zum Konfigurieren von Kundenservern ausgeführt werden.

Wenn sich Ihre Server zurzeit in einer Transaktion befindet, wird in den Servernotizen in den Hardwarelisten ein Link angezeigt. Sie können auf diesen Link klicken, um anzuzeigen, welche Transaktionen für diesen Server anstehen. Sie erhalten dann eine Tabelle mit den Daten für die aktuelle Transaktion, die gerade in Bearbeitung ist.

* **ID** ist die interne Transaktions-ID. Wenn Sie ein Ticket zur Transaktion senden, fügen Sie diese Nummer hinzu.
* **Gruppe** ist eine kurze Beschreibung des Transaktionstyps. Beispiel: *Erneutes Laden des MS-Betriebssystems* bedeutet, dass ein Microsoft-Betriebssystem auf der Maschine neu geladen wird.
* **Aktueller Status** ist der Name für den aktuellen Transaktionsschritt. Beispiel: *INSTALL_OS* ist ein Transaktionsschritt für *Erneutes Laden des MS-Betriebssystems*, der bedeutet, dass auf der Maschine Windows installiert wird.
* **Abgelaufene Zeit und durchschnittliche Zeit** gehören zusammen. Die abgelaufene Zeit stellt dar, wie lange der aktuelle Transaktionsschritt bereits ausgeführt wird. Die durchschnittliche Zeit gibt an, wie lange dieser Schritt im Durchschnitt dauert. Wenn die abgelaufene Zeit wesentlich länger als die durchschnittliche Zeit ist, können Sie ein Support-Ticket für den Status öffnen.
