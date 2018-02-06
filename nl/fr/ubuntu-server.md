---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Installation d'un serveur Ubuntu sur un serveur bare metal

Si vous souhaitez utiliser un système d'exploitation qui n'est pas fourni par {{site.data.keyword.IBM&reg; Cloud}}, vous pouvez l'installer sur des serveurs bare metal en montant des images ISO personnalisées (images de disque). Pour monter une image ISO, téléchargez-la dans le stockage de fichier (stockage en réseau NAS) associé au serveur. Afin de télécharger une image ISO dans NAS, utilisez les procédures décrites ci-après pour monter une image ISO à l'aide de l'interface IPMI.
1. Commandez le serveur bare metal avec l'option **Sans système d'exploitation**.  
* Vous pouvez également sélectionner le système d'exploitation gratuit (par exemple, CentOS) comme système d'exploitation qui peut être utilisé pour la connexion au stockage en réseau NAS. 
* Commandez le stockage en réseau NAS pour stocker l'image ISO amorçable. Si vous disposez déjà d'un serveur CIFS Windows, vous pouvez l'utiliser pour partager l'image ISO. Avec ce serveur CIFS Windows, vous obtiendrez le stockage en réseau NAS existant d'une capacité de 20 Go. Après la mise à disposition du stockage en réseau NAS, vous pourrez afficher la description de celui-ci via votre portail client. 
* Téléchargez l'image ISO à partir de https://www.ubuntu.com/download/server.
* Téléchargez l'image ISO vers le stockage en réseau NAS ou le serveur CIFS Windows. Si vous possédez le stockage en réseau NAS, vous pouvez télécharger le fichier image ISO à l'aide de FTP. 

  Exemple de procédure via FTP :
  ```
  #ftp <nas address>.service.softlayer.com
  Connected to <nas address>.service.softlayer.com
  220 NAS FTP Service
  User (<nas address>.service.softlayer.com:(none)): <nas username>
  331 Please specify the password.
  Password: <nas password>
  230 Login successful.
  ftp> bin
  200 Switching to Binary mode
  ftp> put <iso imagefile name>.iso
  200 PORT command successful. Consider using PASV.
  150 Ok to send data.
  226 Transfer complete.
  ftp: 3170893824 bytes sent in 253.86 Seconds 12490.77Kbytes/sec.
  ```
  
* Etablissez une connexion VPN à {{site.data.keyword.Bluemix_notm}} avec l'interface IPMI. Vous pouvez lancer le menu VPN à partir du menu Support ou l'URL suivante :[Accès VPN](http://www.softlayer.com/VPN-Access)
* Montez l'image ISO à partir du menu IPMI Virtual Media à l'aide de l'option Connect to IPMI over the Management IP.
  1. Affichez les données d'identification IPMI.
  * Connectez-vous à IPMIView.
  * Ouvrez l'onglet Virtual Media.
  * Vous avez besoin de l'ID utilisateur root avec des privilèges d'administrateur sur l'interface IPMI. Si les privilèges affichés sont *Operator*, soumettez un ticket au support afin de remplacer ces privilèges par Administrator.
  * Spécifiez les détails de la connexion à l'image ISO
    Hôte de partage = Adresse IP du stockage en réseau NAS<br/Exemple : 10.3.x.x
    Chemin d'accès à l'image = Nom du fichier ISO file, au format suivant : \NASusername\imagefilesname.iso (par exemple \SLNxxxxxx\SLE-12-SP1-Server-DVD-x86_64-GM-DVD1.iso)
    Utilisateur = Nom d'utilisateur du stockage en réseau NAS
    Mot de passe = Mot de passe pour le stockage en réseau NAS
  * Cliquez sur le bouton **Mount**. 
  * Confirmez l'unité. 
* Cliquez et lancez l'afficheur KVM et ouvrez la page Virtual Storage à partir du menu Virtual Media. Si vous parvenez à monter votre image ISO en tant qu'unité de CD-ROM, la description de l'unité apparaîtra dans **Connection Status History**.
* Soumettez un ticket à l'équipe SoftLayer et spécifiez que votre serveur doit initialiser son unité de CD-ROM virtuelle comme première unité. Effectuez cette demande pour chaque serveur. Vous modifierez le paramétrage d'amorçage une fois le système d'exploitation installé.
  **Remarque** : vous devrez peut-être contacter le support pour modifier l'ordre d'amorçage dans le système BIOS. Cela dépendra de votre serveur. Essayez de redémarrer une fois pour confirmer l'ordre d'amorçage. 
* Redémarrez le serveur à partir de la vue KVM..
* Installez le système d'exploitation à partir de l'image ISO montée. 
* Installez le système d'exploitation Ubuntu sur le serveur bare metal à partir de l'image ISO. 
* Configurez les paramètres réseau (adresse IP/sous-réseau/passerelle/DNS, etc.). Si vous ne configurez pas correctement ces paramètres durant l'installation, vous ne pourrez vous connecter à ce serveur que par l'intermédiaire de la console KVM après le redémarrage. 

* Démontez le support virtuel. Il est recommandé de démonter le support virtuel à partir du serveur via l'onglet IPMI Virtual Media. 
* Redémarrez le serveur.
* Après le redémarrage, vous pouvez accéder au serveur via SSH. 
