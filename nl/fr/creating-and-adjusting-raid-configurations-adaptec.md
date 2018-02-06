---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Création et ajustement des configurations RAID d'Adaptec

Le système BIOS de la technologie RAID d'Adaptec vous permet de configurer et gérer votre configuration RAID. Servez-vous de ce système BIOS si vous utilisez notre option [No OS](introduction-no-os.html) et que vous souhaitez configurer une configuration d'unité spécifique. 

## Accès à l'unité IPMI pour interagir avec le système BIOS de la technologie RAID

Que votre machine soit dotée d'un contrôleur Adaptec ou d'un contrôleur LSI, vous devrez accéder au serveur à l'aide d'IPMI afin de pouvoir interagir avec le système BIOS de la technologie RAID. Afin d'interagir avec IPMI, vous devrez d'abord vous connecter au réseau privé virtuel {{site.data.keyword.IBM&reg; Cloud}} d'Adaptec. 
1. Connectez-vous au réseau privé virtuel via [SSL](/infrastructure/vpn/ssl-vpn-connections.html) ou PPTP. Voir la[page contenant la rubrique sur le réseau privé virtuel](/infrastructure/vpn/index.html).
* Accédez à la liste des unités dans le [portail client](https://control.softlayer.com/). Voir [Accès à la liste des unités](/vsi/vsi_managing.html).
* Cliquez sur l'unité à laquelle vous souhaitez accéder. 
* Sélectionnez l'onglet Gestion à distance pour trouver les détails d'accès du système IPMI à vos serveurs. 
* Placez l'adresse IP de votre unité IPMI dans le navigateur et connectez-vous. 
* Pour commencer à interagir avec la contrôle à distance, cliquez sur Remote Control > Console Redirection. 

## Création de grappes RAID

Durant le processus d'amorçage, appuyez sur Ctrl+A pour accéder au système BIOS de la technologie RAID. 

Pour commencer à configurer votre technologie RAID, sélectionnez Logical Device Configuration (première option). Cette option analyse la topologie de vos unités et affiche un menu dans lequel vous pouvez gérer des grappes, créer des grappes et exécuter d'autres tâches d'administration d'unité. 

L'exemple ci-après montre comment créer une grappe. La liste des unités disponibles que vous pouvez utiliser pour créer votre grappe RAID s'affiche. 

1. Pour sélectionner les unités, appuyez sur la barre d'espacement afin de remplir la zone *Selected Drives*. 
* Après avoir sélectionné toutes les unités à utiliser dans votre grappe, appuyez sur Entrée pour accéder à l'étape de configuration RAID. 
* Choisissez le type de technologie RAID voulu. Si vous avez besoin d'aide pour déterminer quelle configuration RAID répond le mieux à vos besoins, reportez-vous à la [foire aux questions d'Adaptec](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm).
* Indiquez un intitulé de grappe durant la configuration. Une bonne pratique consiste à inclure le type de technologie RAID dans l'intitulé (par exemple, RAID10-A). 
* Appuyez sur Entrée pour accéder aux autres paramètres. Utilisez les valeurs par défaut. 

Une fois la configuration terminée, sélectionnez Done ; la grappe RAID est créée. Vous pouvez voir la nouvelle grappe que vous venez de créer en sélectionnant 'Manage Arrays' dans le menu principal. Pour quitter l'utilitaire de configuration, appuyez sur la touche d'échappement jusqu'à ce que vous soyez invité à quitter le système BIOS Adaptec. 

## Retrait de grappes existantes

Si vous devez retirer une grappe existante, vous devez accéder à Manage Arrays > Select the Array to remove, appuyer sur Delete et confirmer. 

## Exemples de configuration

1. Sur un serveur comprenant 6 unités au total, vous pouvez configurer 2 unités SSD dans une grappe RAID0 pour votre système d'exploitation et 4 unités supplémentaires dans une grappe RAID10 pour vos données réelles. Cela vous permet de recharger rapidement le système d'exploitation des serveurs sans avoir à restaurer votre site ou vos données de maintenance si elles figurent sur la grappe secondaire. 

* Sur un serveur cPanel, les répertoires /var et /home peuvent se trouver dans des grappes RAID SSD distinctes. Puisqu'il s'agit des 2 répertoires utilisant le plus d'entrées-sorties sur un serveur cPanel, vous pouvez potentiellement réduire les temps de réponse du site avec les paramètres suivants : 
  * RAID0 (2 unités SATA) - /
  * RAID0 (2 unités SSD) - /var
  * RAID0 (2 unités SSD) - /home
  * RAID10 (4 unités SATA) - /backup

* Utilisez une seule grappe RAID pour configurer des partitions logiques multiples. Par exemple, utilisez deux unités de 4 To configurées dans une grappe RAID1. Vous pouvez partitionner la grappe RAID en fonction de vos besoins. Exemple :
  * Partition principale de 100 Go pour votre système d'exploitation
  * Partition secondaire de 500 Go pour vos données
  * Troisième partition de l'espace restant pour les sauvegardes
