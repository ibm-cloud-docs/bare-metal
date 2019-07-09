---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-31"

keywords: bare metal, spare pools

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:tip: .tip}
{:table: .aria-labeledby="caption"}


# Ajout de pools de secours
{: #adding-spare-pools}

La mise sur pool de secours permet de contenir certaines unités qui sont désignées comme des unités de secours et qui ont la capacité de prendre en charge le flux de travail d'une unité principale ou d'agir comme une nouvelle unité dans la flotte du client. Pour qu'une unité soit désignée comme unité de secours, elle doit être ajoutée au pool de secours et associée à une unité principale. Suivez les étapes ci-dessous pour ajouter une unité au pool de secours.
{:shortdesc}

1. Accédez à la console [{{site.data.keyword.cloud}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/){: new_window} à l'aide de vos données d'identification uniques.
2. Sélectionnez **Unités > Pool de secours** dans la barre de navigation pour accéder à l'écran *Pool de secours*.
3. Cliquez sur le lien **Ajouter au pool de secours**.

   Ceci complétera la liste des unités éligibles pour être ajoutées au pool de secours.
   {:tip}

4. Sélectionnez les unités que vous souhaitez ajouter au pool de secours.
5. Cliquez sur **Ajouter les unités sélectionnées au pool de secours**.
6. Cliquez sur **Confirmer** pour ajouter les unités au pool de secours.

## Etapes suivantes
Après avoir initié le transfert d'une unité au pool de secours, l'unité est transférée au pool de secours dans l'heure qui suit. Une fois que l'unité est active dans le pool de secours, elle s'affiche sur l'écran Pool de secours et peut être désignée en tant qu'unité de secours à chaud pour une unité principale.
