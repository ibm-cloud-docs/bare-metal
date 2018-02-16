---



copyright:
  years: 2017
lastupdated: "2017-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Mise à disposition d'un serveur bare metal

## Avant de commencer
Deux possibilités s'offrent à vous si vous souhaitez mettre à disposition votre {{site.data.keyword.baremetal_long}} public. Vous pouvez utiliser soit le catalogue {{site.data.keyword.cloud}} soit le portail {{site.data.keyword.slportal_full}}. Des ID de connexion uniques sont requis pour le catalogue et le portail {{site.data.keyword.slportal}}. Le nom d'utilisateur et le mot de passe du catalogue ne fonctionnent pas pour la connexion au portail et vice-versa.
{:shortdesc}

Avant de commencer, vérifiez que vos données d'identification pour le catalogue {{site.data.keyword.cloud_notm}} ou le portail {{site.data.keyword.slportal}} ont été définies.  
  
**Remarque :** pour le catalogue {{site.data.keyword.cloud_notm}}, vous devez posséder un compte ayant été mis à niveau afin de pouvoir commander {{site.data.keyword.baremetal_short}}. Pour plus d'informations sur la mise à niveau d'un compte, voir [Switching to IBMid](https://console.ng.bluemix.net/docs/admin/softlayerlink.html).
  
## Connexion 
Vérifiez que vous êtes connecté, via le catalogue {{site.data.keyword.cloud_notm}} ou le portail {{site.data.keyword.slportal}} : 

  <table>
   <CAPTION>Tableau 1. Choix d'un emplacement de connexion</CAPTION>
   <THEAD>
   <TR>
   <th>Connexion à</th>
   <th>Procédure</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>IBM Cloud Catalog</td>
   <td>
   <ol>
   <li>Ouvrez une fenêtre de navigateur et entrez <a href="https://console.bluemix.net/catalog/">https://console.bluemix.net/catalog/</a>.</li>
   <li>Cliquez sur le lien <b>Se connecter</b>. </li>
   <li>Entrez votre adresse électronique ou votre IBMid, puis cliquez sur <b>Continuer</b>.</li>
   <li>Entrez votre mot de passe, puis cliquez sur <b>Se connecter.</b></li>
   <li>Sélectionnez <b>Infrastructure</b> > <b>Calcul</b>.</li>
   <li>Cliquez sur la vignette <b>{{site.data.keyword.baremetal_short}}</b>.</li>
   <li>Cliquez sur <b>Créer</b>. La page principale du portail {{site.data.keyword.slportal}} s'affiche.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Portail client</td>
   <td>
   <ol>
   <li>Ouvrez une nouvelle fenêtre de navigateur et entrez <a href="https://control.softlayer.com">https://control.softlayer.com</a>.</li>
   <li>Entrez votre nom d'utilisateur et votre mot de passe puis cliquez sur <b>Se connecter</b>. Ou, cliquez sur <b>Connexion par ID IBM</b>. Entrez ensuite votre adresse électronique ou votre ID IBM puis cliquez sur <b>Continuer</b>. Entrez votre mot de passe puis cliquez sur <b>Se connecter</b>. La page principale du portail {{site.data.keyword.slportal}} s'affiche.</li>
   </ol>
   </td>
   </tr>
   </TBODY>
   </table>

## Mise à disposition d'un serveur bare metal
{: #ordering-baremetal-server}
Une fois connecté, vous pouvez commencer à mettre à disposition un serveur {{site.data.keyword.baremetal_short}}. Vous pouvez mettre à disposition votre serveur{{site.data.keyword.baremetal_short}} à l'aide du menu **Equipements** ou de l'icône **Equipements**. 

### Mise à disposition d'un serveur bare metal à l'aide de l'icône Equipements
Pour mettre à disposition votre serveur {{site.data.keyword.baremetal_short}} à l'aide de l'icône *Equipements*, procédez comme suit :

1.  Dans le portail {{site.data.keyword.slportal}}, recherchez la section **Commande**, puis cliquez sur **Equipements**.
2.  Sur cette page, cliquez sur **Horaire** ou **Mensuel** sous {{site.data.keyword.baremetal_short}}.
3.  Sélectionnez votre **centre de données**, faites défiler la page, puis cliquez sur le lien **Prix de départ** afin de choisir votre serveur.  
4.  Renseignez la page **Configurez votre {{site.data.keyword.baremetal_short}}**, puis cliquez sur le bouton **Ajouter à la commande** pour continuer. Pour plus d'informations sur la procédure de configuration de votre serveur, voir [Configuration de votre serveur {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md). Une fois votre commande vérifiée, vous serez redirigé vers la page de **paiement**. 
5.  Renseignez la zone **Configuration système avancé** pour le serveur. Pour plus d'informations sur la procédure de configuration, voir [Configuration de votre serveur {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md). 
6.  Cochez les cases **Conditions des services Cloud** et **Contrat de service tiers**. 
7.  Confirmez ou entrez vos informations de paiement puis cliquez sur le bouton **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

 Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page *Détails de l'unité* après la connexion à {{site.data.keyword.cloud_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.

### Mise à disposition d'un serveur bare metal à l'aide du menu Equipements
{: #ordering-baremetal-devices-menu}

Vous pouvez également mettre à disposition votre serveur {{site.data.keyword.baremetal_short}} à l'aide du menu *Equipements* sur la page principale du portail {{site.data.keyword.slportal}}.  

1. Cliquez sur **Equipements > Liste des unités**. La page Equipements affiche tous les types de terminal (hôtes dédiés, serveurs virtuels, serveurs bare metal et contrôleurs de distribution d'application NetScaler) de votre compte.
2. Cliquez sur le lien **Commander unités** dans le coin supérieur droit.
3. Sur la page Commander les produits et services de SoftLayer, cliquez sur **Horaire** ou **Mensuel** sous {{site.data.keyword.baremetal_short}}.
4. Sélectionnez votre **centre de données**, faites défiler la page, puis cliquez sur le lien **Prix de départ** afin de choisir votre serveur.  
5.  Renseignez la page **Configurez votre {{site.data.keyword.baremetal_short}}**, puis cliquez sur le bouton **Ajouter à la commande** pour continuer. Pour plus d'informations sur la procédure de configuration de votre serveur, voir [Configuration de votre serveur {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md). Une fois votre commande vérifiée, vous serez redirigé vers la page de **paiement**. 
6.  Renseignez la zone **Configuration système avancé** pour le serveur. Pour plus d'informations sur la procédure de configuration, voir [Configuration de votre serveur {{site.data.keyword.baremetal_short}}](../bare-metal/configuring.md). 
7. Cochez les cases **Conditions des services Cloud** et **Contrat de service tiers**. 
8. Confirmez ou entrez vos informations de paiement puis cliquez sur le bouton **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien vous dirigeant directement vers la page *Détails de l'unité* après la connexion à {{site.data.keyword.cloud_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.

### Etapes suivantes
Une fois votre serveur {{site.data.keyword.baremetal_short}} mis à disposition, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
