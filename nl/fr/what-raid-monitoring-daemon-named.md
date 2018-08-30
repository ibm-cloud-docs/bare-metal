---
copyright:
  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Nom et emplacement du démon de surveillance RAID
{{site.data.keyword.cloud}} utilise principalement des cartes Adaptec et LSI RAID à quelques exceptions près pour le matériel existant. Le tableau ci-après présente les emplacements de gestionnaire RAID, les emplacements de moniteur, les configurations et les paramètres d'alerte RAID. 

Vous pouvez configurer des alertes RAID afin d'ignorer le processus de surveillance du portail en modifiant le serveur SMTP et la destination du courrier électronique de notification dans la configuration d'une carte RAID. Si vous modifiez ces configurations, IBM ne peut pas vous avertir des problèmes RAID ou suivre automatiquement les problèmes jusqu'à leur résolution. Ne modifiez pas la configuration fournie sauf si vous êtes conscient des risques encourus.

<caption>Tableau 1. Configurations et paramètres RAID</caption>

||LSI Linux|LSI Windows|Adaptec Linux|Adaptec Windows|
|---|---|---|---|---|
|**Nom de gestionnaire**|LSI MegaRAID Storage Manager|LSI MegaRAID Storage Manager|Adaptec Storage Manager|Adaptec Storage Manager|
|**Emplacement de gestionnaire**|/opt/MegaRAID/storcli|C:\Program Files (x86)\MegaRAID Storage Manager|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Nom de moniteur**|MR_Monitor|MRMonitor|Adaptec Event Manager|Adaptec Event Manager|
|**Emplacement de moniteur**|/opt/lsi/mrmonitor/bin/mrmonitord|C:\Program Files (x86)\LSI\MRMonitor|/usr/StorMan|C:\Program Files\Adaptec\Adaptec Storage Manager|
|**Nom de processus**|/opt/lsi/mrmonitor/bin/mrmonitord|||||
|**Emplacement de journal**|Emplacement de journal des messages par défaut pour le système d'exploitation, par exemple, /var/log/messages|Interface graphique uniquement|/usr/StorMan/RaidEvtA.log|Interface graphique uniquement|
|**Destination du courrier électronique de notification**|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|[hwraid@softlayer.com](mailto:hwraid@softlayer.com)|
|**Format source du courrier électronique de notification**|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|accountid_privatemac<br /><br />@softlayer.com|
|**Port de messagerie**|25|25|25|25|
|**Serveur SMTP**|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|raidalerts-smtp.networklayer.com|
|**Autres options de notification**|Remplacer le serveur SMTP par un serveur SMTP local. Le serveur SMTP local a besoin des configurations de pare-feu appropriées. |Remplacer le serveur SMTP par un serveur SMTP local. Le serveur SMTP local a besoin des configurations de pare-feu appropriées. |Remplacer le serveur SMTP par un serveur SMTP local. Le serveur SMTP local a besoin des configurations de pare-feu appropriées. |Remplacer le serveur SMTP par un serveur SMTP local. Le serveur SMTP local a besoin des configurations de pare-feu appropriées. |
