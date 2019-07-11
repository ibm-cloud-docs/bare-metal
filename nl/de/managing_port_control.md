---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-18"

keywords: manage bare metal port control

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Portsteuerung für eine Einheit verwalten
{: #bm-manage-port-control}

Jede Einheit, die einem Konto zugeordnet ist, verfügt über zwei Netzports, die eingehenden Datenverkehr empfangen - einen für öffentlichen Netzverkehr und einen für privaten Netzverkehr. Sie können diese Ports jederzeit aktivieren oder inaktivieren, um den Netzverkehr zu steuern, den eine Einheit empfängt. Führen Sie die folgenden Schritte aus, um die Portsteuerungseinstellungen für eine Einheit zu aktualisieren.

## Vorbereitungen
* Navigieren Sie zum Einheitenmenü Ihrer Konsole. Weitere Informationen finden Sie unter [Zu Einheiten navigieren](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Stellen Sie sicher, dass Sie über die erforderlichen Berechtigungen für das Konto und den Gerätezugriff verfügen. Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** für die klassische Infrastruktur kann die Berechtigungen anpassen.

Weitere Informationen zu Berechtigungen finden Sie unter [Berechtigungen für die klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Gerätezugriff verwalten](/docs/bare-metal?topic=virtual-servers-managing-device-access).

## Portsteuerung für eine Einheit verwalten

1. Greifen Sie auf die **Einheitenliste** zu und wählen Sie den Namen der **Einheit** aus, die aktualisiert werden soll.  
2. Klicken Sie auf die Dropdown-Liste **Aktionen** für die Einheit.
3. Wählen Sie **Portsteuerung** aus.
4. Aktualisieren Sie die Dropdown-Felder *Öffentliches Netz* und/oder *Privates Netz*, indem Sie eine der folgenden Aktionen ausführen:
   * Wählen Sie die gewünschte Geschwindigkeit aus, um den Netzzugriff zu aktivieren.
   * Wählen Sie "Getrennt" aus, um den Netzzugriff zu inaktivieren.
5. Klicken Sie auf die Schaltfläche "Aktualisieren".
6. Klicken Sie auf die Schaltfläche "Schließen", um das Fenster zu schließen.

## Nächste Schritte

Wenn Sie **Inaktiviert** ausgewählt haben, besteht für die Einheitenschnittstelle kein Netzzugriff mehr auf den inaktivierten Port. Wenn Sie **Aktiviert** ausgewählt haben, ist Netzzugriff für den aktivierten Port verfügbar. Die ausgewählte Einstellung für die Portsteuerung bleibt so lange in Kraft, bis sie manuell geändert wird.
