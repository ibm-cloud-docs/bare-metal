---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-18"

keywords: manage bare metal port control

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Gestion du contrôle de port pour une unité
{: #bm-manage-port-control}

Chaque unité qui est associée à un compte possède deux ports réseau recevant le trafic entrant : un pour le trafic réseau public et un pour le trafic réseau privé. Vous pouvez activer ou désactiver ces ports à tout moment afin de contrôler le trafic réseau reçu par une unité. Exécutez la procédure suivante pour mettre à jour les paramètre de contrôle de port pour une unité.

## Avant de commencer
* Accédez au menu de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Vérifiez que vous disposez des autorisations de compte nécessaires et que vous avez accès à l'unité. Seul le propriétaire du compte, ou un utilisateur avec l'autorisation **Gérer les utilisateurs** de l'infrastructure classique, peut régler les autorisations.

Pour plus d'informations sur les autorisations, voir [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#infrapermission) et [Gestion de l'accès aux terminaux](/docs/bare-metal?topic=virtual-servers-managing-device-access).

## Gestion du contrôle de port pour une unité

1. Accédez à **Liste des unités** et sélectionnez le **Nom de l'unité** à mettre à jour.  
2. Cliquez sur la liste déroulante **Actions** de l'unité.
3. Sélectionnez **Contrôle de port**.
4. Mettez à jour la zone déroulante *Réseau public* et/ou *Réseau privé* en effectuant l'une des actions suivantes :
   * Sélectionnez la vitesse souhaitée pour activer l'accès réseau.
   * Sélectionnez Déconnecté(e) pour désactiver l'accès réseau.
5. Cliquez sur le bouton Mettre à jour.
6. Cliquez sur le bouton Fermer pour fermer la fenêtre.

## Etapes suivantes

Si vous avez sélectionné **Déconnecté(e)**, l'accès réseau du port désactivé est interrompu pour l'interface d'unité. Si vous avez sélectionné **Activé(e)**, l'accès réseau est disponible pour le port activé. Le contrôle de port reste dans le paramètre sélectionné tant qu'il n'est pas changé manuellement.
