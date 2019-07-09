---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-16"

keywords: bare metal, getting started, {{site.data.keyword.cloud}}, {{site.data.keyword.cloud_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Tutoriel de mise en route
{: #getting-started}

Les serveurs bare metal IBM® Cloud sont des serveurs physiques à service exclusif offrant performances et contrôle avec un accès de bas niveau aux ressources matériel. Vous n'avez pas à partager votre serveur avec des "voisins envahissants", il est tout à vous !
{: shortdesc}

Le tableau 1 contient des étapes pour vous aider à rapidement mettre à disposition et configurer votre serveur bare metal.
<table>
   <CAPTION>Tableau 1. Etapes de démarrage rapide</CAPTION>
   <THEAD>
   <TR>
   <th>Tâche</th>
   <th>Détails</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>1. Vérifiez le contenu pouvant vous aider pour votre implémentation</td>
   <td>Nouveaux serveurs IBM Cloud et bare metal ? Les sites suivants fournissent des informations utiles pour planifier votre environnement.
   <li><a href="https://ibm.com/cloud-computing/">What is IBM Cloud</a></li>
   <li><a href="https://ibm.com/cloud/get-started">Getting started with IBM Cloud</a></li>
   <li><a href="https://www.ibm.com/cloud/bare-metal-servers">Bare Metal Servers</a></li>
   </td>
 <tr>
   <td>2. Inscrivez-vous à IBM Cloud</td>
   <td><a href="https://cloud.ibm.com/docs/account?topic=account-signup#signing-up-for-ibm-cloud">Inscription à IBM Cloud</a> fournit la procédure de configuration de votre compte IBM Cloud.</td>
 <tr>
   <td>3. Déterminez vos spécifications de charge de travail</td>
   <td>Avant de mettre à disposition votre serveur, déterminez comment il sera utilisé et la taille du serveur dont vous avez besoin. Prévoyez-vous, par exemple, de l'utiliser à des fins de développement et test ou de production ? Procédez-vous à un test des acquis utilisateur, traitez-vous des algorithmes assez longs, procédez-vous à la restauration et à la sauvegarde de données ou augmentez-vous la vitesse des temps d'attente ?</td>  
 <tr>
   <td>4. Déterminez la taille et le coût de votre serveur</td>
   <td>Vous pouvez utiliser l'<a href="https://cloud.ibm.com/gen1/infrastructure/provision/bm">outil de recherche bare metal</a> pour vous aider à évaluer la taille et le coût de votre serveur.</td>
 <tr>
   <td>5. Connectez-vous à votre compte IBM Cloud</td>
   <td>Vous pouvez accéder au formulaire de commande de serveur bare metal depuis le catalogue IBM Cloud ou le portail client de l'infrastructure IBM Cloud. Il vous faudra <a href="https://cloud.ibm.com/docs/customer-portal?topic=customer-portal-getting-started#getting-started">un IBMid et un mot de passe</a> pour accéder au catalogue et au portail client de l'infrastructure.
   <li><a href="https://cloud.ibm.com/catalog/">Catalogue IBM Cloud</a></li>
   <li><a href="https://cloud.ibm.com">Console IBM Cloud</a></li>  
   </td>   
<tr>   
   <td>6. Mettez à disposition votre serveur</td>
   <td>Trois types de mise à disposition existent pour votre serveur : la mise à disposition rapide, personnalisée et certifiée SAP. Les serveurs "à mise à disposition rapide" sont des serveurs préconfigurés qui répondent aux besoins de la plupart des clients, et qui peuvent être configurés 30 à 40 minutes après leur mise à disposition.


<br>Les serveurs personnalisés sont des serveurs que vous créez en sélectionnant des options spécifiques de calcul, de connectivité, de stockage et de réseau afin de répondre à vos besoins. La mise à disposition d'un serveur personnalisé nécessite davantage de temps, généralement entre 2 et 4 heures, et les coûts de fonctionnement sont plus élevés. Vous pouvez [mettre à disposition un serveur bare metal compatible avec Intel Optane](/docs/bare-metal?topic=bare-metal-provisioning-an-intel-optane-compatible-bare-metal-server#provisioning-an-intel-optane-compatible-bare-metal-server) ou une [architecture Intel SGX](/docs/bare-metal?topic=bare-metal-provisioning-a-bare-metal-server-with-intel-sgx-architecture#provisioning-a-bare-metal-server-with-intel-sgx-architecture).

<br>Les serveurs certifiés SAP sont certifiés pour prendre en charge les paysages SAP HANA et SAP NetWeaver.
Utilisez les liens concernant les informations de mise à disposition pour ce type de serveur. Notez qu'avec les serveurs certifiés SAP, vous devez sélectionner le type de paysage (SAP HANA ou SAP NetWeaver) que vous mettez à disposition. <br>
* [Mise à disposition rapide de serveurs bare metal](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers)<br>
* [Serveurs bare metal personnalisés](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server#ordering-baremetal-server)<br>
* [Infrastructure IBM Cloud certifiée SAP](/docs/bare-metal?topic=bare-metal-ibm-cloud-sap-certified-infrastructure#ibm-cloud-sap-certified-infrastructure)
  </td>
 <tr>
   <td>7. Configurez votre serveur bare metal</td>
   <td>Votre serveur est à présent prêt à être configuré. Voir les rubriques sous **Configuration**.</td>
   </td>
   </tr>
   </TBODY>
   </table>
