---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

keywords: spare pools, cancel, bare metal

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Annulation des pools de secours
{: #cancel-spare-pools}

Les unités ajoutées au pool de secours peuvent uniquement être annulées dans l'écran Pool de secours de la console {{site.data.keyword.cloud}}. L'annulation d'une unité dans le pool de secours est identique à celle d'une unité dans la liste des unités. Suivez les étapes décrites ci-dessous pour annuler une unité dans le pool de secours.
{:shortdesc}

## Annulation des pools de secours

1. Sauvegardez toutes les données que vous souhaitez conserver de l'unité à annuler.

   L'annulation d'une unité entraînera la suppression de toutes les données de l'unité annulée. Les informations stockées sur l'unité ne pourront pas être récupérées après l'annulation de l'unité.
   {:tip}

2. Accédez à la console [{{site.data.keyword.cloud}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/){: new_window} à l'aide de vos données d'identification uniques.
3. Sélectionnez **Unités > Pool de secours** dans la barre de navigation pour accéder à l'écran *Pool de secours*.
4. Sélectionnez **Actions > Annuler unité** pour l'unité concernée.
5. Sélectionnez la raison de l'annulation dans la liste déroulante **Motif**.
6. Entrez une brève explication du motif de l'annulation dans la zone de texte fournie.
7. Cliquez sur **Continuer** pour passer à l'écran suivant. Cliquez sur **Annuler** pour arrêter le processus d'annulation et retourner à l'écran Pool de secours.
8. Sélectionnez l'avis sur la perte de données**** pour confirmer qu'une perte de données peut se produire dans le cadre du processus d'annulation.
9. Cliquez sur **Annuler unité** pour annuler l'unité. Cliquez sur **Fermer** pour arrêter le processus d'annulation et retourner à l'écran Pool de secours.

## Etapes suivantes
Après avoir demandé l'annulation d'une unité dans le pool de secours, l'annulation de l'unité est planifiée. L'unité est alors immédiatement récupérée et supprimée du compte.
