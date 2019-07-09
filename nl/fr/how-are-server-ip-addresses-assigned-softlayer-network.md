---

copyright:
  years: 1994, 2019
lastupdated: "2019-06-17"

keywords: server IP addresses, bare metal, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Affectation et liaison d'adresses IP
{: #bm-assigning-and-binding-ip-addresses}

Utilisez les informations suivantes pour affecter une adresse IP de serveur à votre serveur et lier une adresse IP secondaire à votre serveur, au besoin.
{: shortdesc}

## Affectation d'adresses IP de serveur
{: #bm-assign-ip-address}

{{site.data.keyword.cloud}} configure les serveurs avec les adresses suivantes :
une adresse IPv4 sur le réseau privé;
une adresse IPv4 pour l'accès de gestion de faible niveau sur le réseau privé;
une adresse IPv4 publique, si nécessaire.

Au besoin, une adresse IPv6 sur le réseau public est disponible. Toutes ces adresses IP
sont appelées collectivement des **adresses IP principales**.

Des adresses IP supplémentaires peuvent être liées aux serveurs après l'achat de **sous-réseaux secondaires** via la console [{{site.data.keyword.cloud_notm}} ](https://cloud.ibm.com){: external}. Les adresses IP que vous avez achetées via le portail client
et que vous gérez vous-même sont appelées **adresses IP secondaires**.

Pour plus d'informations sur l'acquisition d'adresses IP, voir [Sous-réseaux et adresses IP](https://cloud.ibm.com/docs/infrastructure/subnets/){: external}.


## Liaison d'adresses IP secondaires
{: #bm-bind-secondary-ip-address}

Après avoir acheté un sous-réseau secondaire, vous devez configurer le système d'exploitation pour l'utilisation d'une ou de plusieurs adresses IP. Chaque système d'exploitation configure les adresses IP différemment, mais on parle généralement de configuration d'"alias d'interface".
