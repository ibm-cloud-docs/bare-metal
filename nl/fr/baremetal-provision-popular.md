---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-02"

keywords: provision bare metal, popular servers, {{site.data.keyword.baremetal_short}}, provision

subcollection: bare-metal


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Sélection depuis les serveurs les plus populaires
{: #bm-select-popular-servers}

Les serveurs de la liste des serveurs les plus populaires sont préconfigurés afin de répondre aux besoins de la plupart des cas d'utilisation client, et ils sont prêts à s'exécuter sous 30 à 40 minutes après leur commande.
1. Ouvrez le [catalogue {{site.data.keyword.cloud_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/catalog/){: new_window}.   
2. Sélectionnez Serveur bare metal.
3. Cliquez sur Continuer.  Si vous ne voyez pas le bouton Continuer, vous devrez peut-être vous connecter.
2. Dans la section Serveurs bare metal, sélectionnez les informations suivantes :
    <table>
    <CAPTION>Tableau 1. Sélections bare metal</CAPTION>
    <THEAD>
    <TR>
    <th>Zone</th>
    <th>Valeur</th>
    </TR>
    </THEAD>
    <TBODY>
    <tr>
    <td>Quantité</td>
    <td>Utilisez les icônes + et - pour spécifier le nombre de serveurs **identiques** à mettre à disposition. La valeur par défaut est 1.<br>Si vous souhaitez mettre à disposition plusieurs serveurs avec des spécifications **différentes**, vous devez les mettre à disposition séparément.
    <tr>
    <tr>
    <td>Type de facturation</td>
    <td>Sélectionnez A l'heure ou Au mois
    <tr>
    <td>Nom d'hôte et domaine</td>
    <td>Ces zones sont renseignées par défaut. Vous pouvez les modifier.</td>
    </tr>
    <tr>
    <td>Emplacement</td>
    <td>Sélectionnez la région dans laquelle vous souhaitez que le serveur soit situé. A l'aide de la liste déroulante, sélectionnez un centre de données dans la région. </td>
    </tr>
    <tr>
    <tr>
    <td>Sélection de votre serveur</td>
    <td>Sélectionnez **Serveurs populaires** et sélectionnez le serveur qui correspond à vos besoins. Ces serveurs sont préconfigurés et prêts à l'emploi sous 30 à 40 minutes.
    </tr>
    <tr>
    <td>Mémoire RAM</td>
    <td>Valeur par défaut basée sur le serveur sélectionné.</td>
    </tr>
    <tr>
    <td>Clés SSH</td>
    <td>Fournit une clé publique de votre clé SSH, utilisée pour la connexion à votre serveur après sa mise à disposition.</td>
    </tr>
    <tr>
    <td>Image <br>(système d'exploitation)</td>
    <td>Sélectionnez le système d'exploitation du serveur. Vos options d'image peuvent être limitées en fonction du serveur sélectionné.</td>
    </tr>
    <td>Modules complémentaires</td>
    <td>Développez la section Modules complémentaires pour sélectionner les options appropriées ou utiliser les valeurs par défaut./td>
    </tr>
    </TBODY>
    </table>
3. Dans la section Disques de stockage, le disque de stockage est déjà sélectionné pour votre sélection dans Serveurs populaires. Développer la section Modules complémentaires si vous souhaitez ajouter IBM Cloud Backup à votre serveur.
4. Dans la section Interface réseau, sélectionnez Vitesses de port pour la liaison montante. Développez la section Modules complémentaires pour sélectionner les options appropriées ou utiliser les valeurs par défaut.
4.  Vérifiez votre commande.
4. Si vous disposez d'un code promotionnel à appliquer à votre commande, développez Appliquez votre code promotionnel.  
5.  Passez en revue tout contrat de service tiers répertorié, puis cochez la case **Contrat de service tiers**.
6.  Cliquez sur **Mettre à disposition**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

 Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée).

 L'_e-mail de mise à disposition de votre commande _ inclut un lien vers votre page *Détails de l'unité* pour que vous puissiez vous connecter à {{site.data.keyword.cloud_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.


## Etapes suivantes

Une fois votre serveur bare metal mis à disposition, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs bare metal](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
