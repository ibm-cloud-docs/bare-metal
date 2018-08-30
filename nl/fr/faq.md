---

copyright:
  years: 2014, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Foire aux questions : Serveurs bare metal

## Pour quelle raison mon système BIOS me réclame-t-il un mot de passe ?

Actuellement, {{site.data.keyword.cloud}} ne vous permet pas d'accéder directement à votre système BIOS, et ce pour différentes raisons. Vous pouvez néanmoins modifier le BIOS. Si vous avez besoin de modifier quoi que ce soit au niveau du BIOS, y compris l'ordre d'amorçage, créez un ticket sous Support > Ajouter un ticket via le [portail client](https://control.softlayer.com/) et demandez les modifications spécifiques requises. 

\*\*REMARQUE\*\* Toute modification nécessite de redémarrer le serveur. Par conséquent, soyez prêt à approuver un réamorçage et/ou à indiquer un délai pour la réalisation de la modification. 

## Fournissez-vous des rechargements du système d'exploitation ?

Les rechargements du système d'exploitation automatisés sont gratuits et peuvent être effectués via le [portail client](https://control.softlayer.com/). Cela inclut des rechargements de système d'exploitation personnalisés (changement de systèmes d'exploitation, ajout/retrait de panneaux de configuration, édition de partition, etc.).  Pour plus d'informations sur l'exécution d'un rechargement du système d'exploitation, voir [la section décrivant la procédure de rechargement du système d'exploitation](../vsi/vsi_perform_os_reload.html).


## L'unité principale de mon serveur bare metal se présente sous la forme /dev/sdb. Que se passe-t-il ?

Cela peut être dû au fait que le disque virtuel d'IPMI utilise l'emplacement /dev/sda. Pour désactiver cette association en toute sécurité, connectez-vous à IPMIView et accédez à l'onglet Virtual Media. Sélectionnez **Options > Disable**, puis cliquez sur le bouton **Apply** pour effectuer la modification. Au prochain redémarrage du serveur {{site.data.keyword.baremetal_short}}, /dev/sda apparaîtra comme unité principale.


## Pour quelle raison la vitesse de l'UC est-elle incorrecte ?

Vous vous connectez à un serveur pour vérifier les informations relatives à l'unité centrale et vous constatez que la vitesse des processeurs est incorrecte. Cette différence peut être liée à la technologie EIST (Enhanced Intel SpeedStep Technology). EIST est le nom Intel pour la technologie de mise à l'échelle de la fréquence dynamique.  Cette technologie est également appelée *limitation d'UC* ou *balayage de bus* dans les systèmes plus anciens.  Certains systèmes AMD possèdent des technologies similaires appelées *Cool'N'Quiet* ou *PowerNow!*. Ces technologies ne sont pas toutes identiques, mais leur finalité est la même, réduire la consommation électrique et la production de chaleur lorsque le processeur n'est pas utilisé de manière intensive en diminuant la vitesse de l'unité centrale. Lorsque le serveur est de nouveau en charge, ces technologies augmentent la fréquence d'horloge si nécessaire.

Pour savoir si le processeur Intel sur votre serveur prend en charge SpeedStep, utilisez la procédure suivante depuis le portail client :
1. Cliquez sur **Equipements**.
* Identifiez votre serveur dans la liste.
* Cliquez sur le nom du serveur pour afficher **Détails de l'unité**.
* Localisez la sous-section intitulée **Matériel** pour trouver le numéro de modèle des processeurs de votre serveur et la vitesse de l'unité centrale.
* Avec le numéro de modèle du processeur de serveur, accédez à [Intel Processor Finder](http://processorfinder.intel.com/) et utilisez ce numéro pour trouver d'autres informations sur le processeur et déterminer s'il prend en charge la technologie Enhanced Intel SpeedStep.

EIST est une technologie établie. La désactivation de EIST n'est pas une procédure courante. Toutefois, si vous ne souhaitez pas utiliser ce dispositif, soumettez un ticket à l'équipe de support afin de le désactiver. Pour désactiver le dispositif, le serveur est réamorcé. 


## Que faire si le microprogramme de mon serveur bare metal est obsolète ?

Comme pour les mises à jour logicielles, il est important d'effectuer les mises à jour du microprogramme afin d'optimiser la compatibilité et la stabilité de vos équipements. Si un microprogramme {{site.data.keyword.baremetal_short}} est obsolète, il est possible de lancer une mise à jour du microprogramme lors du processus de [rechargement du système d'exploitation](../infrastructure/software/vsi_reload_os.html) au sein du [portail client](https://control.softlayer.com).

Vous pouvez également mettre à jour le microprogramme en choisissant le serveur bare metal dans la liste des unités et en sélectionnant **Mettre à niveau le microprogramme** dans le menu des actions. 

## Qu'advient-il des unités sur les serveurs bare metal quand un client a fini de les utiliser ?

Lors de l'annulation, un serveur est automatiquement placé sur un réseau local virtuel de récupération pour une durée d'attente définie. Une fois la période écoulée, les processus de récupération débutent et l'unité est effacée au moyen d'algorithmes DOD 5220.22-M. La récupération est contrôlée via le numéro de série sur l'unité. A l'issue de la procédure, le serveur est placé en mise à disposition pour être réaffecté. Une dysfonctionnement d'unité requiert une intervention manuelle les unités passent alors à l'état de fin de vie. 

Le processus de fin de vie est initié quand la prise en charge ne peut plus être assurée en raison d'un dysfonctionnement, de l'âge ou de la taille de l'unité. Lorsque l'une de ces conditions survient, les unités sont effacées comme décrit précédemment. Une fois le processus d'effacement terminé, l'unité est physiquement détruite (casse, broyage, etc.). Le processus de destruction physique est contrôlé via le numéro de série sur l'unité. 
