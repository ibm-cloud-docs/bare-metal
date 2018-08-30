---

copyright:
  years:  2018
lastupdated: "2018-05-15"

---


# Mise à disposition de pools gérés par client

Pour mettre à disposition un pool de serveur géré par le client, contactez directement IBM : [Aide et assistance](../bare-metal/get-help-and-support.html).

Fournissez les informations suivantes :
* Centre de données dans lequel vous souhaitez localiser vos pools gérés. (Tous les serveurs d'un pool géré doivent se trouver dans le même centre de données.)
* Nombre de serveurs que doit comporter votre pool géré.
* Spécifications dont vous avez besoin pour vos serveurs en pool.

Une fois votre pool créé, IBM fournit les valeurs de paramètre suivantes. Vous avez besoin de ces valeurs lorsque vous exécutez la commande d'API pour gérer votre pool.
* poolKeyName
* backendRouter

## Commande de serveurs depuis votre pool géré
Utilisez le processus standard de mise à disposition pour commander des serveurs dans votre pool. Votre commande est honorée depuis votre pool et celui-ci est réapprovisionné du nombre de serveurs que vous avez commandés.

## Etapes suivantes

Une fois votre pool géré par client mis à disposition et la commande de serveurs depuis le pool effectuée, vous pouvez gérer le nombre de serveurs de votre pool. Voir [Spécification du nombre de serveurs dans votre pool géré par client](../bare-metal/managedPool_managing.html)
