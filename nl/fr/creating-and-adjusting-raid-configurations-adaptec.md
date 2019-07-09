---

copyright:
  years: 2017, 2019
lastupdated: "2018-07-10"

keywords: raid, adaptec, ipmi, raid bios, raid array, RAID configuration

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Création et ajustement des configurations RAID d'Adaptec
{: #bm-create-raid-config}

Le système BIOS de la technologie RAID d'Adaptec vous permet de configurer et gérer votre configuration RAID. Servez-vous de ce système BIOS si vous utilisez notre option [No OS](/docs/bare-metal?topic=bare-metal-the-no-os-option) et que vous souhaitez configurer une configuration d'unité spécifique.

## Accès à l'unité IPMI pour interagir avec le système BIOS de la technologie RAID
{: #bm-access-ipmi}

Que votre machine soit dotée d'un contrôleur Adaptec ou d'un contrôleur LSI, vous devez accéder au serveur utilisant IPMI pour pouvoir interagir avec le système BIOS de la technologie RAID. Pour interagir avec IPMI, vous devez d'abord vous connecter au réseau privé virtuel {{site.data.keyword.cloud}} d'Adaptec.
1. Connectez-vous au réseau privé virtuel via [SSL](/docs/infrastructure/iaas-vpn?topic=VPN-setup-ssl-vpn-connections#setup-ssl-vpn-connections) ou PPTP.
* Accédez à la liste des unités dans le portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/){: new_window}. Voir [Accès à la liste des unités](/docs/infrastructure/vsi?topic=virtual-servers-managing-virtual-servers).
* Cliquez sur l'unité à laquelle vous souhaitez accéder.
* Sélectionnez l'onglet Gestion à distance pour trouver les détails d'accès du système IPMI de votre serveur.
* Placez l'adresse IP de votre unité IPMI dans le navigateur et connectez-vous.
* Pour commencer à interagir avec la contrôle à distance, cliquez sur **Remote Control > Console Redirection**.

## Création de grappes RAID
{: #bm-create-raid-array}

Durant le processus de démarrage, appuyez sur les touches **Ctrl+A** pour accéder au BIOS RAID.

Pour commencer la configuration de RAID, ouvrez la configuration d'unité logique (Logical Device Configuration, première option). Cette option analyse la topologie de vos unités et affiche un menu dans lequel vous pouvez gérer des grappes, créer des grappes et exécuter d'autres tâches d'administration d'unité.

L'exemple ci-après montre comment créer une grappe. La liste des unités disponibles que vous pouvez utiliser pour créer votre grappe RAID s'affiche.

1. Pour sélectionner les unités, appuyez sur la barre d'espacement afin de renseigner la zone *Selected Drives*.
* Après avoir sélectionné toutes les unités à utiliser dans votre grappe, appuyez sur Entrée pour accéder à l'étape de configuration RAID.
* Choisissez le type de technologie RAID à utiliser. Si vous avez besoin d'aide pour déterminer quelle configuration RAID correspond le mieux à vos besoins, reportez-vous à la [foire aux questions d'Adaptec ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm){: new_window}.
* Indiquez un intitulé de grappe durant la configuration. Une bonne pratique consiste à inclure le type de technologie RAID dans l'intitulé (par exemple, RAID10-A).
* Appuyez sur la touche **Entrée** pour accéder aux autres paramètres. Utilisez les valeurs par défaut.

Une fois la configuration terminée, sélectionnez Done ; la grappe RAID est créée. Vous pouvez voir la nouvelle grappe en sélectionnant 'Manage Arrays' dans le menu principal. Pour quitter l'utilitaire de configuration, appuyez sur la touche d'échappement jusqu'à ce que vous soyez invité à quitter le système BIOS Adaptec.

## Retrait des grappes RAID existantes 
{: #bm-remove-raid-array}

Si vous devez retirer une grappe existante, accédez à **Manage Arrays**, sélectionnez la grappe à retirer, appuyez sur **Supprimer** et confirmer.

## Exemples de configuration
{: #bm-example-config}

1. Sur un serveur comprenant au total six unités, vous pouvez configurer jusqu'à deux unités SSD sur une grappe RAID 0 pour votre système d'exploitation, et quatre unités supplémentaires sur une grappe RAID 10 pour vos données réelles. Cette configuration vous permet de recharger rapidement le système d'exploitation du serveur sans devoir restaurer vos données de site ou de service si elles se trouvent sur la grappe secondaire.

* Sur un serveur cPanel, les répertoires /var et /home peuvent se trouver dans des grappes RAID SSD distinctes. Comme il s'agit des deux répertoires utilisant le plus d'entrées-sorties sur un serveur cPanel, vous pouvez potentiellement réduire les temps de réponse du site avec les paramètres suivants :
  * RAID0 (2 unités SATA) - /
  * RAID0 (2 unités SSD) - /var
  * RAID0 (2 unités SSD) - /home
  * RAID10 (4 unités SATA) - /backup

* Utilisez une seule grappe RAID pour configurer des partitions logiques multiples. Utilisez, par exemple, deux unités de 4 To configurées sur une grappe RAID 1. Vous pouvez partitionner la grappe RAID en fonction de vos besoins. Exemple :
  * Partition principale de 100 Go pour votre système d'exploitation
  * Partition secondaire de 500 Go pour vos données
  * Troisième partition de l'espace restant pour les sauvegardes
