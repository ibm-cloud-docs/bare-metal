---



copyright:
  years: 2017, 2018
lastupdated: "2018-06-21"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Sélection depuis les serveurs les plus populaires
Les serveurs de la liste des serveurs les plus populaires sont préconfigurés afin de répondre aux besoins de la plupart des cas d'utilisation client, et ils sont prêts à s'exécuter sous 30 à 40 minutes après que vous les avez commandés.
1. Ouvrez le [catalogue {{site.data.keyword.cloud_notm}}](https://console.bluemix.net/catalog/){:target="_blank"}.   
2. Sélectionnez Serveur bare metal.
3. Cliquez sur Créer.
2. Sélectionnez les informations suivantes :
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
    <td>Utilisez les icônes + et - pour indiquer le nombre de serveur identiques à mettre à disposition.<br>Si vous souhaitez mettre à disposition plusieurs serveurs avec des spécifications différentes, vous devez les mettre à disposition séparément.
    <tr>
    <td>Emplacement</td>
    <td>Sélectionnez la région et le centre de données où vous souhaitez que le serveur soit localisé.</td>
    </tr>
    <tr>
    <tr>
    <td>Nom d'hôte et domaine</td>
    <td>Ces zones sont renseignées par défaut. Vous pouvez les modifier.</td>
    </tr>
    <tr>
    <td>Sélection de votre serveur</td>
    <td>Sous **Serveurs populaires**, sélectionnez le serveur répondant à vos besoins. Ces serveurs sont préconfigurés et prêts à l'emploi sous 30 à 40 minutes.
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
    <td>Sélectionnez le système d'exploitation pour l'instance. **Remarque** : Un message d'erreur s'affiche s'il existe un conflit entre le serveur et le système d'exploitation. Par exemple, la sélection de Linux sur un serveur Microsoft SQL.</td>
    </tr>
    <td>Vitesses de port Uplink</td>
    <td>Détermine la vitesse des interfaces internes et externes.</td>
    </tr>
    <tr>
    <td>Modules complémentaires</td>
    <td> Sélectionnez les options appropriées ou utilisez les valeurs par défaut.</td>
    </tr>
    </TBODY>
    </table>

3.  A la section du récapitulatif de commande, sélectionnez une facturation **Horaire** ou **Mensuelle**. 
4.  Vérifiez votre commande.
5.  Passez en revue tout contrat de service tiers répertorié, puis cochez la case **Contrat de service tiers**.
6.  Cliquez sur **Mettre à disposition**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

 Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). L'e-mail de mise à disposition de votre commande inclut un lien vers votre page *Détails de l'unité* pour que vous puissiez vous connecter à {{site.data.keyword.cloud_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.


## Etapes suivantes
Une fois votre serveur {{site.data.keyword.baremetal_short}} mis à disposition, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
