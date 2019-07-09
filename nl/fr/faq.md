---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-16"

keywords: bare metal, faq, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Foire aux questions : Serveurs bare metal
{: #bm-faq}

## Qu'est-ce que le mode d'amorçage UEFI ?
{: faq}
UEFI (Unified Extensible Firmware Interface) est une spécification pour l'interface logicielle entre un système d'exploitation et le microprogramme.

La prise en charge du mode d'amorçage BIOS dans IBM Cloud est progressivement supprimée en faveur de UEFI.

Pour plus d'informations sur l'UEFI, consultez la documentation du fabricant de votre matériel ou accédez à [https://uefi.org/](https://uefi.org/)

## Pour quelle raison mon système BIOS me réclame-t-il un mot de passe ?
{: faq}

Actuellement, {{site.data.keyword.cloud}} ne vous permet pas d'accéder directement à votre système BIOS, et ce pour différentes raisons. Vous pouvez néanmoins modifier le BIOS. Si vous avez besoin de modifier quoi que ce soit au niveau du BIOS, y compris l'ordre d'amorçage, créez un ticket sous Support > Ajouter un ticket via le portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/){: new_window} et demandez les modifications spécifiques requises.

\*\*REMARQUE\*\* Toute modification nécessite de redémarrer le serveur. Par conséquent, soyez prêt à approuver un redémarrage et/ou à indiquer un délai pour la réalisation de la modification.

## Fournissez-vous des rechargements du système d'exploitation ?
{: faq}

Les rechargements du système d'exploitation automatisés sont gratuits et peuvent être effectués via le portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/){: new_window}. Cela inclut des rechargements de système d'exploitation personnalisés (changement de systèmes d'exploitation, ajout/retrait de panneaux de configuration, édition de partition, etc.).  Pour plus d'informations sur l'exécution d'un rechargement du système d'exploitation, voir [la section décrivant la procédure de rechargement du système d'exploitation](/docs/infrastructure/software?topic=software-reloading-the-os).


## L'unité principale de mon serveur bare metal se présente sous la forme /dev/sdb. Que se passe-t-il ?
{: faq}

Cela peut être dû au fait que le disque virtuel d'IPMI utilise l'emplacement /dev/sda. Pour désactiver cette association en toute sécurité, connectez-vous à IPMIView et accédez à l'onglet Virtual Media. Sélectionnez **Options > Désactiver**, puis cliquez sur le bouton **Appliquer** pour effectuer la modification. Au prochain redémarrage du serveur {{site.data.keyword.baremetal_short}}, /dev/sda apparaîtra comme unité principale.


## Pour quelle raison la vitesse de l'UC est-elle incorrecte ?
{: faq}

Vous vous connectez à un serveur pour vérifier les informations relatives à l'unité centrale et vous constatez que la vitesse des processeurs est incorrecte. Cette différence peut être liée à la technologie EIST (Enhanced Intel SpeedStep Technology). EIST est le nom Intel pour la technologie de mise à l'échelle de la fréquence dynamique.  Cette technologie est également appelée *limitation d'UC* ou *balayage de bus* dans les systèmes plus anciens.  Certains systèmes AMD possèdent des technologies similaires appelées *Cool'N'Quiet* ou *PowerNow!*.  Ces technologies ne sont pas toutes identiques, mais leur finalité est la même, réduire la consommation électrique et la production de chaleur lorsque le processeur n'est pas utilisé de manière intensive en diminuant la vitesse de l'unité centrale.  Lorsque le serveur est de nouveau en charge, ces technologies augmentent la fréquence d'horloge si nécessaire.

Pour savoir si le processeur Intel sur votre serveur prend en charge SpeedStep, utilisez la procédure suivante depuis le portail client :
1. Cliquez sur **Equipements**.
* Identifiez votre serveur dans la liste.
* Cliquez sur le nom du serveur pour afficher **Détails de l'unité**.
* Localisez la sous-section intitulée **Matériel** pour trouver le numéro de modèle des processeurs de votre serveur et la vitesse de l'unité centrale.
* Avec le numéro de modèle du processeur de serveur, accédez à [Intel Processor Finder ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://processorfinder.intel.com/){: new_window} et utilisez ce numéro pour trouver d'autres informations sur le processeur et déterminer s'il prend en charge la technologie Enhanced Intel SpeedStep.

EIST est une technologie établie. La désactivation de EIST n'est pas une procédure courante. Toutefois, si vous ne souhaitez pas utiliser ce dispositif, soumettez un ticket à l'équipe de support afin de le désactiver.  Pour désactiver le dispositif, vous devez redémarrer le serveur.


## Que faire si le microprogramme de mon serveur bare metal est obsolète ?
{: faq}

Il est important de mettre à jour le microprogramme pour s'assurer que votre serveur bare metal assure une compatibilité et une stabilité optimales des équipements. Si une version de microprogramme de serveurs {{site.data.keyword.baremetal_short}} est obsolète, le microprogramme peut être mis à jour en sélectionnant le serveur bare metal dans la liste des unités et en sélectionnant **Mettre à niveau le microprogramme** dans le menu d'actions.

Vous pouvez lancer une mise à jour du microprogramme pendant le processus [Rechargement du système d'exploitation](/docs/infrastructure/software?topic=software-reloading-the-os) dans le portail [{{site.data.keyword.slportal}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/){: new_window}.

## Qu'advient-il des unités sur les serveurs bare metal quand un client a fini de les utiliser ?
{: faq}

Lors de l'annulation, un serveur est automatiquement placé sur un réseau local virtuel de récupération pour une durée d'attente définie. Une fois la période écoulée, les processus de récupération débutent et l'unité est effacée au moyen d'algorithmes DOD 5220.22-M.  La récupération est contrôlée via le numéro de série sur l'unité. A l'issue de la procédure, le serveur est placé en mise à disposition pour être réaffecté. Une dysfonctionnement d'unité requiert une intervention manuelle les unités passent alors à l'état de fin de vie.

Le processus de fin de vie est initié quand la prise en charge ne peut plus être assurée en raison d'un dysfonctionnement, de l'âge ou de la taille de l'unité. Lorsque l'une de ces conditions survient, les unités sont effacées comme décrit précédemment. Une fois le processus d'effacement terminé, l'unité est physiquement détruite (casse, broyage, etc.).  Le processus de destruction physique est contrôlé via le numéro de série sur l'unité.

## Puis-je voir quels serveurs bare metal sont disponibles à l'achat ?
{: faq}

Oui. Vous pouvez maintenant voir quels serveurs sont disponibles dans quel centre de données lorsque vous mettez à disposition un serveur bare metal. Cependant, cette option n'est disponible que pour l'offre horaire. Vous ne pouvez pas voir la disponibilité du serveur avec l'offre mensuelle. Pour en savoir plus sur la mise à disposition d'un serveur bare metal, voir [Sélection depuis les serveurs les plus populaires](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers#bm-select-popular-servers).

## Qu'est-ce qui est inclus avec mon serveur bare metal réservé ?
{: faq}

Le CPU, la RAM, le lecteur de disque et le RAID sont inclus dans la réservation durant toute la durée du contrat. Si vous avez besoin d'une bande passante réseau plus importante, d'une plus grande capacité de stockage, d'un système d'exploitation et de logiciels tiers, ces extensions sont facturées mensuellement.

## Que se passe-t-il à la fin de mon contrat de serveur bare metal réservé ?
{: faq}

Votre service cloud continue sur une période de service mensuelle au tarif en vigueur à l'expiration de votre contrat.
