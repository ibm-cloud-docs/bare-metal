---

copyright:
  years: 2017, 2018
lastupdated: "2018-07-10"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Création et ajustement des configurations RAID d'Adaptec

Le système BIOS de la technologie RAID d'Adaptec vous permet de configurer et gérer votre configuration RAID. Servez-vous de ce système BIOS si vous utilisez notre option [No OS](introduction-no-os.html) et que vous souhaitez configurer une configuration d'unité spécifique. 

## Accès à l'unité IPMI pour interagir avec le système BIOS de la technologie RAID

Que votre machine soit dotée d'un contrôleur Adaptec ou d'un contrôleur LSI, vous devez accéder au serveur utilisant IPMI pour pouvoir interagir avec le système BIOS de la technologie RAID. Pour interagir avec IPMI, vous devez d'abord vous connecter au réseau privé virtuel {{site.data.keyword.cloud}} d'Adaptec. 
1. Connectez-vous au réseau privé virtuel via [SSL](../infrastructure/vpn/ssl-vpn-connections.html) ou PPTP. Voir la[page contenant la rubrique sur le réseau privé virtuel](../infrastructure/vpn/index.html).
* Accédez à la liste des unités dans le [portail client](https://control.softlayer.com/). Voir [Accès à la liste des unités](../vsi/vsi_managing.html).
* Cliquez sur l'unité à laquelle vous souhaitez accéder. 
* Sélectionnez l'onglet Gestion à distance pour trouver les détails d'accès du système IPMI de votre serveur. 
* Placez l'adresse IP de votre unité IPMI dans le navigateur et connectez-vous.
* Pour commencer à interagir avec la contrôle à distance, cliquez sur **Remote Control > Console Redirection**.

## Création de grappes RAID

Durant le processus de démarrage, appuyez sur les touches **Ctrl+A** pour accéder au BIOS RAID.

Pour commencer la configuration de RAID, ouvrez la configuration d'unité logique (Logical Device Configuration, première option). Cette option analyse la topologie de vos unités et affiche un menu dans lequel vous pouvez gérer des grappes, créer des grappes et exécuter d'autres tâches d'administration d'unité. 

L'exemple ci-après montre comment créer une grappe. La liste des unités disponibles que vous pouvez utiliser pour créer votre grappe RAID s'affiche.

1. Pour sélectionner les unités, appuyez sur la barre d'espacement afin de renseigner la zone *Selected Drives*. 
* Après avoir sélectionné toutes les unités à utiliser dans votre grappe, appuyez sur Entrée pour accéder à l'étape de configuration RAID.
* Choisissez le type de technologie RAID à utiliser. Si vous avez besoin d'aide pour déterminer quelle configuration RAID répond le mieux à vos besoins, reportez-vous à la [foire aux questions d'Adaptec](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm).
* Indiquez un intitulé de grappe durant la configuration. Une bonne pratique consiste à inclure le type de technologie RAID dans l'intitulé (par exemple, RAID10-A). 
* Appuyez sur la touche **Entrée** pour accéder aux autres paramètres. Utilisez les valeurs par défaut.

Une fois la configuration terminée, sélectionnez Done ; la grappe RAID est créée. Vous pouvez voir la nouvelle grappe en sélectionnant 'Manage Arrays' dans le menu principal. Pour quitter l'utilitaire de configuration, appuyez sur la touche d'échappement jusqu'à ce que vous soyez invité à quitter le système BIOS Adaptec.

## Retrait de grappes existantes

Si vous devez retirer une grappe existante, accédez à **Manage Arrays**, sélectionnez la grappe à retirer, appuyez sur **Supprimer** et confirmer.

## Exemples de configuration

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
