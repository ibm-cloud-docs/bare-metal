---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Sauvegarde et reprise

{{site.data.keyword.Bluemix_notm}} fournit diverses [solutions de sauvegarde et de stockage](https://www.softlayer.com/cloud-storage) évolutives adaptées à vos besoins en matière de sauvegarde. Toutefois, nous n'effectuons pas les sauvegardes des unités client. Un utilisateur de votre compte doit lancer toutes les sauvegardes planifiées et ponctuelles sur vos unités. 

Si au moins deux serveurs {{site.data.keyword.baremetal_short}} existent sur un compte, les données d'une unité peuvent être sauvegardées sur une autre. Il n'y a aucune limite de bande passante pour le trafic réseau privé, par conséquent, les données peuvent être transférées entre les unités ou sauvegardées sur n'importe quelle unité qui partage un compte.
Plusieurs solutions de sauvegarde sont disponibles pour {{site.data.keyword.baremetal_short}}, et notamment les suivantes : 

1. La [sauvegarde Evault](../infrastructure/backup/index.html) est une solution de sauvegarde d'entreprise qui peut automatiser les sauvegardes sur plusieurs serveurs. Les données sont stockées sur un réseau de stockage d'entreprise. 
* Le [stockage sur réseau](../infrastructure/network-attached-storage/nas.html) est une norme de l'industrie et fournit un espace de stockage hors du serveur pour les données critiques. Les données sont stockées sur un réseau de stockage d'entreprise. 
* [R1Soft CDP](../infrastructure/backup/r1soft.html) exécute une sauvegarde de serveur disque à disque à hautes performances, avec une fonction de gestion centralisée et un référentiel de données.
R1Soft CDP protège les données au niveau bloc, et des blocs disque uniques sur le serveur sont stockés une seule fois dans les points de reprise, ce qui augmente l'efficacité du stockage.

