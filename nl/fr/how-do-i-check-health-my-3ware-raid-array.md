---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Vérification de la santé de votre grappe RAID 3ware

3ware permet d'utiliser une interface de navigateur. Toutefois, à moins d'accéder à l'interface en local, celle solution peut présenter un risque de sécurité. C'est pourquoi vous utilisez l'interface de ligne de commande.

<!--You can download the 3ware CLI utilities the software Library, located in the bottom of Customer Portal.  Please check http://downloads.service.softlayer.com for the latest version (VPN access required to access the downloads page). -->

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
Le numéro d'unité varie en fonction du nombre de grappes. 0 dans la plupart des cas.<br/>
p = port<br/>
Port indique le numéro de port. Compris entre 0 et 4 dans la plupart des cas.
