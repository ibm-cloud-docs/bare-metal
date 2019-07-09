---

copyright:
  years:  2019
lastupdated: "2018-05-15"

keywrods: bare metal, managed pools

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# A propos des pools gérés par client
{: #bm-customer-managed-pools}

Les pools gérés par client vous donnent accès à un ensemble de serveurs toujours disponibles pour votre organisation. Ces serveurs sont configurés en fonction de vos spécifications. Vous pouvez commander des serveurs du pool lorsque vous en avez besoin.

Cette fonction est idéale si votre organisation a fréquemment besoin de mettre à disposition un grand nombre de serveurs pour une utilisation pendant les périodes de forte activité. Elle vous permet d'utiliser uniquement le nombre minimum de serveurs dont vous avez besoin tout en disposant toujours d'un ensemble important de serveurs disponibles pour répondre à des besoins supplémentaires.

## Exemple d'utilisation
{: #bm-managed-pools-use-case}

La société utilise 1000 serveurs actifs pour ses opérations quotidiennes. Toutefois, aux heures pleines, jusqu'à 500 serveurs supplémentaires peuvent être nécessaires. Ces serveurs doivent être opérationnels rapidement.

Pour répondre à ses besoins, la société A contacte IBM afin de configurer un pool de serveurs géré. Une fois le pool configuré, elle lance un appel API pour définir le nombre de serveurs du pool sur 500.

En juillet, la société A a besoin de 250 serveurs supplémentaires provenant du pool. Elle commande 250 serveurs. Cette commande est rapidement remplie à partir du pool. Une fois la commande terminée, 250 serveurs sont ajoutés au pool géré de la société A afin que 500 serveurs soient toujours disponibles.


## Etapes suivantes

Si votre organisation souhaite utiliser un pool géré par le client, voir [Mise à disposition de pools gérés par le client](/bare-metal?topic=bare-metal-provisioning-customer-managed-pools)
