---



copyright:
  years: 2016
lastupdated: "2016-01-19"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Initiation aux serveurs {{site.data.keyword.baremetal_short}}

Les serveurs {{site.data.keyword.baremetal_long}} sont performants et vous offrent davantage de contrôle. Les serveurs {{site.data.keyword.baremetal_short}} ne s'exécutent pas dans un hyperviseur et vous obtenez un accès de bas niveau aux ressources matériel. De plus, vous ne partagez le serveur avec personne d'autre, il est tout à vous !
{:shortdesc}

Lorsque vous créez un serveur {{site.data.keyword.baremetal_short}}, vous pouvez personnaliser les spécifications des processeurs et de la région sur le système d'exploitation et le disque dur. 

Pour mettre à disposition un serveur {{site.data.keyword.baremetal_short}} :
  1. Accédez à **Calcul > {{site.data.keyword.baremetal_short}}** et cliquez sur **Ajouter**.
  2. Sélectionnez l'emplacement où vous souhaitez mettre à disposition l'instance {{site.data.keyword.baremetal_short}}. Il s'agit d'un centre de données dans l'une des régions {{site.data.keyword.Bluemix}}. 
  3. Sélectionnez la configuration des serveurs. Cette configuration s'applique à tous les serveurs créés pour cette instance.
  4. Sélectionnez le nombre de serveurs que vous souhaitez créer pour cette instance. Pour chaque serveur, entrez un nom d'hôte unique. 
  5. **Facultatif :** entrez une adresse URL vers un script ou un fichier texte que vous avez défini pour configurer le serveur. Le script de mise à disposition doit utiliser un protocole HTTPS. Le script sera téléchargé et exécuté une fois l'instance mise à disposition, si possible. Si l'adresse URL n'est pas associée à un script exécutable, le script est simplement téléchargé. 
  6. Sélectionnez le système d'exploitation pour les serveurs. Ce système d'exploitation s'applique à tous les serveurs créés pour cette instance. 

Au bout d'une heure, votre {{site.data.keyword.baremetal_short}} est mis à disposition et prêt à être utilisé. 
