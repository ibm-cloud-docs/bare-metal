---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Option Sans système d'exploitation

L'option Sans système d'exploitation permet de commander un serveur bare metal sans système d'exploitation. 

## Commande d'un serveur bare metal sans système d'exploitation

Commencez par commander un serveur bare metal via le site Web [SoftLayer.com](softlayer.com) ou le [portail client](https://control.softlayer.com).

1. Sélectionnez **Autre** à partir de **Configuration système > Système d'exploitation**.
2. Sélectionnez **Sans système d'exploitation**.

## Installation d'un système d'exploitation sur un serveur qui ne comporte pas de système d'exploitation

Deux méthodes permettent d'installer un système d'exploitation sur un serveur bare metal qui ne comporte pas de système d'exploitation. 

### Option 1 : Serveur PXE

Un serveur bare metal qui ne comporte pas de système d'exploitation peut être configuré pour démarrer et charger le système d'exploitation à partir d'une configuration PXE (pour plus d'informations, voir [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment)). Il suffit de déployer le serveur bare metal dans un environnement réseau avec une configuration PXE (cela implique généralement d'exécuter un démon DHCP et TFTP) et de configurer le nouveau système BIOS du serveur bare metal pour qu'il démarre à partir de l'adaptateur de réseau. Pour que cela fonctionne correctement, sachez que la configuration PXE doit figurer dans le même réseau local virtuel que la configuration PXE, ou bien l'acheminement DHCP doit être utilisé. 

**Remarque :** il peut s'avérer nécessaire de soumettre un ticket à l'équipe de support pour demander que les ports de commutation soient regroupés en mode de base et permettre à cette option de fonctionner. Cela est dû au fait que le protocole PXE ne requiert pas de compatibilité avec l'agrégation de liaisons (protocole LACP, voir [agrégation de liaisons](http://en.wikipedia.org/wiki/Link_aggregation)), qui est désormais une fonction standard assurant la redondance. L'autre option consiste à commander le serveur avec des liaisons montantes non bornées (sans agrégation de liaisons), puis à les remplacer par des liaisons montantes redondantes une fois le système d'exploitation installé. 

### Option 2 : Unité IPMI

Installez un système d'exploitation sur un serveur bare metal qui ne comporte pas de système d'exploitation en effectuant un démarrage à partir d'une image ISO via l'unité IPMI incluse. Cliquez [ici](mount-iso-bare-metal-server.html) pour obtenir davantage d'informations relatives au démarrage à partir d'une image ISO.
