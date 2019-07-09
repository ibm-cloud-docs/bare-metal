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

# Specifica del numero di server nel tuo pool gestito dal cliente
{: #set-amount-servers-pool}

Imposta il numero di server nel tuo pool gestito utilizzando la seguente chiamata API:

|Chiamata API|Parametri|Descrizione|
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank">Imposta la quantità di pool gestiti</a>|poolKeyName|Nome chiave che identifica il tuo pool. IBM ti fornisce questo valore.|
|  | backendRouter | Identifica il router di backend per il tuo pool. IBM ti fornisce questo valore.|
|  | quantity | Il numero totale di server che vuoi nel tuo pool.<br><br>Se il numero corrente di server nel tuo pool è inferiore al valore che fornisci qui, i server vengono aggiunti.<br>Se il numero corrente di server nel tuo pool è superiore al valore che fornisci qui, i server vengono rimossi.|
