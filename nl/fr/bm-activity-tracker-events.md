---

copyright:
  years: 2016, 2019
lastupdated: "2018-11-06"

keywords: activity tracker, bare metal, {{site.data.keyword.Bluemix}}

subcollection: bare-metal

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Evénements d'Activity Tracker
{: #bm-at-events}

En tant que responsable de la sécurité, auditeur ou gestionnaire, vous pouvez utiliser le service {{site.data.keyword.cloudaccesstrailfull}} pour déterminer comment les utilisateurs et les applications interagissent avec les serveurs bare metal dans {{site.data.keyword.Bluemix}}. Le propriétaire du compte et les utilisateurs associés au compte peuvent déclencher des événements de serveur bare metal qui sont consignés dans {{site.data.keyword.cloudaccesstrailshort}}.
{:shortdesc}

Le service {{site.data.keyword.cloudaccesstrailshort}} enregistre les activités lancées par l'utilisateur qui modifient l'état d'un service dans {{site.data.keyword.Bluemix_notm}}. Pour plus d'informations, voir [A propos d'{{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov ).

Pour commencer à surveiller les actions de vos utilisateurs, voir [Initiation à IBM Cloud Activity Tracker](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started#getting-started).

L'initiateur peut être un utilisateur, un service ou une application. Pour qu'un utilisateur puisse générer des événements, il doit avoir accès aux ressources **d'infrastructure** dans la console {{site.data.keyword.Bluemix}}.
{: tip}

## Evénements d'instances de serveurs bare metal
{: #bare-metal-events}

Vous pouvez auditer un serveur bare metal tout au long de son cycle de vie à l'aide du service {{site.data.keyword.cloudaccesstrailshort}}.

Le tableau suivant répertorie les actions qui génèrent un événement :

| Action | Description |
|----------|---------|
| `audit-log.bare-metal.provision`             | Un événement est généré lorsqu'un initiateur met à disposition un serveur bare metal.  |
| `audit-log.bare-metal-port.disable`          | Un événement est généré lorsqu'un initiateur désactive un port dans un serveur bare metal. |
| `audit-log.bare-metal-port.enable`           | Un événement est généré lorsqu'un initiateur active un port dans un serveur bare metal. |
| `audit-log.bare-metal-port-speed.update`     | Un événement est généré lorsqu'un initiateur met à jour la vitesse de port dans un serveur bare metal. |
| `audit-log.bare-metal.power-off`             | Un événement est généré lorsqu'un initiateur met hors tension un serveur bare metal.  |
| `audit-log.bare-metal.reboot`                | Un événement est généré lorsqu'un initiateur redémarre un serveur bare metal. |
| `audit-log.bare-metal.soft-reboot`           | Un événement est généré lorsqu'un initiateur effectue un redémarrage logiciel (graduel) sur un serveur bare metal. |
| `audit-log.bare-metal.hard-reboot`           | Un événement est généré lorsqu'un initiateur effectue un redémarrage matériel (immédiat) sur un serveur bare metal. |
| `audit-log.bare-metal.power-on`              | Un événement est généré lorsqu'un initiateur met sous tension un serveur bare metal. |
| `audit-log.bare-metal.rename`                | Un événement est généré lorsqu'un initiateur renomme un serveur bare metal. |
| `audit-log.bare-metal.rescue`                | Un événement est généré lorsqu'un initiateur récupère un serveur bare metal. |
| `audit-log.bare-metal.reload`                | Un événement est généré lorsqu'un initiateur effectue un rechargement du système d'exploitation pour un serveur bare metal. |
{: caption="Tableau 2. Actions sur les serveurs bare metal" caption-side="top"}


## Affichage des événements
{: #bm-view-events}

Les événements d'{{site.data.keyword.cloudaccesstrailshort}} sont disponibles dans le **domaine de compte** d'{{site.data.keyword.cloudaccesstrailshort}} dans la région {{site.data.keyword.Bluemix_notm}} dans laquelle les événements sont générés. Pour plus d'informations, voir [Affichage des événements
de compte](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events).

Les événements d'{{site.data.keyword.cloudaccesstrailshort}} sont automatiquement renvoyés au service {{site.data.keyword.cloudaccesstrailshort}} dans la région dans laquelle l'action se produit.
