---

copyright:
  years:  2018
lastupdated: "2018-05-15"

---

# Specifica del numero di server nel tuo pool gestito dal cliente

Imposta il numero di server nel tuo pool gestito utilizzando la seguente chiamata API:

|Chiamata API|Parametri|Descrizione|
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank">Imposta la quantità del pool gestito</a>|poolKeyName|Nome chiave che identifica il tuo pool. IBM fornisce questo valore per tuo conto.|
|  | backendRouter | Identifica il router di backend per il tuo pool. IBM fornisce questo valore per tuo conto.|
|  | quantity | Il numero totale di server che desideri nel pool.<br><br>Se il numero corrente di server nel tuo pool è inferiore al valore da te qui fornito, vengono aggiunti dei server. <br>Se il numero corrente di server nel tuo pool è superiore al valore da te qui fornito, vengono rimossi dei server. |
