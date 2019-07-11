---

copyright:
  years:  2019
lastupdated: "2018-05-15"

keywords: number servers managed pool, managed pool

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Anzahl der Server in Ihrem vom Kunden verwalteten Pool angeben
{: #set-amount-servers-pool}

Legen Sie die Anzahl der Server in Ihrem verwalteten Pool mithilfe des folgenden API-Aufrufs fest:

|API-Aufruf|Parameter|Beschreibung|
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank">setManagedPoolQuantity</a>|poolKeyName|Schlüsselname, der Ihren Pool angibt. Diesen Wert stellt IBM Ihnen zur Verfügung.|
|  | backendRouter | Gibt den Back-End-Router für Ihren Pool an. Diesen Wert stellt IBM Ihnen zur Verfügung.|
|  | quantity | Die Gesamtzahl der Server, die in Ihrem Pool enthalten sein sollen.<br><br>Wenn die aktuelle Anzahl der Server in Ihrem Pool kleiner als der hier angegebene Wert ist, werden Server hinzugefügt.<br>Wenn die aktuelle Anzahl der Server in Ihrem Pool größer als der hier angegebene Wert ist, werden Server entfernt.|
