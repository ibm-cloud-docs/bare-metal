---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords: raid, about raid

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# A propos de la technologie RAID
{: #bm-raid-levels}

La technologie RAID (Redundant Array of Independent Disks) crée un disque de données utilisable dans lequel plusieurs disques physiques sont combinés en une grappe pour améliorer la vitesse et la tolérance aux pannes. La technologie RAID comporte trois concepts clé :
* **Mise en miroir **: copie des données sur plusieurs disques
* **Segmentation des données **: fractionnement des données sur plusieurs disques
* **Correction d'erreur** (tolérance aux pannes) : les données redondantes sont stockées pour permettre la détection des problèmes et leur résolution éventuelle.

Bien qu'il existe plusieurs niveaux de RAID, {{site.data.keyword.IBM_notm}} choisit de prendre en charge les types RAID les plus courants : 0, 1, 5, 6 et 10. Les différents niveaux RAID utilisent une ou plusieurs des techniques suivantes, en fonction de la configuration système requise. La technologie RAID permet principalement d'améliorer la fiabilité via un contrôleur 3Ware 9550SX Raid SATA ou Adaptec SA-SCSI RAID pour toutes les solutions RAID déployées.

La technologie RAID n'est pas une solution de sauvegarde. En effet, elle crée un disque de données utilisable dans lequel plusieurs disques physiques sont combinés en une grappe pour une meilleure vitesse et une meilleure tolérance aux pannes.
{: note}

**RAID 0** (ensemble segmenté sans parité/grappe non redondante) : Implémente la segmentation de données au cours de laquelle des blocs de fichiers sont écrits sur plusieurs disques sous forme de fragments et requiert au moins deux disques. Avec le niveau RAID 0, la vitesse des opérations d'écriture et de lecture augmente considérablement. Plus la grappe comporte de disques, plus la bande passante est importante. L'inconvénient d'un RAID 0 est l'absence de tolérance aux pannes. Si une seule unité tombe en panne, la grappe est cassée. De plus, RAID 0 n'implémente pas la vérification des erreurs. Ainsi, toute erreur est également irrécupérable. Une solution couramment employée pour la tolérance aux pannes consiste à utiliser comme stockage de sauvegarde pour les pannes matérielles une unité qui ne figure pas dans la grappe.

**RAID 1** (ensemble miroir sans parité) : Implémente la mise en miroir des données. Les données sont dupliquées sur 2 ou 4 disques par l'intermédiaire d'un contrôleur RAID matériel et offrent une certaine tolérance aux pannes. La grappe peut être récupérée si au moins une unité n'échoue pas. Il offre des performances de lecture plus rapides qu'une seule unité et assure la redondance de l'unité en cas de panne de cette dernière. La vitesse d'écriture est légèrement réduite.

**RAID 5** (ensemble segmenté avec double parité répartie) : Implémente la segmentation de données au niveau des blocs et répartit la parité parmi les disques. Les informations de parité permettent d'effectuer une reprise après un incident survenu sur n'importe quelle unité unique car les opérations de lecture suivantes peuvent être calculées à partir de la parité répartie. Le niveau RAID 5 permet également d'augmenter les vitesses de lecture/d'écriture et d'utiliser l'espace disque de la manière la plus efficiente qui soit. Le niveau RAID 5 requiert au moins trois disques.

**RAID 6** (double parité) : Implémente des bandes de parité doubles sur chaque disque et permet à deux disques de tomber en panne avant qu'aucune donnée ne soit perdue. Comme le RAID 6 a une capacité de deux unités de disque dédiées au stockage de données de parité dans un jeu de parité, les opérations d'E/S sont plus importantes avec le RAID 6 qu'avec le RAID 5. Ces opérations d'E/S plus importantes peuvent diminuer les performances. RAID 6 nécessite un minimum de 4 disques et un maximum de 18 disques.

**RAID 10** (RAID 1 + 0) : Crée plusieurs miroirs, dans lesquels les données sont organisées sous forme de segments répartis sur plusieurs disques, puis les ensembles de disques segments sont mis en miroir. Le niveau RAID 10 offre la même tolérance aux pannes que le niveau RAID 1 avec des vitesses de lecture/d'écriture supérieures par rapport à un volume RAID 1 unique ou une unité unique. Le niveau RAID 10 demande l'implémentation de quatre disques.
