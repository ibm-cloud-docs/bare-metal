---



copyright:
  years: 2014, 2018
lastupdated: "2018-02-01"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Réactivation d'une unité dans le pool de secours 
{: #reactivating-spare-pools}

Lorsqu'une unité est ajoutée au pool de secours, son état change passe de Actif (indiquant que l'unité est éligible pour des interactions standard) à Pool de secours. Les unités qui font partie du pool de secours sont dédiées à cette fonction et ne peuvent pas être utilisées pour les opérations quotidiennes et traditionnelles comme les autres unités. Pour supprimer une unité du pool de secours afin qu'elle puisse reprendre sa fonction traditionnelle, vous devez la réactiver. Pour réactiver une unité, procédez comme suit.
{:shortdesc}

## Réactivation d'une unité dans le pool de secours 

1. Accédez au portail [{{site.data.keyword.slportal_full}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com/){: new_window} en utilisant vos données d'identification uniques.
2. Sélectionnez **Unités > Pool de secours** dans la barre de navigation pour accéder à l'écran *Pool de secours*.
3. Sélectionnez **Actions > Réactiver unité** pour l'unité souhaitée.
4. Cliquez sur **Oui** pour réactiver le serveur. Cliquez sur **Non** pour annuler l'action.

## Etapes suivantes
Après avoir initié le processus de réactivation, l'unité est placée hors ligne, le microprogramme est mis à jour et l'unité devient disponible pour une utilisation normale. Le processus de réactivation dure environ une heure. Les unités qui sont supprimées du pool de secours ne peuvent plus être utilisées comme méthode de reprise en ligne. Vous pouvez replacer l'unité sur le pool de secours à tout moment en l'ajoutant à celui-ci à nouveau. Pour plus d'informations, veuillez vous référer à [Ajouter une unité au pool de secours](../vsi/adding_spare_pool.html).
