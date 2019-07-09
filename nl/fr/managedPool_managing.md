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

# Spécification du nombre de serveurs dans votre pool géré par client
{: #set-amount-servers-pool}

Définissez le nombre de serveurs de votre pool géré en utilisant l'appel d'API suivant :

|Appel API|Paramètres|Description|
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank">Set managed pool quantity</a> (définir la quantité de pool géré)|poolKeyName|Nom de clé identifiant votre pool. IBM fournit cette valeur.|
|  | backendRouter | Identifie le routeur de back end pour votre pool. IBM fournit cette valeur.|
|  | quantité | Nombre total de serveurs souhaité pour votre pool.<br><br>Si le nombre actuel de serveurs dans votre pool est inférieur à la valeur que vous fournissez ici, des serveurs sont ajoutés.<br>Si le nombre actuel de serveurs dans votre pool est supérieur à la valeur que vous fournissez ici, des serveurs sont supprimés.|
