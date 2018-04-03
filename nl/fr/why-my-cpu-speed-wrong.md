---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Pour quelle raison la vitesse de l'UC est-elle incorrecte ?

Vous vous connectez à un serveur pour vérifier les informations relatives à l'unité centrale et vous constatez que la vitesse des processeurs est incorrecte. Cette différence peut être liée à la technologie EIST (Enhanced Intel SpeedStep Technology). EIST est le nom Intel pour la technologie de mise à l'échelle de la fréquence dynamique. Cette technologie est également appelée *limitation d'UC* ou *balayage de bus* dans les systèmes plus anciens. Sur certains systèmes AMD, il existe des technologies similaires appelées *Cool'N'Quiet* ou *PowerNow!*. Ces technologies ne sont pas toutes identiques, mais leur finalité est la même, réduire la consommation électrique et la production de chaleur lorsque le processeur n'est pas utilisé de manière intensive en diminuant la vitesse de l'unité centrale. Lorsque le serveur est de nouveau en charge, ces technologies augmentent la fréquence d'horloge si nécessaire. 

Pour savoir si le processeur Intel sur votre serveur prend en charge SpeedStep : 
1. Cliquez sur **Equipements**.
* Identifiez votre serveur dans la liste.
* Cliquez sur le nom du serveur pour afficher **Détails de l'unité**.
* Localisez la sous-section intitulée **Matériel** pour trouver le numéro de modèle des processeurs de votre serveur et la vitesse de l'unité centrale. 
* Avec le numéro de modèle du processeur de serveur, accédez à [Intel Processor Finder](http://processorfinder.intel.com/) et utilisez ce numéro pour trouver d'autres informations sur le processeur et déterminer s'il prend en charge la technologie Enhanced Intel SpeedStep. 

EIST est une technologie établie. Vous ne devriez pas être amené à mettre EIST hors tension. Toutefois, si vous ne souhaitez pas utiliser ce dispositif, soumettez un ticket à l'équipe de support afin de le désactiver. La désactivation de ce dispositif entraînera le redémarrage du serveur. 
