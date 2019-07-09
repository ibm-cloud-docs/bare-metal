---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: bare metal, no os, no operating system

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# Option Aucun système d'exploitation
{: #bm-no-os}

**Aucun système d'exploitation** est une option qui permet de commander des serveurs bare metal IBM® Cloud sans système d'exploitation.

## Commande d'un serveur bare metal sans système d'exploitation
{: #ordering-no-os}

1. Utilisez les étapes décrites dans [Génération d'un serveur bare metal personnalisé](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server) pour commander votre serveur.
2. Sélectionnez **Aucun système d'exploitation** sous **Image**.
3. Procédez à la commande de votre serveur. 

## Passage à un serveur sans système d'exploitation
{: #changing-to-no-os}

Un serveur peut être reconfiguré pour ne pas avoir de système d'exploitation. La reconfiguration s'effectue par le biais d'un rechargement du système d'exploitation. Pour en savoir plus, voir [Rechargement du système d'exploitation](/docs/infrastructure/software?topic=software-reloading-the-os).

1. Cliquez sur **Unités** > **Liste des unités**.
2. Sélectionnez le serveur que vous souhaitez reconfigurer sans système d'exploitation.
3. Cliquez sur **Rechargement du système d'exploitation** et entrez les informations applicables.

## Installation d'un système d'exploitation sur un serveur sans système d'exploitation
{: #installing-os-on-no-os-server}

Il existe deux moyens d'installer des systèmes d'exploitation sur des serveurs bare metal sans système d'exploitation.

### Option 1 : Serveur PXE
{: #option-1}

Le serveur bare metal sans système d'exploitation peut être configuré pour être démarré et charger un système d'exploitation à partir d'une configuration PXE.<!--(see [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) for more information)--> Déployez le serveur bare metal dans un environnement réseau avec une configuration PXE (ceci implique généralement l'exécution d'un démon DHCP et TFTP) et configurez le système BIOS des nouveaux serveurs pour démarrer à partir de l'adaptateur réseau. Pour que l'option sans système d'exploitation fonctionne correctement, la configuration PXE doit figurer dans le même réseau local virtuel que le serveur bare metal, ou bien l'acheminement DHCP doit être utilisé.

Il peut être nécessaire d'ouvrir un ticket de demande de service pour demander que les ports de commutation soient regroupés en mode de base pour que cette option fonctionne. Cela est dû au fait que le protocole PXE n'a pas besoin d'être compatible avec l'agrégation de liaison (LACP), <!--see [Link Aggregation](http://en.wikipedia.org/wiki/Link_aggregation))--> qui est désormais une fonction standard assurant la redondance. L'autre option consiste à commander le serveur avec des liaisons montantes non bornées (sans agrégation de liaisons), puis à les remplacer par des liaisons montantes redondantes une fois le système d'exploitation installé.
{: note}

### Option 2 : Unité IPMI
{: #option-2}

Installez les systèmes d'exploitation sur des serveurs bare metal sans système d'exploitation en effectuant un démarrage à partir d'une image ISO via l'unité IPMI incluse. Pour plus d'informations sur le démarrage à partir d'une image ISO, voir [Montage d'une image ISO sur un serveur bare metal](/docs/bare-metal?topic=bare-metal-mounting-an-iso-on-a-bare-metal-server).
