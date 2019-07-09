---

copyright:
  years: 1994, 2019
lastupdated: "2019-05-02"

keywords: back up, recovery, IBM Cloud Backup, r1soft

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Sauvegarde et reprise
{: #sm-back-up-recovery}

{{site.data.keyword.Bluemix_notm}} offre diverses [solutions de sauvegarde et de stockage ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/cloud/storage){: new_window} évolutives adaptées à vos besoins en matière de sauvegarde. Toutefois, {{site.data.keyword.Bluemix_notm}} n'effectue pas les sauvegardes des unités client. Un utilisateur de votre compte doit lancer toutes les sauvegardes planifiées et ponctuelles sur vos unités.

Si au moins deux serveurs {{site.data.keyword.baremetal_short}} existent sur un compte, les données d'une unité peuvent être sauvegardées sur une autre. Aucune limite de bande passante n'est appliquée pour le trafic réseau privé, par conséquent, les données peuvent être transférées entre les unités ou sauvegardées sur n'importe quelle unité qui partage un compte. Plusieurs solutions de sauvegarde sont disponibles pour {{site.data.keyword.baremetal_short}}, et notamment les suivantes :

* [IBM Cloud Backup](/docs/infrastructure/Backup?topic=Backup-getting-started#getting-started) est une solution de sauvegarde pour entreprise qui permet d'automatiser les sauvegardes sur plusieurs serveurs. Les données sont stockées sur un réseau de stockage d'entreprise.
* Le [stockage sur réseau](/docs/infrastructure/network-attached-storage?topic=network-attached-storage-GettingStarted#GettingStarted) est une norme de l'industrie et fournit un espace de stockage hors du serveur pour les données critiques. Les données sont stockées sur un réseau de stockage d'entreprise.
* [R1Soft CDP](/docs/infrastructure/software?topic=software-ordering-r1soft#ordering-r1soft) exécute une sauvegarde de serveur disque à disque à hautes performances, avec une fonction de gestion centralisée et un référentiel de données. R1Soft CDP protège les données au niveau bloc, et des blocs disque uniques sur le serveur sont stockés une seule fois dans les points de reprise, ce qui augmente l'efficacité du stockage.
