---



copyright:
  years: 2017
lastupdated: "2017-12-05"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Configuration de votre serveur bare metal

Il est bon de prendre le temps et de prendre les décisions de configuration bien avant la mise à disposition d'un serveur {{site.data.keyword.baremetal_long}}. Ainsi, le processus de mise à disposition sera plus rapide et plus lisse. {:shortdesc}

## Processus visant à déterminer l'utilisation du serveur et à définir sa taille

Votre première tâche consiste à déterminer de quelle façon vous envisagez d'utiliser votre serveur {{site.data.keyword.baremetal_short}}. Par exemple, avez-vous l'intention de l'utiliser dans un environnement de développement/test ou dans un environnement de production ? Procédez-vous à un test des acquis utilisateur, traitez-vous des algorithmes assez longs, procédez-vous à la restauration et à la sauvegarde de données ou augmentez-vous la vitesse des temps d'attente ?

Après avoir déterminé la façon dont le serveur {{site.data.keyword.baremetal_short}} sera utilisé, vous devez définir la taille de celui-ci. Le [calculateur du coût total de possession SoftLayer](http://www.softlayer.com/tco/) peut vous aider à déterminer la partie du serveur {{site.data.keyword.baremetal_short}} qui répond le mieux à vos besoins.

## Sélection de votre serveur

{{site.data.keyword.cloud_notm}} offre sept serveurs avec mise à disposition rapide afin de vous garantir des performances en adéquation avec votre charge de travail. Ces serveurs sont actuellement disponibles au Royaume-uni et dans les régions du Sud des Etats-Unis.

| **Configuration** | **Processeur** | **Mémoire** | **Disque dur** | **Vitesse de port** |
|-------------------|---------------|------------|----------------|----------------|
| Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 coeurs, 3,50 GHz) |32 Go de mémoire RAM |1 unité de disque dur interne |Vitesse de port maximale de 100 Mbit/s |
|Intel Xeon E5-2620 v3 |Dual Intel Xeon E5-2620 v3 (6 coeurs, 2,40 GHz) |64 Go de mémoire RAM |2 unités de disque dur internes |Vitesse de port maximale de 100 Mbit/s |
|Intel Xeon E3-1270 v3 |Single Intel Xeon E3-1270 v3 (4 coeurs, 3,50 GHz) |32 Go de mémoire RAM |2 unités de disque dur internes |Vitesse de port maximale de 100 Mbit/s |
|Intel Xeon E5-2650 v3 |Dual Intel Xeon E5-2650 v3 (10 coeurs, 2,30 GHz) |128 Go de mémoire RAM |1 unité de disque dur interne |Vitesse de port maximale de 100 Mbit/s |
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 coeurs, 2,60 GHz) |128 Go de mémoire RAM |2 unités de disque dur internes |Vitesse de port maximale de 100 Mbit/s |
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 coeurs, 2,60 GHz) |64 Go de mémoire RAM |4 unités de disque dur internes |Vitesse de port maximale de 1 000 Mbit/s |
|Intel Xeon E5-2690 v3 |Dual Intel Xeon E5-2690 v3 (12 coeurs, 2,60 GHz) |256 Go de mémoire RAM |4 unités de disque dur internes |Vitesse de port maximale de 1 000 Mbit/s |

Outre les sept serveurs avec mise à disposition rapide, {{site.data.keyword.cloud_notm}} a développé son offre {{site.data.keyword.baremetal_short}} afin d'inclure des systèmes bare metal POWER8. Ces systèmes sont créés avec le processeur POWER8 d'{{site.data.keyword.IBM_notm}} et une plateforme OpenPOWER, réglée spécifiquement pour les déploiements de type cloud de données et de contenu cognitif et Web sous Linux.

N'importe quel serveur {{site.data.keyword.baremetal_short}} peut être mis à niveau pour inclure une bande passante non mesurée (illimitée). Toutes les unités non mesurées sont sur des ports dédiés privés.

