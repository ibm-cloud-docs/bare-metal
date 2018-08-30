---
copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# A propos de la technologie RAID

La technologie RAID (Redundant Array of Independent Disks) crée n disque de données utilisable dans lequel plusieurs disques physiques sont combinés en une grappe pour améliorer la vitesse et la tolérance aux pannes. La technologie RAID comporte trois concepts clé : 
* Mise en miroir : copie des données sur plusieurs disques
* Segmentation de données : fractionnement des données sur plusieurs disques
* Correction d'erreur (tolérance aux pannes) : les données redondantes sont stockées pour permettre la détection des problèmes et leur résolution éventuelle.

Bien qu'il existe de nombreux niveaux RAID différents, IBM choisit de prendre en charge les types RAID les plus courants : 0, 1, 5 et 10. Les différents niveaux RAID utilisent une ou plusieurs des techniques suivantes, en fonction de la configuration système requise. La technologie RAID permet principalement d'améliorer la fiabilité via un contrôleur 3Ware 9550SX Raid SATA ou Adaptec SA-SCSI RAID pour toutes les solutions RAID déployées.

La technologie RAID n'est pas une solution de sauvegarde.  Elle crée un disque de données utilisable dans lequel plusieurs disques physiques sont combinés en une grappe pour améliorer la vitesse et/ou la tolérance aux pannes.


**RAID 0** (ensemble segmenté sans parité/grappe non redondante) : Implémente la segmentation de données au cours de laquelle des blocs de fichiers sont écrits sur plusieurs unités sous forme de fragments et requiert au moins deux disques. Avec le niveau RAID 0, la vitesse des opérations d'écriture et de lecture augmente considérablement. Plus la grappe comporte de disques, plus la bande passante est importante. L'inconvénient du niveau RAID0 est son manque de tolérance aux pannes. Par conséquent, si une seule unité échoue, la grappe est détruite. En outre, le niveau RAID 0 n'implémente pas la vérification des erreurs. Par conséquent, toutes les erreurs, quelles qu'elles soient, sont irrécupérables. Une solution couramment employée pour la tolérance aux pannes consiste à utiliser comme stockage de sauvegarde pour les pannes matérielles une unité qui ne figure pas dans la grappe. 

**RAID 1** (ensemble miroir sans parité) : Implémente la mise en miroir des données. Les données sont dupliquées sur 2 ou 4 unités via un contrôleur RAID de matériel et fournit la tolérance aux pannes. La grappe peut être récupérée si au moins une unité n'échoue pas. Les performances de lecture obtenues sont meilleures qu'avec une seule unité et la redondance des unités est fournie en cas de défaillance d'unité. La vitesse d'écriture est également légèrement réduite. 

**RAID 5** (ensemble segmenté avec double parité répartie) : Implémente la segmentation de données au niveau des blocs et répartit la parité parmi les unités. Les informations de parité permettent d'effectuer une reprise après un incident survenu sur n'importe quelle unité unique car les opérations de lecture suivantes peuvent être calculées à partir de la parité répartie. Le niveau RAID 5 permet également d'augmenter les vitesses de lecture/d'écriture et d'utiliser l'espace disque de la manière la plus efficiente qui soit. Le niveau RAID 5 requiert au moins trois disques.

**RAID 10** (RAID 1 + 0) : Crée plusieurs miroirs, dans lesquels les données sont organisées sous forme de segments répartis sur plusieurs disques, puis les ensembles de disques segments sont mis en miroir. Le niveau RAID 10 offre la même tolérance aux pannes que le niveau RAID 1 avec des vitesses de lecture/d'écriture supérieures par rapport à un volume RAID 1 unique ou une unité unique. Quatre unités sont requises pour le niveau RAID 10.
