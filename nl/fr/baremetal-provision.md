---



copyright:
  years: 2017, 2018
lastupdated: "2018-07-06"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Génération d'un serveur bare metal personnalisé
{: #ordering-baremetal-server}

Utilisez la procédure suivante pour générer un serveur bare metal personnalisé.

1. Ouvrez le [catalogue {{site.data.keyword.cloud_notm}}](https://console.bluemix.net/catalog/){:target="_blank"}.   
2. Sélectionnez Serveur bare metal.
3. Cliquez sur Créer.
4. Dans la liste des serveurs ci-après, recherchez l'instruction **Intéressé par d'autres options de configuration ? Cliquez ici**. Sélectionnez cette option. Le formulaire de serveur personnalisé s'affiche.
1. Sélectionnez un emplacement de centre de données pour votre serveur.
* Sélectionnez un serveur parmi les trois catégories proposées en cliquant sur le lien **Prix de départ par**.
  * Serveurs certifiés SAP (Pour plus d'informations sur la mise à disposition d'un serveur certifié SAP, voir [Infrastructure certifiée SAP {{site.data.keyword.cloud_notm}}](/docs/bare-metal/bare-metal-sap-applications.html))
  * Serveurs multicoeur à processeur unique
  * Serveurs multicoeur à processeur double

* Choisissez parmi vos options de configuration. **Centre de données**, **Mémoire RAM** et **Système d'exploitation** sont des zones obligatoires. Toutes les autres zones sont facultatives. Pour plus d'informations sur les zones facultatives, reportez-vous aux **[options supplémentaires de configuration du serveur](#addl-server-options)**.

    **Remarque** : Un message d'erreur s'affiche s'il existe un conflit entre le serveur et le système d'exploitation. Par exemple, la sélection de Linux sur un serveur Microsoft SQL.
* Cliquez sur **Ajouter à la commande**. La page Paiement s'affiche.

  Depuis la page de réservation, vous pouvez revenir à la page de configuration en cliquant sur l'une des options de reconfiguration.
* A la section Configuration système avancée, spécifiez des options de configuration supplémentaires. Pour plus d'informations, voir **[Configuration système avancée](#adv-system-config)**.

*   Cochez les cases **Conditions des services Cloud** et **Contrat de service tiers**.
*   Confirmez ou entrez vos informations de paiement et cliquez sur **Soumettre commande**. Un écran incluant votre numéro de commande de mise à disposition s'affiche. Vous pouvez imprimer cette page car il s'agit de votre reçu de commande de mise à disposition.

  Vous pouvez également sauvegarder la commande sans effectuer d'achat en cliquant sur **Enregistrer sous devis**.

 Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). L'e-mail de mise à disposition de votre commande inclut un lien vers votre page *Détails de l'unité* une fois que vous vous connectez à {{site.data.keyword.cloud_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.

 ## Options de configuration de serveur supplémentaires
 {: #addl-server-options}

 D'autres options sont disponibles lorsque vous mettez à disposition votre serveur bare metal, par exemple la bande passante publique, la vitesse de port uplink, des adresses IP secondaires publiques, etc. Le Tableau 1 décrit ces options supplémentaires. 


 | **Zone** | **Description** |
 |-------------------|---------------|
 |Sécurité du serveur|Telle que Trusted Execution Technology (Intel TXT)|
 |Software Guard Extensions|Sécurité accrue pour le code et les données sensibles (Intel SGX). <br><br>Voir [Mise à disposition d'un serveur bare metal avec Intel SGX](../bare-metal/bare-metal-provision-SGX.html).|
 |Mémoire RAM|Choisissez un niveau de RAM répondant aux besoins de votre serveur.|
 |Système d'exploitation |Faites votre choix parmi CentOS, FreeBSD, Microsoft, Red Hat, Ubuntu ou Autre. |
 |Disques durs |L'utilisation de l'outil dans l'interface utilisateur configure vos disques durs en préremplissant les zones en fonction du système d'exploitation sélectionné. <br><br> Vous pouvez également choisir d'utiliser une unité SSD Intel Optane. Voir [Mise à disposition d'une unité Intel Optane SSD DC P4800X](../bare-metal/bm-provision_ssd.html).
 |Bande passante publique |Détermine la quantité de données pouvant être transférée via l'interface publique durant un mois. Pour les environnements de test pour lesquels des données d'installation doivent être transférées via cette interface, les valeurs doivent être adaptées au-delà de la quantité de données transférées initialement. Prenez en compte le [réseau {{site.data.keyword.cloud_notm}} Content Delivery Network](https://www.ibm.com/cloud/cdn) afin d'expédier un chargement de données initial à l'un des centres de données {{site.data.keyword.cloud_notm}}. N'importe quel serveur {{site.data.keyword.baremetal_short}} peut être mis à niveau pour inclure une bande passante non mesurée (illimitée). Toutes les unités non mesurées sont sur des ports dédiés privés.|
 |Vitesses de port Uplink |Détermine la vitesse des interfaces internes et externes. |
 |Adresses IP secondaires publiques |Affecte d'autres adresses IP à votre serveur. En fonction de votre scénario, vous aurez besoin que d'autres adresses IP soient affectées à votre serveur. Des adresses IPv4 supplémentaires sont disponibles dans les quantités suivantes : 1, 2, 4, 8, 16 ou 32. |
 |Adresses IPv6 principales |Affectées aux interfaces internes et externes de votre serveur. |
 |Adresses IPv6 statiques publiques |Affecte d'autres adresses IPv6 à partir d'un bloc /64. |
 |Modules complémentaires de système d'exploitation|Sélectionnez des options telles que VMware, solutions de sauvegarde, panneau de commande, base de données, pare-feux matériels et logiciels, protection antivirus et contre les logiciel espion, détection et protection contre les intrusions. <br><br>Il est fortement recommandé que votre service de sécurité d'entreprise se rapproche du support {{site.data.keyword.cloud_notm}} afin de discuter des caractéristiques de ces options.
 |Evault |Outil de sauvegarde basé sur un agent pouvant être installé sur votre serveur afin de répliquer des sauvegardes entre les serveurs. |
 |Modules complémentaires de service|Sélectionnez des modules complémentaires de service comme la surveillance, l'automatisation ou l'assurance.|
 {: caption="Tableau 1. Options de serveur supplémentaires" caption-side="top"}

## Configuration système avancée
{: #adv-system-config}

Les zones sous **Configuration système avancée** complètent le processus de mise à disposition.

| **Zone** | **Description** |
|---|---|
| Nom d'hôte | Nom permanent ou temporaire affecté à votre serveur, par exemple, _server1_. **Remarque** : Si vous mettez à disposition un serveur certifié SAP, votre nom d'hôte SAP doit être composé au maximum de 13 caractères alphanumériques. Pour plus d'informations sur les noms d'hôte SAP, voir les Notes SAP [611361](https://launchpad.support.sap.com/#/notes/2611361) et [129997](https://launchpad.support.sap.com/#/notes/129997). Requiert un ID utilisateur SAP S. |
| Domaine |Nom de sous-domaine qui ne doit pas entrer en conflit avec un nom de domaine Internet, par exemple, _test.acme.com_. |
| Sélection VLAN |S'il existe un réseau local virtuel sous votre compte car vous avez déjà commandé au moins un serveur, vous pouvez ajouter le nouveau serveur à ce réseau local virtuel. |
| Script de mise à disposition |Vous pouvez fournir un script afin d'automatiser certaines étapes après la mise à disposition. |
| Clés SSH |Vous pouvez fournir la clé publique de votre clé SSH, ce qui vous permettra de vous connecter à votre serveur une fois celui-ci mis à disposition. |
{: caption="Tableau 2. Configuration système avancée" caption-side="top"}

 Consultez le support {{site.data.keyword.cloud_notm}} pour plus d'informations.

 **REMARQUE :** Vous pouvez commander des sous-réseaux secondaires avec vos unités de calcul. Toutefois, si vous commandez des sous-réseaux secondaires, ceux-ci sont récupérés en même temps que l'unité. Si vous commandez un sous-réseau secondaire de manière indépendante (et non comme une option de module complémentaire), vous pouvez conserver le sous-réseau tant que vous ne l'annulez pas explicitement. Cette distinction est importante, car elle vous évite de perdre des adresses IP en rendant une unité de calcul.

## Etapes suivantes
Une fois votre serveur {{site.data.keyword.baremetal_short}} mis à disposition, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs {{site.data.keyword.baremetal_short}}](../bare-metal/managing.html).
