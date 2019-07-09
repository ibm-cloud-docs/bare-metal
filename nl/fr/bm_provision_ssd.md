---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-02"

keywords: provision Intel Optane compatible bare metal server, Intel Optane, optane 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Mise à disposition d'un serveur bare metal compatible Intel Optane
{: #bm-provision-optane-server}

Pour mettre à disposition un serveur bare metal avec une unité Intel Optane :
1. Utilisez la procédure [Génération d'un serveur bare metal personnalisé](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server).
* Sélectionnez les options suivantes du formulaire de commande :

|Section|Option à sélectionner
|------|------|
|Région-Centre de données|Pour utiliser l'unité Intel Optane, sélectionnez l'un des centres de données suivants :<br>Europe - AMS03, FRA02, LON02, OSL01<br>Amérique du Nord, Sud DAL09, DAL10, DAL12<br>Asie-Pacifique - MEL01<br>Amérique du Nord, Est - MON01, TOR01, WDC04<br>Amérique du Nord, Ouest - SJC03<br>|
|Serveur|1. Sélectionnez **Tous les serveurs**<br>2. Sélectionnez *Biprocesseurs*<br>3. Sélectionnez l'un des serveurs suivants<br>-Intel Xeon 4110, jusqu'à 12 unités<br>-Intel Xeon 5120 avec jusqu'à 12 unités<br>-Intel Xeon 6140 avec jusqu'à 12 unités<br>-Intel Xeon E5-2620 v4 avec prise en charge de processeur graphique<br>-Intel Xeon E5-2650 v4 avec prise en charge de processeur graphique<br>-Intel Xeon E5-2690 v4 avec prise en charge de processeur graphique<br><br>  **Remarque** : Si vous sélectionnez E5-2620 v4, E5-2650 v4 ou E5-2650 v4, l'unité Intel Optane remplace votre processeur graphique (GPU) ; vous ne pouvez donc pas avoir à la fois un processeur graphique et une unité Intel Optane.|
|Système d’exploitation|Pour des unités Optane fournies par Intel, les systèmes d'exploitation suivants sont certifiés par Intel :<br>Windows Server 2016 (toutes éditions)<br>Windows Server 2012 R2 (toutes éditions)<br><br>Pour des unités livrées, open source, non-Intel, la compatibilité et la fonctionnalité sont validées mais non certifiées :<br>Red Hat Enterprise Linux 7.x (64 bits)<br>Red Hat Enterprise Linux 6.x (64 bits).
|Modules complémentaires des images| Sélectionnez une unité Intel Optane pour l'un et/ou l'autre des premier et deuxième composants PCIe.|
