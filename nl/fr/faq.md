---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Foire aux questions : Serveurs bare metal

## Pour quelle raison mon système BIOS me réclame-t-il un mot de passe ?

Actuellement, {{site.data.keyword.cloud}} ne vous permet pas d'accéder directement à votre système BIOS. Cela se justifie à plusieurs titres, pour autant, vous avez tout de même la possibilité de modifier votre système BIOS. Si vous avez besoin de modifier quelque chose dans le système BIOS, y compris l'ordre d'amorçage, créez un ticket sous Support > Ajouter un ticket via le [portail client](control.softlayer.com) et demandez les modifications spécifiques requises. 

\*\*REMARQUE\*\* cela nécessitera de redémarrer le serveur. Par conséquent, soyez prêt à approuver un réamorçage et/ou à indiquer un délai pour la réalisation de la modification. 

## Fournissez-vous des rechargements du système d'exploitation ?

Les rechargements du système d'exploitation automatisés sont gratuits et peuvent être effectués via le [portail client](control.softlayer.com). Cela inclut des rechargements de système d'exploitation personnalisés (changement de systèmes d'exploitation, ajout/retrait de panneaux de configuration, édition de partition, etc.). Pour plus d'informations sur l'exécution d'un rechargement du système d'exploitation, voir [la section décrivant la procédure de rechargement du système d'exploitation](../vsi/vsi_perform_os_reload.html).


## L'unité principale de mon serveur bare metal se présente sous la forme /dev/sdb. Que se passe-t-il ?

Cela peut être dû au fait que le disque virtuel d'IPMI utilise l'emplacement /dev/sda. Pour désactiver cette association, connectez-vous à IPMIView et accédez à l'onglet Virtual Media. Sélectionnez **Options > Disable**, puis cliquez sur le bouton **Apply** pour effectuer la modification. Au prochain redémarrage du serveur {{site.data.keyword.baremetal_short}}, /dev/sda apparaîtra comme unité principale.


## Pour quelle raison la vitesse de l'UC est-elle incorrecte ?

Vous vous connectez à un serveur pour vérifier les informations relatives à l'unité centrale et vous constatez que la vitesse des processeurs est incorrecte. Cette différence peut être liée à la technologie EIST (Enhanced Intel SpeedStep Technology). EIST est le nom Intel pour la technologie de mise à l'échelle de la fréquence dynamique. Cette technologie est également appelée *limitation d'UC* ou *balayage de bus* dans les systèmes plus anciens. Sur certains systèmes AMD, il existe des technologies similaires appelées *Cool'N'Quiet* ou *PowerNow!*. Ces technologies ne sont pas toutes identiques, mais leur finalité est la même, réduire la consommation électrique et la production de chaleur lorsque le processeur n'est pas utilisé de manière intensive en diminuant la vitesse de l'unité centrale. Lorsque le serveur est de nouveau en charge, ces technologies augmentent la fréquence d'horloge si nécessaire. 

Pour savoir si le processeur Intel sur votre serveur prend en charge SpeedStep : 
1. Cliquez sur **Equipements**.
* Identifiez votre serveur dans la liste.
* Cliquez sur le nom du serveur pour afficher **Détails de l'unité**.
* Localisez la sous-section intitulée **Matériel** pour trouver le numéro de modèle des processeurs de votre serveur et la vitesse de l'unité centrale. 
* Avec le numéro de modèle du processeur de serveur, accédez à [Intel Processor Finder](http://processorfinder.intel.com/) et utilisez ce numéro pour trouver d'autres informations sur le processeur et déterminer s'il prend en charge la technologie Enhanced Intel SpeedStep. 

EIST est une technologie établie. Vous ne devriez pas être amené à mettre EIST hors tension. Toutefois, si vous ne souhaitez pas utiliser ce dispositif, soumettez un ticket à l'équipe de support afin de le désactiver. La désactivation de ce dispositif entraînera le redémarrage du serveur. 


## Que faire si le microprogramme de mon serveur bare metal est obsolète ?

Comme pour les mises à jour logicielles, il est important d'effectuer les mises à jour du microprogramme afin d'optimiser la compatibilité et la stabilité de vos équipements. Si un microprogramme {{site.data.keyword.baremetal_short}} est obsolète, il est possible de lancer une mise à jour du microprogramme lors du processus de [rechargement du système d'exploitation](../infrastructure/software/vsi_reload_os.html) au sein du [portail client](https://control.softlayer.com).

Vous pouvez également mettre à jour le microprogramme en choisissant le serveur bare metal dans la liste des unités et en sélectionnant **Mettre à niveau le microprogramme** dans le menu déroulant des actions. 
