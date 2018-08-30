---

copyright:
  years:  2018
lastupdated: "2018-05-15"

---


# Suministro de agrupaciones gestionadas por el cliente

Para suministrar una agrupación de servidores gestionados por el cliente, póngase en contacto con IBM directamente: [Obtención de ayuda y soporte](../bare-metal/get-help-and-support.html).

Proporcione la siguiente información:
* El centro de datos en el que desea que se coloquen las agrupaciones gestionadas. (Todos los servidores de una agrupación gestionada deben estar ubicados en el mismo centro de datos).
* El número de servidores que desea en la agrupación gestionada
* Las especificaciones que necesita para los servidores agrupados

Una vez creada la agrupación, IBM le proporciona los siguientes valores de parámetros. Necesitará estos valores cuando envíe el mandato de API para gestionar la agrupación.
* poolKeyName
* backendRouter

## Solicitud de servidores desde la agrupación gestionada
Utilice el proceso de suministro estándar para solicitar servidores en la agrupación. Su pedido se ha realizado desde la agrupación y la agrupación se repone con el número de servidores que ha solicitado.

## Pasos siguientes

Después de suministrar la agrupación gestionada por el cliente y de solicitar servidores desde la agrupación gestionada, puede gestionar el número de servidores de la agrupación. Consulte [Especificación del número de servidores en la agrupación gestionada por el cliente](../bare-metal/managedPool_managing.html)
