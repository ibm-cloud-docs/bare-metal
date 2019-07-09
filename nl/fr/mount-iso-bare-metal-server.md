---

copyright:
  years: 2017, 2019
lastupdated: "2018-06-03"

keywords: mount iso bare metal

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Montage d'une image ISO sur un serveur bare metal
{: #bm-mount-iso}

## Présentation

Bien que la plupart des clients {{site.data.keyword.cloud}} utilise l'un des systèmes d'exploitation standard livrés avec nos serveurs, vous pouvez monter des images ISO (images de disque) sur des serveurs. Vous disposez de trois options pour monter des images ISO personnalisées.

Pour que les méthodes fonctionnent, vous devez vous connecter au réseau privé via la service VPN SL, par exemple [SoftLayer SSL VPN Portal - AMS01](https://vpn.ams01.softlayer.com/prx/000/http/localhost/login) ou via un autre serveur déjà connecté au réseau.

**Remarque :** Les images de disque matériel Lenovo d'une taille supérieure à 50 Mo doivent être montées à l'aide de l'interface de la console IMM, l'onglet de support (média).

## Option 1 (préférée) : Utilisation d'IPMI (image ISO sur un partage CIFS)
{: #bm-mount-iso-opt-1}

Si une infrastructure est déjà déployée sur {{site.data.keyword.cloud_notm}}, vous pouvez configurer un serveur existant pour qu'il offre un partage CIFS avec le réseau interne. Vous pouvez ensuite monter n'importe quelle image ISO sur un serveur bare metal.

Il s'agit de la méthode préférée pour installer un système d'exploitation personnalisé sur un serveur bare metal car l'installation s'effectue via le réseau local, qui est très rapide et sur lequel une image ISO reste montée même si vous vous déconnectez ou si vous êtes déconnecté de l'interface de gestion.

Pour installer un système d'exploitation personnalisé à partir d'un partage CIFS, procédez comme suit :

1. Vérifiez que l'image ISO se trouve sur le partage CIFS.
* Connectez-vous à la console de gestion IPMI en faisant pointer votre navigateur Web sur l'adresse IP spécifiée dans cloud.ibm.com et sous devices -> your server (device details) -> Remote Mgmt. Le nom d'utilisateur et le mot de passe sont également spécifiés ici.
* Survolez l'onglet **Virtual Media** et cliquez sur **CD-ROM image**
* Indiquez les détails appropriés, puis cliquez sur **Save and Mount**.
* Les utilisateurs ne sont pas tous autorisés à modifier le système BIOS du serveur. Si nécessaire, vous pouvez soumettre un ticket à l'équipe de support pour demander :
  * Les privilèges d'administrateur d'utilisateur root sur l'interface IPMI (pour modifier le mode de connexion de support virtuel).
  * Le remplacement de la séquence d'amorçage par 'IPMI Virtual Disk' comme première option d'amorçage.
* Une fois ces modifications effectuées, revenez dans la console de gestion IPMI et accédez à Configuration -> Remote session et remplacez le mode de connexion par **attach**. Dans certaines consoles IMPI plus anciennes, vous pouvez ignorer cette option.
* Redémarrez le serveur et effectuez un démarrage à partir du support virtuel.


## Option 2 : Utilisation d'IPMIView (image ISO sur un partage CIFS)
{: #bm-mount-iso-opt-2}

Conditions préalables :<br/>
* Vous devez disposer d'une image SO amorçable.
* Vous devez disposer d'un serveur CIFS Windows ou d'un stockage en réseau NAS pour stocker l'image ISO amorçable.
* L'image ISO doit avoir été téléchargée dans le stockage de fichiers (stockage en réseau NAS) associé au serveur.
* IPMIView doit avoir été installé ou avoir accès à la console KVM.
* Un fichier ISO doit pouvoir être téléchargé via wget.
* Vous devez disposer d'un accès SSH avec des privilèges pour accéder/installer des packages et créer un montage.


### Linux et Windows
Pour monter une image ISO avec IPMIView, procédez comme suit :
1. Soumettez un ticket à l'équipe de support et spécifiez que votre serveur doit initialiser son unité de CD-ROM virtuelle comme première unité. Chaque unité doit être initialisée à partir de l'unité de CD-ROM virtuelle qui lui est associée. Vous pourrez annuler ce paramètre une fois le système d'exploitation installé.
* Etablissez une connexion VPN à [VPN](http://www.softlayer.com/VPN-Access). Si vous utilisez Microsoft Internet Explorer, prenez soin d'inclure .softlayer.com et .cloud.ibm.com dans votre liste des sites de confiance et de maintenir JAVA à jour.
* Copiez le support ISO sur le stockage en réseau NAS ou le serveur CIFS Windows.
  * Connectez-vous à votre jumpbox Linux à l'aide de SSH.
  * Montez le partage NAS sur votre jumpbox Linux :

        mkdir /mnt/nasmount
        mount -t cifs //NAS_SERVER_NAME_ORIP/SLN#####-2 -o username=SLN#####-2,
        password=NAS_STORAGE_PW,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755 /mnt/nasmount
  * Clé de paramètre de la commande mount :
        NAS_SERVER_NAME_ORIP = Nom ou adresse IP du stockage en réseau NAS.
        /SLN#####-2 = Nom d'utilisateur et nom de dossier à utiliser pour la connexion à votre stockage en réseau NAS.
        NAS_STORAGE_PW = Mot de passe de votre stockage en réseau NAS.
        /mnt/nasmount = Dossier dans lequel monter le stockage en réseau NAS.
  * Passez dans le dossier où le nouveau stockage en réseau NAS a été monté.
        cd /mnt/nasmount
  * Téléchargez le fichier ISO à l'aide de wget.
        wget http://www.linktoyouriso.com/isofilename.iso
  Un message de confirmation s'affichera pour indiquer que le téléchargement a abouti.
* Téléchargez IPMI View ici :
      https://www.servethehome.com/download-supermicro-ipmiview-latest-version/
* Connectez-vous au serveur via l'adresse IP de gestion.<br>
      1. Connectez-vous à `winadmin`.
      2. Ouvrez IPMIView et accédez à **File > New > System**.
      3. Utilisez l'adresse IP d'IPMI figurant dans l'objet matériel pour renseigner les zones Server Name et IP address.<br>
      4. Double-cliquez sur le système indiquant la même adresse IP sur le côté gauche et entrez ADMIN sous Login ID et le mot de passe IPMI figurant dans l'objet matériel.
      5. Après vous être reconnecté, un grand nombre d'onglets peut apparaître dans la fenêtre. Vous pouvez utiliser **Text Console** ou **KVM Console** pour vous connecter au serveur.

* Ouvrez l'onglet Virtual Media.
* Entrez les détails de la connexion de l'image de CD-ROM.
  *
    * Hôte de partage = Adresse IP du stockage en réseau NAS. Pour obtenir cette valeur, vous pouvez exécuter une commande PING portant sur le nom du stockage en réseau NAS. Par exemple, `ping nas501.service.softlayer.com`
    * Nom de partage = Nom d'utilisateur du stockage en réseau NAS.
    * Chemin d'accès à l'image = Nom du fichier ISO, au format suivant :
          \NASusername\isoname.iso (i.e. \SLN123456\centos6.iso)
    * Utilisateur = Nom d'utilisateur du stockage en réseau NAS
    * Mot de passe = Mot de passe du stockage en réseau NAS
* Redémarrez le serveur
* Ouvrez la vue de la console KVM
* Suivez les invites système pour initialer l'image ISO amorçable
* Installez le système d'exploitation
* Démontez le support virtuel
* Redémarrez le serveur

## Option 3 : Montage d'une image ISO à partir de votre ordinateur local
{: #bm-mount-iso-opt-3}

<a name="option3"></a>

Vous pouvez monter une image ISO à partir de votre ordinateur local en utilisant l'afficheur iKVM Java (console). Cela vous permettra de monter une image ISO tout en étant connecté à la console. La progression de l'installation peut varier en fonction de la vitesse de téléchargement et du temps d'attente de votre connexion à Internet, et des performances de Java et de votre ordinateur.

Si vous n'êtes pas autorisé à modifier le système BIOS sur un serveur, soumettez un ticket à l'équipe de support afin de demander les modifications suivantes :
* Les privilèges d'administrateur d'utilisateur Root sur l'interface IPMI (pour modifier le mode de connexion de support virtuel).
* Le remplacement de la séquence d'amorçage par 'IPMI Virtual Disk' comme première option d'amorçage. (L'image ISO n'étant pas encore montée, l'équipe de support ne devrait modifier que la priorité d'unité d'amorçage pour l'instant.)


1. Connectez-vous à la console de gestion d'IPMI en faisant pointer votre navigateur Web vers l'adresse IP spécifiée dans cloud.ibm.com.
* Cliquez sur Devices > your server (device details) > Remote Mgmt. Indiquez le nom d'utilisateur et le mot de passe.
* Cliquez sur Configuration > Remote session et remplacez le mode de connexion par **attach**. Dans certaines consoles IMPI plus anciennes, cette option n'est pas disponible, par conséquent, vous pouvez ignorer cette étape.
* Cliquez sur System > System information pour revenir sur la page des informations système. Une icône de fenêtre console s'affiche.
* Cliquez sur cette icône pour ouvrir la console. Acceptez tous les avertissements de sécurité.
* Lorsque la console est connectée, une invite d'ouverture de session apparaît.
* Cliquez sur Virtual Media > Virtual Storage.
* Accédez à l'onglet **CDROM&ISO** et sélectionnez le fichier ISO sous **Logical Drive Type**.
* Cliquez sur **Open Image** et sélectionnez l'image ISO sur votre ordinateur local.
* Cliquez sur **Plug in** pour insérer l'image ISO dans l'unité virtuelle de CD-ROM.
* Cliquez sur **OK**.
* Redémarrez le serveur et utilisez l'option **Boot from the virtual cd-rom drive**. Vous devrez peut-être utiliser le clavier virtuel dans l'afficheur iKVM pour sélectionnez une unité d'amorçage.

## Identification et résolution des problèmes
{: #bm-mount-iso-troubleshooting}

* Par défaut, les utilisateurs ne disposent pas tous des droits d'accès au support virtuel de montage. Si une erreur liée aux droits d'utilisateur se produit, contactez le support pour demander une mise à jour des droits d'utilisateur IPMI root.
* Si une image ISO est déjà montée, un message d'erreur s'affiche avec le texte **There is a disk mounted**. Vous devez démonter le disque et le remplacer par la nouvelle image ISO. Il n'est pas possible de monter deux images ISO en même temps.
* Vous devrez peut-être contacter le support pour modifier l'ordre d'amorçage dans le système BIOS.
* Lorsque vous montez une image ISO, utilisez le [VPN SSL](http://vpn.softlayer.com) au lieu du VPN PPTP.  Une fois que vous êtes connecté au réseau VPN, vous pouvez également accéder à l'interface IPMI du système à l'adresse IPMI (https://private-ip-IPMI-management).
* Lorsque vous entrez un chemin d'accès à une image ISO, utilisez la syntaxe de nom UNC (Universal Naming Convention) pour le chemin, par exemple :
  `\\<NAS username>\<isoname>.iso`
