---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Mise à disposition d'un serveur bare metal compatible Intel Optane
Pour mettre à disposition un serveur bare metal avec une unité Intel Optane :
1. Utilisez la procédure [Génération d'un serveur bare metal personnalisé](../bare-metal/baremetal-provision.html).
* Sélectionnez les options suivantes du formulaire de commande :

|Section|Option à sélectionner
|------|------|
|Centre de données|Pour utiliser l'unité Intel Optane, sélectionnez l'un des centres de données suivants :<br>AMS03 - Amsterdam<br>DAL09 - Dallas<br>DAL10 - Dallas<br>DAL12 - Dallas<br>FRA02 - Francfort<br>LON02 - Londres<br>MEL01 - Melbourne<br>MON01 - Montréal<br>OSL01 - Oslo<br>SJC03 - San Jose<br>TOR01 - Toronto<br>WDC04 - Washington, DC|
|Serveur|Les serveurs suivants sont compatibles avec l'unité Intel Optane<br>Intel Xeon 4110  jusqu'à 12 unités<br>Intel Xeon 5120  jusqu'à 12 unités<br>Intel Xeon 6140  jusqu'à 12 unités<br>Intel Xeon E5-2620 v4 avec prise en charge GPU<br>Intel Xeon E5-2650 v4 avec prise en charge GPU<br>Intel Xeon E5-2690 v4 avec prise en charge GPU<br><br>  **Remarque** : Si vous sélectionnez E5-2620 v4, E5-2650 v4 ou E5-2650 v4, l'unité Intel Optane remplace votre processeur graphique (GPU) ; vous ne pouvez donc pas avoir à la fois un processeur graphique et une unité Intel Optane.|
|Composants PCIe| Sélectionnez une unité Intel Optane pour l'un et/ou l'autre des premier et deuxième composants PCIe.|
|Système d’exploitation|Pour des unités Optane fournies par Intel, les systèmes d'exploitation suivants sont certifiés par Intel :<br>Windows Server 2016 (toutes éditions)<br>Windows Server 2012 R2 (toutes éditions)<br><br>Pour des unités livrées, open source, non-Intel, la compatibilité et la fonctionnalité sont validées mais non certifiées :<br>Red Hat Enterprise Linux 7.x (64 bits)<br>Red Hat Enterprise Linux 6.x (64 bits).
