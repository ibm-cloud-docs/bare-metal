---

copyright:
  years:  2018
lastupdated: "2018-05-15"

---

# Spécification du nombre de serveurs dans votre pool géré par client

Définissez le nombre de serveurs de votre pool géré en utilisant l'appel d'API suivant :

|Appel API|Paramètres|Description|
|---|---|---|
|<a href="https://softlayer.github.io/reference/services/SoftLayer_Account/setManagedPoolQuantity/" target="_blank">Set managed pool quantity</a> (définir la quantité de pool géré)|poolKeyName|Nom de clé identifiant votre pool. IBM fournit cette valeur.|
|  | backendRouter | Identifie le routeur de back end pour votre pool. IBM fournit cette valeur.|
|  | quantité | Nombre total de serveurs souhaité pour votre pool.<br><br>Si le nombre actuel de serveurs dans votre pool est inférieur à la valeur indiquée ici, des serveurs sont ajoutés. <br>Si le nombre actuel de serveurs dans votre pool est supérieur à la valeur indiquée ici, des serveurs sont retirés. |
