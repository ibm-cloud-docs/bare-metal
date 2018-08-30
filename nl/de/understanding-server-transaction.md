---
copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Eine Servertransaktion verstehen

Wenn ein Server unter {{site.data.keyword.Bluemix_short}} bereitgestellt, ein Betriebssystem geladen oder Software installiert wird, wird eine *Transaktion* ausgeführt.  Eine Transaktion ist eine automatisierte Reihe von Schritten, die von den {{site.data.keyword.Bluemix_notm}}-Managementsystemen zum Konfigurieren von Kundenservern ausgeführt werden. 

Wenn einer Ihrer Server sich in einer Transaktion befindet, wird in den Servernotizen in den Hardwarelisten ein Link angezeigt. Sie können auf diesen Link klicken, um anzuzeigen, welche Transaktionen für diesen Server anstehen.  Anschließend wird eine Tabelle angezeigt, in der Daten für die aktuelle Transaktion aufgelistet werden, die gerade in Bearbeitung ist. 

* **ID** ist die interne Transaktions-ID.  Wenn Sie ein Ticket zur Transaktion senden, fügen Sie diese Nummer hinzu.
* **Gruppe** ist eine kurze Beschreibung des Transaktionstyps.  Beispiel: *Erneutes Laden des MS-Betriebssystems* bedeutet, dass ein Microsoft-Betriebssystem auf der Maschine neu geladen wird.
* **Aktueller Status** ist der Name für den aktuellen Transaktionsschritt.  Beispiel: *INSTALL_OS* ist ein Transaktionsschritt für *Erneutes Laden des MS-Betriebssystems*, der bedeutet, dass auf der Maschine Windows installiert wird.
* **Abgelaufene Zeit und durchschnittliche Zeit** gehören zusammen.  Die abgelaufene Zeit stellt dar, wie lange der aktuelle Transaktionsschritt bereits ausgeführt wird.  Die durchschnittliche Zeit gibt an, wie lange dieser Schritt im Durchschnitt dauert.  Wenn die abgelaufene Zeit wesentlich länger als die durchschnittliche Zeit ist, kann es sinnvoll sein, ein Support-Ticket für den Status zu öffnen. 
