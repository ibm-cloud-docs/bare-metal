---
copyright:
  years: 1994, 2018
lastupdated: "2018-5-10"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Commandes de contrôleur RAID

Vous utilisez l'utilitaire de ligne de commande Adapatec pour exécuter des commandes de contrôleur RAID.
Vous trouverez ci-après les commandes de contrôleur RAID les plus courantes que vous pouvez utiliser.
{:shortdesc}

**Remarque :** Windows et VMware possèdent des chemins différents pour exécuter des commandes storcli. Voir les exemples ci-après pour le chemin de commande approprié.

Windows (utiliser CMD)
`C:\Program Files (x86)\MegaRAID Storage Manager>`      
ou
`C:\Program Files\LSIStorCli>`

VMware (vous devez installer storcli avant d'exécuter des commandes storcli)
`/opt/lsi/storcli/`

## Commandes communes de contrôleur RAID

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_ répertorie le type d'opération, le numéro d'unité, la taille
d'unité logique et la progression de l'opération. Vous pouvez également voir le statut des commandes qui s'exécutent en arrière-plan, comme par exemple dans les éléments suivants :
<ul>
  <li> Régénération la plus récente
  <li> Synchronisation
  <li> Migration d'unité logique
  <li> Compression/Extension
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1</b></code> <br>
_GETCONFIG_ répertorie les informations sur les contrôleurs, unités logiques et unités physiques. Vous pouvez voir des informations telles que les éléments suivants :
<ul>
  <li> Type de contrôleur
  <li> BIOS, bloc d'amorçage, pilote de périphérique et versions de microprogramme
  <li> Type d'unité physique, ID unité, présence de PFA
  <li> Etat d'unité physique
  <li> Informations de boîtier : ventilateur, alimentation électrique et température
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular</code></b>
_GETLOGS_ vous donne accès au statut et aux journaux des événements d'un contrôleur. _DEVICE xxx_ affiche un journal des erreurs d'unité rencontrées par le contrôleur. 

Voici un exemple de sortie obtenue via la commande _GETLOGS_ :
```
driveErrorEntry
smartError.. ............................ false 
vendorID ................................ WDC
serialNumber ............................ WD-XXX
wwn ..................................... xxxxxxxxxxxxxxxx - CC_FILTER
deviceID ................................ 10
productID ............................... WD1003FB
numParityErrors ......................... 0
linkFailures ............................ 0
hwErrors ................................ 0
abortedCmds ............................. 7
mediumErrors ............................ 20
smartWarning ............................ 0
```

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show all | grep -iE "det|cou|tem|SN|S.M|fir” </code></b><br>
Vous utilisez cette commande pour afficher les unités spécifiques ainsi que toute erreur d'unité possible qu'elles pourraient comporter.
Voici un exemple de la sortie :
```
Drive /c0/e252/s0 - Detailed Information: 
Shield Counter = 0
 Media Error Count = 0
 Other Error Count = 0 
Drive Temperature = 24C (75.20 F) 
Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No 
SN = XXXX 
Firmware Revision = SN04

 Drive /c0/e252/s1 - Detailed Information: 
Shield Counter = 0 
Media Error Count = 0 
Other Error Count = 0 
Drive Temperature = 22C (71.60 F) 
Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No 
SN = xxxx 
Firmware Revision = SN03 

Drive /c0/e252/s2 - Detailed Information:
 Shield Counter = 0 
Media Error Count = 0 
Other Error Count = 0 
Drive Temperature = 21C (69.80 F)
 Predictive Failure Count = 0 
S.M.A.R.T alert flagged by drive = No
 SN = xxxx 
Firmware Revision = SN04

 Drive /c0/e252/s3 - Detailed Information:
 Shield Counter = 0 
Media Error Count = 0
 Other Error Count =
 Drive Temperature = 23C (73.40 F) 
Predictive Failure Count = 0
 S.M.A.R.T alert flagged by drive = No 
SN = xxxx
Firmware Revision = SN03  
```

<!--<code><b>/opt/MegaRAID/storcli/storcli64 /c0 show all | less </code></b>-->
<!--You use this command to view RAID health, size, name, and other important information.-->

<code><b>/opt/MegaRAID/storcli/storcli64 /c0/eall/sall show rebuild</code></b>
Cette commande affiche le statut de régénération de toutes les unités ainsi que la durée estimée d'exécution de la régénération. Voici la sortie qui s'affiche à l'exécution de la commande :
```
---------------------------------------------
Drive-ID Progress% Status Estimated Time Left 
---------------------------------------------
/c0/e252/s0 - Not in progress
 /c0/e252/s1 - Not in progress
 /c0/e252/s2 - Not in progress
 /c0/e252/s3 - Not in progress
--------------------------------------------- 
```

<b>RAID alert "Spam"</b>
Changer la section "global" de la configuration par défaut (/opt/lsi/mrmonitor/MegaMonitor/config-current.xml) :
```<global>
 <severity level="FATAL"> 
<do-systemlog/> 
<do-email/>
 </severity>
<severity level="CRITICAL"> 
<do-email/>
 <do-systemlog/> 
</severity>
 <severity level="WARNING">
 <do-email/> 
<do-systemlog/> 
</severity>
 <severity level="INFO"> <do-systemlog/>
</severity>
 </global> 
```
to this: 
```
<global> 
<severity level="FATAL"> 
<do-systemlog/> 
<do-email/>
 </severity> 
<severity level="CRITICAL"> 
<do-email/> 
<do-systemlog/> 
</severity> 
<severity level="WARNING"> 
<do-systemlog/> 
</severity> 
<severity level="INFO">
<do-systemlog/>
 </severity> 
</global> 
```
**Remarque :** Retirez la balise "do-email" pour le niveau "WARNING" (avertissement). Ou bien, passez le niveau de sécurité à "INFO".

## Erreurs communes liées aux unités

Les erreurs d'unité les plus courantes sont les erreurs smart, matérielles et de support. Vous constatez ces erreurs en cas de panne d'un unité. C'est pourquoi vous devez remplacer l'unité dès que possible.

Bien qu'elles ne soient pas inhabituelles, les commandes annulées ne constituent pas un autre type d'erreur courante. Néanmoins, si le nombre de commandes abandonnées augmente (et passe, par exemple, 100), ouvrez un ticket de demande de service.   

Des erreurs de liaison peuvent indiquer qu'un câble doit peut-être être vérifié ou remplacé.

## Informations de ticket de demande de service

<b>Cartes RAID Adaptec</b>
Veillez à inclure la sortie complète de la commande `arcconf getconfig 1/arcconf getlogs 1 device tabular` lorsque vous créez un ticket de demande de service. Fournir ces informations aidera l'équipe de support à identifier l'ordre d'unité, l'appartenance à la grappe, la géométrie de la grappe et les problèmes de câblage. Ces informations sont essentielles pour la récupération d'une configuration RAID perdue. Accorder des droit pour redémarrer/mettre hors tension la mise à jour initiale ou demander un remplacement à chaud permettent d'accélérer le traitement de ticket de demande de service.

<b>Cartes RAIDE LSI</b>
Utilisez les commandes suivantes pour obtenir les fichiers journaux de cartes RAID LSI. Vous devez inclure la sortie complète de ces fichiers journaux dans votre ticket de demande de service. 
```
/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```

**Remarque** : N'oubliez pas de sauvegarder votre travail avant d'effectuer une procédure de traitement des incidents.
