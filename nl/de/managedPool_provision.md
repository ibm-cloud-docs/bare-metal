---

copyright:
  years:  2019
lastupdated: "2019-02-01"

keywrods: provision managed pool, managed pools

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Vom Kunden verwaltete Pools bereitstellen
{: #bm-provision-managed-pools}

Zur Bereitstellung eines vom Kunden verwalteten Pools von Servern wenden Sie sich direkt an IBM: [Hilfe und Unterstützung anfordern](/docs/bare-metal?topic=bare-metal-gettinghelp).

Geben Sie die folgenden Informationen an:
* Das Rechenzentrum, in dem Ihre verwalteten Pools sich befinden sollen. (Alle Server in einem verwalteten Pool müssen sich in demselben Rechenzentrum befinden.)
* Die Anzahl der Server, die in Ihrem verwalteten Pool vorhanden sein sollen.
* Die Spezifikationen, die Sie für Ihre in einem Pool zusammengefassten Server benötigen.

Nachdem Ihr Pool erstellt wurde, stellt IBM Ihnen die folgenden Parameterwerte bereit. Sie benötigen diese Werte, wenn Sie den API-Befehl zum Verwalten des Pools senden.
* poolKeyName
* backendRouter

## Server aus Ihrem verwalteten Pool bestellen
{: #bm-order-server-managed-pool}
Verwenden Sie den Standardbereitstellungsprozess, um Server aus Ihrem Pool zu bestellen. Sie erhalten die bestellten Server aus Ihrem Pool und Ihr Pool wird mit der Anzahl der Server, die Sie bestellt haben, wieder aufgefüllt.

## Nächste Schritte

Nachdem Sie Ihren vom Kunden verwalteten Pool bereitgestellt und Server aus Ihrem verwalteten Pool bestellt haben, können Sie die Anzahl der Server in Ihrem Pool verwalten. Siehe [Anzahl der Server in Ihrem vom Kunden verwalteten Pool angeben](/docs/bare-metal?topic=bare-metal-set-amount-servers-pool#set-amount-servers-pool).
