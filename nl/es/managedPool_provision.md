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

# Suministro de agrupaciones gestionadas por el cliente
{: #bm-provision-managed-pools}

Para suministrar una agrupación de servidores gestionados por el cliente, póngase en contacto con IBM directamente: [Obtención de ayuda y soporte](/docs/bare-metal?topic=bare-metal-gettinghelp).

Proporcione la siguiente información:
* El centro de datos en el que desea que se coloquen las agrupaciones gestionadas. (Todos los servidores de una agrupación gestionada deben estar ubicados en el mismo centro de datos).
* El número de servidores que desea en la agrupación gestionada
* Las especificaciones que necesita para los servidores agrupados

Una vez creada la agrupación, IBM le proporciona los siguientes valores de parámetros. Necesitará estos valores cuando envíe el mandato de API para gestionar la agrupación.
* poolKeyName
* backendRouter

## Solicitud de servidores desde la agrupación gestionada
{: #bm-order-server-managed-pool}
Utilice el proceso de suministro estándar para solicitar servidores en la agrupación. Su pedido se ha realizado desde la agrupación y la agrupación se repone con el número de servidores que ha solicitado.

## Pasos siguientes

Después de suministrar la agrupación gestionada por el cliente y de solicitar servidores desde la agrupación gestionada, puede gestionar el número de servidores de la agrupación. Consulte [Especificación del número de servidores en la agrupación gestionada por el cliente](/docs/bare-metal?topic=bare-metal-set-amount-servers-pool#set-amount-servers-pool)