## Configuration de vos serveurs bare metal

Après avoir sélectionné un centre de données, un serveur et une option de facturation (mensuelle ou horaire), vous devez décider de quelle manière vous souhaitez configurer votre serveur. Les valeurs par défaut de certaines zones (Serveurs, Mémoire RAM, Carte graphique et Carte graphique secondaire) sur la page **Configurez votre {{site.data.keyword.baremetal_short}}** dépendront de votre sélection de serveur. Le tableau ci-après décrit les zones pour lesquelles vous pouvez définir une valeur.

| **Zone** | **Description** |
|-------------------|---------------|
|Système d'exploitation |Choisissez CentOS, FreeBSD, Microsoft, Red Hat, Unbuntu ou d'autres systèmes d'exploitation. |
|Disques durs |L'outil de configuration de disque vous permet de configurer vos disques durs en renseignant préalablement les zones en fonction de votre sélection de système d'exploitation. |
|Bande passante publique |Détermine la quantité de données pouvant être transférée via l'interface publique durant un mois. Pour les environnements de test, pour lesquels des données d'installation doivent être transférées via cette interface, les valeurs doivent être adaptées au-delà de la quantité de données transférées initialement. Vous souhaiterez peut-être utiliser le [réseau {{site.data.keyword.cloud_notm}} Content Delivery Network](https://www.ibm.com/cloud/cdn) afin d'expédier un chargement de données initial à l'un des centres de données {{site.data.keyword.cloud_notm}}. |
|Vitesses de port Uplink |Détermine la vitesse des interfaces internes et externes. |
|Adresses IP secondaires publiques |Affecte une adresse IP supplémentaire à votre serveur. En fonction de votre scénario, vous aurez besoin que d'autres adresses IP soient affectées à votre serveur. D'autres adresses IPv4 sont disponibles dans les quantités suivantes : 1, 2, 4, 8, 16 ou 32. |
|Adresses IPv6 principales |Affectées aux interfaces internes et externes de votre serveur. |
|Adresses IPv6 statiques publiques |Affecte d'autres adresses IPv6 à partir d'un bloc /64. |
|Pare-feux matériel & logiciel, Antivirus & protection contre les logiciels espions et Détection d'intrusion et protection anti-intrusion |Sélectionnez les options appropriées si le serveur sera exposé à Internet. Il est fortement recommandé que votre service de sécurité d'entreprise se rapproche du support {{site.data.keyword.cloud_notm}} afin de discuter des caractéristiques de ces options. |
|Evault |Outil de sauvegarde basé sur un agent pouvant être installé sur votre serveur afin de répliquer des sauvegardes entre les serveurs. |

Pour plus d'informations, contacter le support {{site.data.keyword.cloud_notm}}. 


## Configuration système avancée

La configuration système avancée est effectuée une fois que vous avez cliqué sur le bouton **Ajouter à la commande** et que vous êtes redirigé vers la page de réservation. Le tableau ci-après décrit les zones sous la section de configuration système avancée.

| **Zone** | **Description** |
|-------------------|---------------|
|Nom d'hôte |Nom permanent ou temporaire affecté à votre serveur, par exemple, _server1_. |
|Domaine |Nom de sous-domaine qui ne doit pas entrer en conflit avec un nom de domaine Internet, par exemple, _test.acme.com_. |
|Sélection VLAN |S'il existe un réseau local virtuel sous votre compte car vous avez déjà commandé au moins un serveur, vous pouvez ajouter le nouveau serveur à ce réseau local virtuel. |
|Script de mise à disposition |Vous pouvez fournir un script qui vous permet d'automatiser certaines étapes après que le serveur a été mis à disposition. |
|Clés SSH |Vous pouvez fournir une clé publique pour votre clé SSH, ce qui vous permettra de vous connecter à votre serveur une fois celui-ci mis à disposition. |
