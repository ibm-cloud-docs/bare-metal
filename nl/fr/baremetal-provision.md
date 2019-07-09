---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: custom server, {{site.data.keyword.baremetal_short}}, {{site.data.keyword.Bluemix_notm}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}


# Génération d'un serveur bare metal personnalisé
{: #ordering-baremetal-server}

Utilisez la procédure suivante pour générer un serveur bare metal personnalisé.

## Mise à disposition via le catalogue {{site.data.keyword.cloud_notm}}
{: #provision-through-the-catalog}

Utilisez la procédure suivante pour mettre à disposition votre serveur bare metal via {{site.data.keyword.cloud_notm}}.

1. Ouvrez le [catalogue {{site.data.keyword.cloud_notm}}](https://cloud.ibm.com/catalog/){: external}.   
2. Sélectionnez Serveurs bare metal sous **Calcul**.
3. Cliquez sur Continuer. Si vous ne voyez pas le bouton Continuer, vous devrez peut-être vous connecter.
4. Entrez la **quantité** de serveurs **identiques** à mettre à disposition. La valeur par défaut est 1. Si vous souhaitez mettre à disposition plusieurs serveurs avec des spécifications _différentes_, vous devez les mettre à disposition séparément.
5. Le **nom d'hôte** est un nom permanent ou temporaire affecté à vos serveurs, par exemple, baremetal01. Cliquez sur **Information** pour obtenir des informations sur le formatage.
6. Le **domaine** est la chaîne d'identification qui définit le contrôle administratif dans Internet, par exemple, Customer-123456.cloud. Cliquez sur **Information** pour obtenir des informations sur le formatage.
7. La **facturation** peut être calculée sur une base **horaire** ou **mensuelle**.
8. Sélectionnez l'**emplacement**, la région et le centre de données où votre serveur doit être situé.
9. Cliquez sur **Tous les serveurs** pour afficher une liste des processeurs (simples, doubles et quadruples) et des serveurs certifiés (SAP et VMware). Sélectionnez le serveur qui correspond le mieux à votre flux de travail.
10. Sélectionnez votre mémoire **RAM**. Pour certains serveurs, la mémoire RAM est définie par défaut en fonction du modèle de l'unité centrale, et ne peut pas être modifiée. 

Pour les serveurs certifiés SAP, la mémoire RAM et le système d'exploitation sont définis par défaut en fonction de votre sélection de serveur. Votre option de stockage locale est également définie par défaut en fonction de votre sélection de serveur.
{ :Remarque}

11. Entrez une clé publique facultative pour votre **clé SSH**, que vous pouvez utiliser pour vous connecter à votre serveur après sa mise à disposition.
12. Sélectionnez une **image** (système d'exploitation) pour votre serveur. Vos options sont basées sur le serveur que vous avez sélectionné.
13. Développez **Modules complémentaires** pour sélectionner les options relatives à la configuration du serveur.
14. Les **disques de stockage** sont préconfigurés en fonction du serveur que vous avez sélectionné. Développez **Modules complémentaires** pour ajouter des volumes de stockage de fichier ou de bloc après avoir mis à disposition votre serveur bare metal. 
15. Sous **Interface réseau**, sélectionnez les options Vitesses de port pour la liaison montante et VLAN privé. Développez **Modules complémentaires** pour sélectionner les options appropriées ou utilisez les valeurs par défaut.
16. Vérifiez votre commande dans le récapitulatif de la commande.
17. Entrez votre code promotionnel sous **Appliquez votre code promotionnel**, si vous en avez un.
18. Cliquez sur les accords sur les services tiers pour afficher tous les accords répertoriés.
19. Cliquez sur **Créer** pour mettre votre serveur à disposition. Vous êtes redirigé vers un écran avec votre numéro de commande de mise à disposition, que vous pouvez imprimer à titre de reçu.

Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée).

L'e-mail de _mise à disposition_ inclut un lien vers votre page *Détails de l'unité* pour que vous puissiez vous connecter à {{site.data.keyword.cloud_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.

Vous avez en outre la possibilité de sauvegarder la commande en tant que devis ou de l'ajouter à une estimation. Lorsque vous sauvegardez un devis, un lien est envoyé à l'adresse e-mail associée à votre compte. Ouvrez le lien pour voir les informations de devis sauvegardées. Une autre option possible est d'accéder à Gérer > Facturation et utilisation, et de sélectionner Ventes > Devis de périphérique. Si vous disposez de l'accès nécessaire, vous pouvez acheter l'offre du devis en cliquant sur ce dernier et en confirmant la commande. L'ajout à l'estimation place les coûts de configurations proposés dans le calculateur de prix. Cliquez sur **Information** pour en savoir plus sur le calculateur de prix.

## Mise à disposition via le portail client
Suivez la procédure suivante pour mettre à disposition votre serveur bare metal via le portail {{site.data.keyword.slportal}}.

1. Connectez-vous au portail [{{site.data.keyword.slportal}}](control.softlayer.com){: external} à l'aide de vos données d'identification uniques.
2. Accédez à **Compte** > **Passer une commande**.
3. Choisissez **Horaire** ou **Mensuel**.
3. Sélectionnez le centre de données où vous souhaitez que votre serveur bare metal soit situé dans la liste, puis sélectionnez votre serveur certifié (SAP ou VMware) ou processeur (simple, double et quadruple) en cliquant sur le **Prix de départ**.
4. Entrez la **quantité** de serveurs _identiques_ à mettre à disposition. La valeur par défaut est 1. Si vous souhaitez mettre à disposition plusieurs serveurs avec des spécifications _différentes_, vous devez les mettre à disposition séparément.
5. Sélectionnez votre mémoire **RAM**. Pour certains serveurs, la mémoire RAM est définie par défaut en fonction du modèle de l'unité centrale, et ne peut pas être modifiée. 

Pour les serveurs certifiés SAP, la mémoire RAM et le système d'exploitation sont définis par défaut en fonction de votre sélection de serveur. Votre option de stockage locale est également définie par défaut en fonction de votre sélection de serveur.
{ :Remarque}

6. Sélectionnez votre système d'exploitation.
7. Sélectionnez vos disques durs et les modèles complémentaires du système.
8. Cliquez sur **Ajouter à la commande**. Vous êtes alors redirigé pour confirmer votre commande.
9. Confirmez ou éditez les informations de domaine du serveur. Le **nom d'hôte** est un nom permanent ou temporaire affecté à vos serveurs, par exemple, baremetal01.  
10. Sélectionnez **Conditions des services Cloud** et **Accords de services tiers**.
11. Entrez un code promotionnel sous **Code promotionnel**, si vous en avez un, et cliquez sur **Appliquer**.
12. Confirmez ou entrez vos informations de paiement et cliquez sur **Soumettre commande**. Vous êtes redirigé vers un écran avec votre numéro de commande de mise à disposition, que vous pouvez imprimer à titre de reçu. 

Plusieurs messages électroniques sont envoyés à votre administrateur (accusé de réception de la commande de mise à disposition, approbation et traitement de la commande de mise à disposition et mise à disposition terminée). Le message électronique indiquant que la mise à disposition est terminée inclut un lien qui vous dirige directement vers la page *Détails de l'unité* après la connexion à {{site.data.keyword.Bluemix_notm}}. Vous pouvez également vous connecter directement au portail {{site.data.keyword.slportal}}.

## Etapes suivantes
Une fois que votre serveur bare metal a été mis à disposition, vous pouvez commencer à le gérer. Pour plus d'informations, voir [Gestion des serveurs bare metal](/docs/bare-metal?topic=bare-metal-bm-manage-servers#bm-manage-servers).
