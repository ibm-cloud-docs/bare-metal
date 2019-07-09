---
copyright:
  years: 2014, 2018
lastupdated: "2019-04-22"

subcollection: bare-metal

keywords: Avago SafeStore, encryption
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Activation de la sécurité d'unité à l'aide de Avago SafeStore Encryption Services
{: #enabling-drive-security-by-using-avago-safestore-encryption-services}

La configuration de la sécurité d'unité permet d'empêcher l'accès aux données stockées sur des disques retirés sans une clé de sécurité. Les données d'unité ne peuvent pas être récupérées dans cette clé. {{site.data.keyword.BluSoftlayer_full}} fournit des unités SED (à chiffrement automatique) dans certains centres de données pour les unités qui peuvent être achetées sur un serveur bare metal. Des unités SATA 10 To sont disponibles dans nos centres de données aux Etats-Unis.

## Prérequis
{: #prerequisites-enabling-drive-security-by-using-avago-safestore-encryption-services}

* Serveur bare metal avec unités SED – 10 To SATA
* LSI/AVAGO MegaRAID SAS 9361 -8i ou cartes RAID LSI/AVAGO similaires
* Logiciel Mega RAID Storage Manager installé

## Activation de la sécurité d'unité à l'aide de MegaRAID Storage Manager (MSM)
{: #enabling-drive-security-by-using-megaraid-storage-manager-msm-}

Vous pouvez définir la clé de sécurité et les données de protection dans un disque supprimé à l'aide de MegaRAID Storage Manager. Vous pouvez également utiliser l'interface WebBIOS qui nécessite une clé de sécurité au démarrage du serveur pour entrer dans le BIOS de la carte MegaRAID et configurer les paramètres de sécurité de l'unité. Pour plus d'informations sur MegaRAID Controller Card SAS 9361-8i, voir le site Broadcom, [MegaRAID SAS 9361-8i ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#documentation).

### Identification des unités SED préinstallées
{: #identifying-preinstalled-sed-drives}

MegaRAID Storage Manager est préinstallé sur la plupart des systèmes d'exploitation pris en charge. S'il n'est pas présent, vous pouvez l'installer manuellement à partir du site Broadcom. Pour plus d'informations, voir le site de [téléchargements de MegaRAID SAS 9361-8i](https://www.broadcom.com/products/storage/raid-controllers/megaraid-sas-9361-8i#downloads).

Vous pouvez ouvrir MegaRAID Storage Manager à l'aide des données d'identification du système. Dans l'exemple, un environnement Windows est utilisé et MSM est préinstallé.

Lorsque vous démarrez MSM, vous devez entrer le **nom d'utilisateur** et le **mot de passe** de l'utilisateur privilégié (administrateur).

Cliquez sur l'onglet **Physical** et cliquez sur les unités qui sont disponibles sur le système. Le panneau **Properties** contient la section **Drive Security Properties** qui inclut la zone **Full Disk Encryption capable**, qui indique **Yes**. Dans l'exemple utilisé, deux disques non SED et quatre disques SED sont utilisés.

### Activation de la sécurité des unités sur le contrôleur
{: #enabling-drive-security-at-the-controller}

1. Pour activer la sécurité d'unité, cliquez avec le bouton droit de la souris sur **Controller 0 :AVAGO MegaRAID SAS 9361-8i** dans l'onglet **Physical** et sélectionnez **Enable Drive Security**.
  * Vous pouvez à présenter renseignez les zones **Security key identifier** et **Security key**. Si vous avez plusieurs clés de sécurité, un identificateur de clé de sécurité peut vous aider à identifier quelle clé de sécurité vous devez utiliser. Vous devez enregistrer la clé de sécurité dans un endroit sûr. La clé de sécurité est obligatoire lorsque vous reconfigurez les unités, par exemple, lors du retrait ou de la réinsertion d'une unité. Sans la clé de sécurité, il n'est pas possible d'extraire des données stockées dans un volume créé en dehors des unités SED. Il n'est pas possible de récupérer une clé de sécurité publiée. Un mot de passe au démarrage peut également être défini ; le système est mis en pause et attend que le mot de passe défini soit saisi. Cette action est facultative. Si le mot de passe au démarrage est défini, vous devez vous connecter à IPMI et le taper à chaque fois que le système est réamorcé. Faites défiler l'écran, cochez la case **I recorded the security settings for future reference** et cliquez sur **Yes** pour activer la sécurité d'unité.
  * Lorsque la sécurité d'unité est activée, une image représentant une clé jaune apparaît pour **Controller 0 AVAGO MegaRAID SAS 9361-8i**.
2. Créez à présent un volume sécurisé en utilisant les unités SED. Avec le bouton droit de la souris, cliquez sur **Controller0** dans l'onglet **Logical** et sélectionnez   
**Create Virtual Drive**.
3. Choisissez l'option **Advanced**. L'écran doit spécifier le **niveau RAID** et la **méthode de sécurité d'unité** pour
**Full Disk encryption (FDE)**. Sélectionnez les unités FDE qui sont requises et cliquez sur **Add** > **Create Drive Group** > **Next**.
4. Passez en revue les paramètres d'unité virtuelle et apportez les corrections nécessaires. La valeur suggérée pour **Read Policy** est **Always Read Ahead**. La valeur suggérée pour **Write policy** est **Write Back**. Cliquez sur **Create Virtual Drive**. Acceptez l'impact  de la politique de réécriture en raison de BBU en cliquant sur **Yes**. Cliquez sur **Next** et passez en revue l'écran récapitulatif. Cliquez sur **Finish**.
5. Pour confirmer que le disque virtuel est sécurisé, cliquez sur l'onglet **Logical** et sur l'unité virtuelle qui a été créée. Dans la section **Drive Security Properties**, la zone **Secured** a pour valeur **Yes**.

Si le serveur a été livré avec des volumes RAID qui sont déjà créés à l'aide d'unités SED, vous pouvez sécuriser ces volumes en procédant comme suit :

Dans l'onglet **Logical**, cliquer avec le bouton droit de la souris sur **Drive Group** et sélectionnez **Secure Using FDE**. Si vous avez mélangé des unités FDE et non FDE pour un volume, cette option ne s'affiche pas.

Pour retirer la sécurité d'unité, vous devez d'abord supprimer les disques virtuels sécurisés et cliquer avec le bouton droit de la souris sur Controller 0 et sélectionner l'option **Disable Drive Security**. Cette fonction efface les données de façon sécurisée et retire la sécurité d'unité.

Vous pouvez également configurer la sécurité d'unité à l'aide de webBIOS en vous connectant via l'IPMI au moment du démarrage et en entrant le BIOS RAID. <!--For more information, see **Avago SafeStore Encryption Services** in the **12 Gb/s MegaRAID SAS Software User Guide**.-->
