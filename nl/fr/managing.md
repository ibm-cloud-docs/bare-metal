---


copyright:

  years: 2016, 2018
lastupdated: "2018-04-02"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Gestion des serveurs bare metal
{: #managing}


Vous pouvez arrêter, démarrer, redémarrer et annuler des serveurs.
{:shortdesc}

## Réplication d'une instance de serveur
Vous pouvez copier ou cloner une instance de serveur bare metal afin de répliquer la configuration du serveur et obtenir rapidement un nouveau serveur opérationnel.
{:shortdesc}

Pour cloner l'instance :
 1. Accédez au menu et sélectionnez **Configure Replica**. Toutes les configurations sont copiées. Aucune donnée ni aucun contenu n'est copié.
 2. Entrez un nom de serveur unique.
 3. Spécifiez le nom du domaine.

## Rechargement du système d'exploitation
Il peut arriver que vous souhaitiez recharger le système d'exploitation sur votre serveur.
{:shortdesc}

Pour recharger le système d'exploitation :
 1. Sauvegardez toutes les données avant de commencer. Si vous ignorez cette étape, toutes les données existantes sont perdues et ne peuvent pas être récupérées. 
 2. Accédez au menu et sélectionnez **Rechargement du système d'exploitation**. Vous pouvez sélectionner l'une des options suivantes : 
  * Remplacer le système d'exploitation par un autre et recommencer avec de nouvelles configurations.
  * Conserver le système d'exploitation existant avec les configurations en cours, mais réinitialiser le serveur pour recommencer.

Au cours du rechargement du système d'exploitation, le serveur est déconnecté et non disponible. La durée de l'opération de rechargement varie en fonction de la capacité et du système d'exploitation du serveur. Si vous avez défini un script de mise à disposition, toutes les configurations seront restaurées une fois l'opération de rechargement terminée. Si vos données ont été sauvegardées avant l'opération de rechargement du système d'exploitation, vous pourrez les télécharger sur le serveur lorsque ce dernier sera disponible.

## Suppression d'une instance de serveur
Vous pouvez à tout moment supprimer l'instance de serveur bare metal si vous n'en avez plus besoin et ne souhaitez pas être facturé pour cette instance.
{:shortdesc}

Pour supprimer l'instance, accédez au menu et sélectionnez **Cancel Server**.

## Mise hors tension d'un serveur
Vous pouvez créer un serveur à l'avance pour vous préparer à l'utiliser. Une fois le serveur créé, mettez-le hors tension afin que rien ne soit modifié sur ce serveur et que personne ne puisse y accéder. Lorsque vous êtes prêt, vous pouvez mettre le serveur sous tension et être en mesure de l'utiliser en quelques minutes.
{:shortdesc}

Pour mettre le serveur hors tension, accédez au menu et sélectionnez **Power On/Off**. Même si le serveur est hors tension, vous serez tout de même facturé. 

**Remarque :** si le serveur est hors tension, il conserve cet état et vous devez manuellement le mettre sous tension. 
