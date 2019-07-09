---

copyright:
  years: 2016, 2019
lastupdated: "2019-06-19"

keywords: bare metal, bare metal servers, POWER8, SAP-certified, {{site.data.keyword.baremetal_long}}, {{site.data.keyword.baremetal_short}}, available bare metal, cascade lake

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:note: .note}

# A propos des serveurs bare metal
{: #about-bm}

Les serveurs bare metal IBM® Cloud constituent la base de votre solution d'infrastructure sous forme de service (IaaS). Que vous soyez un développeur de jeux ayant besoin d'un débit élevé d'entrées-sorties ou que vous ayez besoin de mettre en place des serveurs haute performance pour vos utilisateurs, les serveurs bare metal peuvent répondre à vos besoins.
{:shortdesc}

Votre serveur bare metal est un serveur à service exclusif horaire ou mensuel qui vous est dédié : il n'est partagé avec aucun autre client, y compris les ressources serveur. Vous gérez votre serveur, qui est mis à disposition sans hyperviseur et déployé sur un ou plusieurs centres de données. Plusieurs serveurs bare metal peuvent communiquer sur le réseau privé virtuel {{site.data.keyword.cloud_notm}} comme s'ils étaient positionnés sur le même rack.

## Un serveur pour chaque charge de travail
{: #servers-every-need}

{{site.data.keyword.cloud_notm}} propose un serveur bare metal pour répondre à chaque type de charge de travail. Pour plus d'informations, voir [Serveurs bare metal](https://www.ibm.com/cloud/bare-metal-servers){: external}

### Serveurs à mise à disposition rapide
{: #Popular-bm}

{{site.data.keyword.cloud_notm}} propose des serveurs préconfigurés répondant aux besoins de la plupart des cas d'utilisation. Ces serveurs sont considérés comme étant "à mise à disposition rapide" car vos options de calcul (nombre de coeurs, vitesse, mémoire RAM et nombre d'unités) sont prédéfinies. Les serveurs prédéfinis sont prêts à être configurés 30 à 40 minutes après leur mise à disposition. 

### Serveurs basés sur le client
{: #custom-based-bm}

Si aucun des serveurs de mise à disposition rapide ne répond à vos besoins en charge de travail, vous pouvez personnaliser votre serveur bare metal pour répondre à vos besoins. Les serveurs personnalisés sont mis à disposition sous 2 à 4 heures et offrent une grande variété en matière de coeurs, vitesses, RAM et unités. 

### Serveurs POWER8 personnalisés
{: #bm-power8}

{{site.data.keyword.cloud_notm}} vous offre la possibilité de mettre à disposition un serveur bare metal à processeur IBM POWER8. Les serveurs POWER8 sont construits avec le processeur POWER8 et une plateforme basée OpenPower, réglée spécifiquement pour des déploiements en cloud de charges de données, cognitives et Web sous Linux. Pour plus d'informations, voir [POWER8 Servers](https://www.ibm.com/cloud/bare-metal-servers/power){: external}.

### Serveurs bare metal certifiés SAP
{: #bm-SAP-cert}

Les serveurs {{site.data.keyword.cloud_notm}} bare metal sont certifiés pour la prise en charge de vos charges de travail SAP HANA et SAP NetWeaver. Pour plus d'informations, voir [Infrastructure certifiée SAP](https://www.ibm.com/cloud/sap/certified-infrastructure){: external}.

## Options de serveurs bare metal disponibles<!--test new section - test as each option goes GA-->
{: #options-for-bare-metal-servers}
{{site.data.keyword.cloud_notm}} offre des options de serveurs bare metal que vous pouvez personnaliser pour répondre à vos besoins.

### Prise en charge de l'unité centrale Intel Cascade Lake 
<!--Need to add which servers are also available for SAP once the certification is done-->
Lorsque vous mettez à disposition un serveur bare metal, vous pouvez choisir l'une des unités centrales Intel Cascade Lake suivantes :

* Intel Xeon 4210 (10 coeurs, 2,2 GHz, 85 W)
* Intel Xeon 5218 (16 coeurs, 2,3 GHz, 125 W)
* Intel Xeon 6248 (20 coeurs, 2,6 GHz, 150 W)
<!--Intel Xeon 8280M (28-Core, 2.7 GHz, 205 W)--><br>

<br>Les processeurs Cascade Lake sont disponibles dans les centres de données suivants :

<table style="width:100%">
<CAPTION>Tableau 1. Centres de données avec processeurs Cascade Lake</CAPTION>
 <tr>
   
   <th colspan="6">Centres de données</th>
 </tr>
 <tr>
   <td>DAL10</td>
   <td>FRA02</td>
   <td>LON04</td>
   <td>SYD01</td>
   <td>TOK02</td>
   <td>WDC04</td>
   
</tr>

<tr>
  <td>DAL12</td>
  <td>FRA04</td>
  <td>LON05</td>
  <td>SYD04</td>
  <td>TOK04</td>
  <td>WDC06</td>
  
</tr>

<tr>
  <td>DAL13</td>
  <td>FRA05</td>
  <td>LON06</td>
  <td>SYD05</td>
  <td>TOK05</td>
  <td>WDC07</td>
</tr>
</table>


### Inventaire dynamique 
{: #bm-dynamic-inv}

Vous pouvez maintenant voir quels serveurs sont disponibles dans quel centre de données lorsque vous mettez à disposition un serveur bare metal. Cependant, cette option n'est disponible que pour l'offre horaire. Vous ne pouvez pas voir la disponibilité du serveur avec l'offre mensuelle. Pour en savoir plus sur la mise à disposition d'un serveur bare metal, voir [Sélection depuis les serveurs les plus populaires](/bare-metal?topic=bare-metal-bm-select-popular-servers).

### Module complémentaire de stockage de blocs et de fichiers
{: #bm-block-and-file-add-on}

Si vous avez besoin de stockage supplémentaire, {{site.data.keyword.IBM_notm}} vous simplifie la tâche ! Vous pouvez maintenant commander un stockage de blocs et de fichiers (20 - 12 000 Go) lorsque vous mettez à disposition un serveur bare metal. 

Votre stockage supplémentaire n'est pas automatiquement connecté à votre serveur bare metal. Vous devez connecter l'espace de stockage supplémentaire à votre serveur bare metal après la mise à disposition de votre serveur.
{: note} 

<!--The add-on storage shares the data center that your bare metal server is on.-->

Pour plus d'informations sur le stockage de blocs et de fichiers, voir les liens suivants.
* [A propos du stockage de blocs](/docs/infrastructure/BlockStorage?topic=BlockStorage-About)
* [A propos du stockage de fichiers](/docs/infrastructure/FileStorage?topic=FileStorage-about)
