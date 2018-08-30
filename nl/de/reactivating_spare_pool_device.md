---



copyright:
  years: 2014, 2018
lastupdated: "2018-02-01"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Einheit aus dem Ersatzpool reaktivieren 
{: #reactivating-spare-pools}

Wenn eine Einheit zum Ersatzpool hinzugefügt wird, ändert sich ihr Status in der Einheitenliste von "Aktiv" (gibt an, dass die Einheit für Standardinteraktionen infrage kommt) in "Ersatzpool". Einheiten, die Bestandteil des Ersatzpools sind, sind dieser Funktion zugeordnet und können nicht wie andere Einheiten für normale alltägliche Aktionen verwendet werden. Um eine Einheit aus dem Ersatzpool zu entfernen, sodass sie zur ihrer normalen Funktion zurückkehren kann, muss sie reaktiviert werden. Führen Sie die folgenden Schritte aus, um eine Einheit zu reaktivieren.
{:shortdesc}

## Einheit aus dem Ersatzpool reaktivieren 

1. Greifen Sie mit Ihren eindeutigen Berechtigungsnachweisen auf das [{{site.data.keyword.slportal_full}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window} zu. 
2. Wählen Sie in der Navigationsleiste **Einheiten > Ersatzpool** aus, um auf die Anzeige *Ersatzpool* zuzugreifen. 
3. Wählen Sie **Aktionen > Einheit reaktivieren** für die gewünschte Einheit aus. 
4. Klicken Sie auf **Ja**, um den Server zu reaktivieren. Klicken Sie auf **Nein**, um die Aktion abzubrechen. 

## Nächste Schritte
Nachdem der Reaktivierungsprozess eingeleitet wurde, wird die Einheit offline geschaltet, die Firmware aktualisiert und die Einheit für die normale Verwendung zur Verfügung gestellt. Der Reaktivierungsprozess dauert etwa eine Stunde. Einheiten, die aus dem Ersatzpool entfernt werden, können nicht mehr für das Failover verwendet werden. Die Einheit kann jederzeit wieder zum Ersatzpool zurückkehren, indem sie erneut zum Ersatzpool hinzugefügt wird. Weitere Informationen finden Sie unter [Einheit zum Ersatzpool hinzufügen](../vsi/adding_spare_pool.html). 
