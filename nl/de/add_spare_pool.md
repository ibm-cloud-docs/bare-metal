---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

keywords: bare metal, spare pools

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Ersatzpools hinzufügen
{: #adding-spare-pools}

Ersatzpools sind eine Form des Bereithaltens bestimmter Einheiten, die als Ersatz vorgesehen sind und den Workflow einer primären Einheit übernehmen oder als neue Einheit in der Kundenflotte dienen können. Damit eine Einheit als Ersatzeinheit definiert werden kann, muss sie zum Ersatzpool hinzugefügt und einer primären Einheit zugeordnet werden. Führen Sie die folgenden Schritte aus, um eine Einheit zum Ersatzpool hinzuzufügen.
{:shortdesc}

1. Greifen Sie mit Ihren eindeutigen Berechtigungsnachweisen auf die [{{site.data.keyword.cloud}}-Konsole ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/){: new_window} zu.
2. Wählen Sie in der Navigationsleiste **Einheiten > Ersatzpool** aus, um auf die Anzeige *Ersatzpool* zuzugreifen.
3. Klicken Sie auf den Link **Zu Ersatzpool hinzufügen**.

   Eine Liste der Einheiten, die zum Hinzufügen zum Ersatzpool infrage kommen, wird gefüllt.
   {:tip}

4. Wählen Sie die Einheiten aus, die zum Ersatzpool hinzugefügt werden sollen.
5. Klicken Sie auf **Ausgewählte Einheiten hinzufügen**.
6. Klicken Sie auf **Bestätigen**, um diese Einheiten zum Ersatzpool hinzuzufügen.

## Nächste Schritte
Nachdem die Übertragung einer Einheit in den Ersatzpool eingeleitet wurde, wird die Einheit innerhalb einer Stunde in den Ersatzpool überführt. Wenn die Einheit im Ersatzpool aktiv ist, wird sie in der Anzeige für Ersatzpool angezeigt und kann als Hot-Spare-Einheit für eine primäre Einheit definiert werden.
