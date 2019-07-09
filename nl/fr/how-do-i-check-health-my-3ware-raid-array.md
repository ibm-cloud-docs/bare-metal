---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-25"

keywords: bare metal, 3ware 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Vérification de la santé de votre grappe RAID 3ware
{: #bm-check-health-3ware-raid}

3ware permet d'utiliser une interface de navigateur. Toutefois, à moins d'accéder à l'interface en local, celle solution peut présenter un risque de sécurité. C'est pourquoi vous utilisez l'interface de ligne de commande.

Vous pouvez télécharger les utilitaires 3ware de l'interface CLI du [référentiel de plug-ins de l'interface CLI IBM Cloud](https://plugins.cloud.ibm.com/ui/repository.html#cf-plugins). Pour en savoir plus sur l'utilitaire de l'interface CLI, voir [VPN CLI Plug-in for cf CLI](https://cloud.ibm.com/docs/cli?topic=cloud-cli-vpn_cli_for_cf).

**Aide-mémoire des commandes pour les outils CLI 3ware**

Ces unités doivent être suivies d'un numéro identifiant les unités visées par la requête.

tw_cli /c0 show (la sortie affiche les informations nécessaires pour connaître la santé de la grappe RAID)

./tw_cli /c1 show

Exemple

    Unit  UnitType  Status         %Cmpl  Stripe  Size(GB)  Cache  AVerify  IgnECC

    ------------------------------------------------------------------------------

    u0    RAID-5    OK             -      64K     465.641   OFF    OFF      OFF    

    Port   Status           Unit   Size        Blocks        Serial

    ---------------------------------------------------------------

    p0     OK               u0     233.76 GB   490234752     WD-WCANY1727093

    p1     OK               u0     233.76 GB   490234752     WD-WCANY1622544

    p2     OK               u0     233.76 GB   490234752     WD-WCANY1657267

    p3     NOT-PRESENT      -      -           -             -

*Remarque :

c = contrôleur<br/>
Le contrôleur peut être 0 ou 1<br/>
u = unité<br/>
Le nombre d'unités dépend du nombre de grappes. Il est de 0 dans la plupart des cas.<br/>
p = port<br/>
Le port indique le numéro de port. Il est compris entre 0 et 4 dans la plupart des cas.
