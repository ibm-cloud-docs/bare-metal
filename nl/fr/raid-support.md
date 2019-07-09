---

copyright:
  years: 1994, 2019
lastupdated: "2018-5-31"

keywords: raid support, raid help

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Informations sur les tickets de demande de service relatifs à RAID 
{:# bm-raid-support-ticket}

Si vous avez un problème ou une question concernant l'utilisation du RAID sur votre serveur bare metal, vous trouverez peut-être une réponse dans le forum [IBM developerWorks dW Answers](https://developer.ibm.com/answers/topics/ibm-cloud/){:new_window}.
Vous pouvez également ouvrir un ticket de demande de service. Pour plus d'informations sur les tickets de demande de service, voir [Ouvrir un ticket de support.](https://test.cloud.ibm.com/docs/get-support?topic=get-support-getting-customer-support#open-ticket){:new_window}
{:shortdesc}

<!--During a drive or RAID failure, support tickets are automatically created. You can create a support ticket for other problems.--> Lorsqu'un ticket de demande de service est créé, vous devez fournir des fichiers journaux RAID. Les informations contenues dans les fichiers journaux RAID sont essentielles à la récupération d'une configuration RAID perdue. Fournir vos fichiers journaux aide l'équipe de support à identifier l'ordre des unités, l'appartenance à la grappe, la géométrie de la grappe et les problèmes de câblage. En fonction du type de contrôleur RAID que vous utilisez (Adaptec ou LSI), utilisez les commandes suivantes pour obtenir les fichiers journaux RAID.

**Remarque :** Si vous autorisez le redémarrage/la mise hors tension lors de la mise à jour initiale ou si vous demandez l'échange à chaud du disque, vous accélérerez le processus du ticket de demande de service.

<b>Cartes RAID Adaptec</b><br>
Utilisez la commande suivante pour obtenir les fichiers journaux des cartes RAID Adaptec. Assurez-vous d'inclure la sortie complète de ce fichier journal dans votre ticket de demande de service.

`arcconf getconfig 1/arcconf getlogs 1 device tabular`.

<b>Cartes RAID LSI</b><br>
Utilisez les commandes suivantes pour obtenir les fichiers journaux des cartes RAID LSI. Vous devez inclure la sortie complète de ces fichiers journaux dans votre ticket de demande de service.
```/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
**Important :** N'oubliez pas de sauvegarder votre travail avant de commencer une procédure de traitement des incidents.
