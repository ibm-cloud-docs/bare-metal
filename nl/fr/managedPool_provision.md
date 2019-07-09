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

# Mise à disposition de pools gérés par le client
{: #bm-provision-managed-pools}

Pour mettre à disposition un pool de serveur géré par le client, contactez directement IBM : [Aide et assistance](/docs/bare-metal?topic=bare-metal-gettinghelp).

Fournissez les informations suivantes :
* Centre de données dans lequel vous souhaitez localiser vos pools gérés. (Tous les serveurs d'un pool géré doivent se trouver dans le même centre de données.)
* Nombre de serveurs que doit comporter votre pool géré.
* Spécifications dont vous avez besoin pour vos serveurs en pool.

Une fois votre pool créé, IBM fournit les valeurs de paramètre suivantes. Vous avez besoin de ces valeurs lorsque vous exécutez la commande d'API pour gérer votre pool.
* poolKeyName
* backendRouter

## Commande de serveurs depuis votre pool géré
{: #bm-order-server-managed-pool}
Utilisez le processus standard de mise à disposition pour commander des serveurs dans votre pool. Votre commande est honorée depuis votre pool et celui-ci est réapprovisionné du nombre de serveurs que vous avez commandés.

## Etapes suivantes

Une fois votre pool géré par client mis à disposition et la commande de serveurs depuis le pool effectuée, vous pouvez gérer le nombre de serveurs de votre pool. Voir [Spécification du nombre de serveurs dans votre pool géré par client](/docs/bare-metal?topic=bare-metal-set-amount-servers-pool#set-amount-servers-pool)
