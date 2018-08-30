---

copyright:
  years: 1994, 2018
lastupdated: "2018-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Affectation d'adresses IP de serveur

{{site.data.keyword.cloud}} configure les serveurs avec une adresse IPv4
sur le réseau privé, une adresse IPv4 pour l'accès à la gestion de bas niveau sur
le réseau privé et, si nécessaire, une adresse IPv4 publique.
Au besoin, une adresse IPv6 sur le réseau public est disponible. Toutes ces adresses IP
sont appelées collectivement des **adresses IP principales**.

Des adresses IP supplémentaires peuvent être liées aux serveurs après l'achat de **sous-réseaux
secondaires** via le [Portail client ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com). Les adresses IP que vous avez achetées via le portail client
et que vous gérez vous-même sont appelées **adresses IP secondaires**.

Pour plus d'informations sur l'acquisition d'adresses IP, voir [Sous-réseaux et adresses IP](https://console.bluemix.net/docs/infrastructure/subnets/).


# Liaison d'adresses IP secondaires

Après que vous avez acheté un sous-réseau secondaire, vous devez
configurer le système d'exploitation pour l'utilisation d'une ou de plusieurs adresses IP. Chaque système d'exploitation configure les adresses IP différemment, mais on parle généralement de configuration d'"alias d'interface". 
