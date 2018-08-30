---

copyright:
  years:  2018
lastupdated: "2018-05-15"

---

# Anzahl der Server in Ihrem vom Kunden verwalteten Pool angeben

Legen Sie die Anzahl der Server in Ihrem verwalteten Pool mithilfe des folgenden API-Aufrufs fest: 

|API-Aufruf|Parameter|Beschreibung|
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank">setManagedPoolQuantity</a>|poolKeyName|Schlüsselname, der Ihren Pool angibt. Diesen Wert stellt IBM Ihnen zur Verfügung. |
|  | backendRouter | Gibt den Back-End-Router für Ihren Pool an. Diesen Wert stellt IBM Ihnen zur Verfügung. |
|  | quantity | Die Gesamtzahl der Server, die in Ihrem Pool enthalten sein sollen. <br><br>Wenn die aktuelle Anzahl der Server in Ihrem Pool kleiner als der hier angegebene Wert ist, werden Server hinzugefügt. <br>Wenn die aktuelle Anzahl der Server in Ihrem Pool größer als der hier angegebene Wert ist, werden Server entfernt. |
