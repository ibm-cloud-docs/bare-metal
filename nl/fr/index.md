---



copyright:
  years: 2018, 2018
lastupdated: "2018-06-18"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Initiation aux serveurs bare metal
{: #getting-started}

Les serveurs bare metal sont des serveurs physiques à service exclusif offrant performances et contrôle avec un accès de bas niveau aux ressources matériel. Vous n'avez pas à partager votre serveur avec des "voisins envahissants", il est tout à vous !
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
   <td><a href="https://console.bluemix.net/docs/admin/adminpublic.html#signing-up-for-ibm-cloud">Inscription à IBM Cloud</a> fournit la procédure de configuration de votre compte IBM Cloud.</td>
 <tr>
   <td>3. Déterminez vos spécifications de charge de travail</td>
   <td>Avant de mettre à disposition votre serveur, déterminez comment celui-ci sera utilisé, ainsi que la taille de serveur dont vous avez besoin pour un fonctionnement optimal. Prévoyez-vous, par exemple, de l'utiliser à des fins de développement et test ou de production ? Procédez-vous à un test des acquis utilisateur, traitez-vous des algorithmes assez longs, procédez-vous à la restauration et à la sauvegarde de données ou augmentez-vous la vitesse des temps d'attente ?</td>  
 <tr>
   <td>4. Déterminez la taille et le coût de votre serveur</td>
   <td>Vous pouvez utiliser l'<a href="https://www.ibm.com/cloud-computing/bluemix/bare-metal-search">outil de recherche bare metal</a> pour vous aider à évaluer la taille et le coût de votre serveur. </td>
 <tr>
   <td>5. Connectez-vous à votre compte IBM Cloud</td>
   <td>Vous pouvez accéder au formulaire de commande de serveur bare metal depuis le catalogue IBM Cloud ou le portail client de l'infrastructure IBM Cloud. Il vous faudra <a href="https://console.bluemix.net/docs/customer-portal/getting-started.html#getting-started">un IBMid et un mot de passe</a> pour accéder au catalogue et au portail client de l'infrastructure. <li><a href="https://console.bluemix.net/catalog/">Catalogue IBM Cloud</a></li>
   <li><a href="https://control.softlayer.com">Portail client de l'infrastructure IBM Cloud</a></li>  
   </td>   
<tr>   
   <td>6. Mettez à disposition votre serveur</td>
   <td>Trois options s'offrent à vous quant à la mise à disposition de votre serveur : classique, personnalisée et certifiée SAP. La version "classique" concerne des serveurs préconfigurés répondant aux besoins de la plupart des clients, et qui peuvent être prêts pour configuration 30 à 40 minutes après la mise à disposition. 
   
     
<br>Les serveurs personnalisés sont des serveurs que vous créez en sélectionnant des options spécifiques de calcul, connectivité, stockage et réseau afin de répondre à vos besoins. Il est à noté que la mise à disposition d'un serveur personnalisé nécessite davantage de temps, généralement entre 2 et 4 heures, et que les coûts de fonctionnement en sont plus élevés. Vous avez également la possibilité de <a href="bm_provision_ssd.html">mettre à disposition un serveur bare metal compatible Intel Optane</a> ou une <a href="bare-metal-provision-SGX.html">architecture Intel SGX</a>. 
     
<br>Les serveurs certifiés SAP ont été spécifiquement certifiés pour la prise en charge d'environnements SAP HANA et SAP NetWeaver.
Utilisez les liens concernant les informations de mise à disposition pour ce type de serveur. Remarque : Avec des serveurs certifiés SAP, vous devez sélectionner le type d'environnement, SAP HANA ou SAP NetWeaver, à mettre à disposition.  
  <li><a href="baremetal-provision-popular.html">Mise à disposition rapide de serveurs bare metal</a></li>
  <li><a href="baremetal-provision.html">serveurs bare metal personnalisés</a></li>
  <li><a href="bare-metal-sap-applications.html">IBM Cloud SAP-Certified Infrastructure</a></li>
  </td>
 <tr>
   <td>7. Configurez votre serveur bare metal</td>
   <td>Votre serveur est à présent prêt à être configuré. Voir les rubriques sous *Configuration*.</td>
   </td>
   </tr>
   </TBODY>
   </table>
