---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

keywords: set up bare metal server

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Configuration d'un serveur bare metal
{: #bm-set-up}

Vous pouvez configurer un serveur bare metal en tant que serveur dédié.
{:shortdesc}

## Avant de commencer
* Accédez au menu de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Vérifiez que vous disposez des autorisations de compte nécessaires et que vous avez accès à l'unité. Seul le propriétaire du compte, ou un utilisateur avec l'autorisation **Gérer les utilisateurs** de l'infrastructure classique, peut régler les autorisations.

Pour plus d'informations sur les autorisations, voir [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#infrapermission) et [Gestion de l'accès aux terminaux](/docs/bare-metal?topic=virtual-servers-managing-device-access).

## Configuration d'un serveur bare metal

Pour configurer un serveur bare metal, procédez comme suit :

1. Dans le menu, cliquez sur **Unités** > **Liste des unités** et recherchez votre système. Toutes vos unités sont indiquées dans la Liste des unités, qui vous permet de gérer et de mettre à niveau vos unités ou de générer des diagrammes liés à l'utilisation de la bande passante.

2. Choisissez de gérer votre serveur de l'une des façons suivantes :
  * Cliquez sur la flèche située sous Nom de l'unité pour afficher un récapitulatif de vos unités dans la vue Instantané et pour les gérer.
  * Cliquez sur le nom d'unité du serveur pour afficher une liste détaillée et gérer vos unités à partir de l'écran Détails de l'unité.

3. Enregistrez l'adresse IP et les données d'identification du serveur dans un emplacement sécurisé afin de pouvoir accéder rapidement à ces données sans avoir besoin de vous connecter à chaque fois au portail client. Vous pouvez enregistrer ces détails pour une unité individuelle et toutes les unités associées avec votre compte :
  * Affichez les adresses IP d'unité individuelles à partir de la Liste des unités.
  * Affichez les mots de passe racine de l'unité individuelle dans la vue Instantané de l'unité.
  * Affichez plusieurs adresses IP d'unité à l'aide de l'option **Télécharger CSV** de la **Liste des unités**. Sélectionnez ensuite **Télécharger CSV** dans **Paramètres** pour télécharger la liste complète des unités et des détails au format d'une feuille de calcul.

4. Mettez à jour les données d'identification des systèmes d'exploitation et des autres logiciels. Des données d'identification temporaires ont été affectées à tous les logiciels qui ont été chargés sur votre unité lors du processus de mise à disposition. Vous pouvez afficher et gérer ces données d'identification sur l'onglet Mots de passe de chaque unité du portail client. Utilisez ces données d'identification temporaires pour accéder à votre logiciel pour la première fois. Modifiez ensuite le mot de passe de votre logiciel en suivant les pratiques de mots de passe fiables. Le mot de passe créé doit être formé d'une combinaison de lettres, de numéros et de symboles. Vous pouvez éventuellement stocker les mises à jour de mot de passe sous l'onglet Mots de passe pour chaque appareil. Cependant, lorsque vous stockez des mots de passe dans le portail client, toute personne ayant accès au compte et disposant des droits appropriés peut visualiser les mots de passe qui sont stockés sur l'écran Mots de passe.

5. Accédez à votre serveur sur le réseau privé. Vous pouvez utiliser le réseau privé d'infrastructure {{site.data.keyword.cloud_notm}} pour interagir avec vos unités par l'intermédiaire de RDP (Remote Desktop Protocol) via SSH et KVM sur IP. Vous pouvez utiliser l'outil VPN Access pour établir une connexion de réseau privé vers le noeud final VPN SSL le plus proche ou le noeud final de votre choix. L'accès VPN est également requis si vous souhaitez interagir avec plusieurs services. Pour accéder au réseau privé, éditez l'accès VPN de l'utilisateur à partir de la Liste utilisateurs. Pour accéder à la Liste utilisateurs, cliquez sur **Compte** > **Utilisateurs** > **Liste utilisateurs**. Accédez à la page [Virtual Private Network ![Icône de lien externe](../icons/launch-glyph.svg)](https://www.softlayer.com/VPN-Access){:new_window} pour vous connecter à l'une des options VPN.

6. Configurez la surveillance pour vérifier le statut de votre serveur et savoir quand vous devez le faire évoluer. Vous pouvez utiliser des services de surveillance standard ou Nimsoft. Vous pouvez employer la surveillance standard, ou de base, dans la méthode ping-avec-réponse en utilisant un ping avec réponse lente ou un ping de service à partir du portail client. Vous pouvez également faire appel à la surveillance Nimsoft, ou avancée, à partir du portail client ou dans 1 des 3 niveaux suivants : de base, avancé et premium.

7. Sécurisez votre système. Utilisez les pare-feux matériels disponibles pour sécuriser votre unité. Vous pouvez mettre à disposition des pare-feux matériels à la demande sans temps d'indisponibilité si des règles sont correctement établies afin de protéger votre serveur contre toute activité indésirable. Après avoir commandé votre pare-feu, vous devez l'activer et définir des règles.

8. Planifiez des sauvegardes pour vous assurer que vos données sont stockées en toute sécurité en dehors de votre unité et que vous pouvez les recharger en cas de perte de données. Vous pouvez choisir l'un des services de sauvegarde suivants pour stocker vos données dans un emplacement sécurisé :
  * IBM Cloud Backup est un système de sauvegarde automatique basé sur un agent. IBM Cloud Backup est une solution clé en main de gestion de votre unité. Elle est compatible avec les logiciels Microsoft tels qu'Exchange et SQL via des plug-ins additionnels. Les utilisateurs d'IBM Cloud Backup interagissent avec ce service via l'application Web WebCC d'IBM Cloud Backup.
  * R1Soft Continuous Data Protection (CDP) peut être installé sur votre serveur ou sur une machine virtuelle auto-gérée. Il est recommandé si vous souhaitez disposer d'une seule interface pour gérer toutes vos sauvegardes. Vous interagissez avec R1Soft CDP via votre système de gestion propriétaire qui permet d'installer des agents sur des machines virtuelles et offre des plug-in de base de données pour plus de fonctionnalité.
