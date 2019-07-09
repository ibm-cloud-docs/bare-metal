---

copyright:
  years: 2016, 2019
lastupdated: "2019-06-17"

keywords: manage bare metal servers, power off, replicate, reload os, delete server, manage server

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note .note}

# Gestion des serveurs bare metal
{: #bm-manage-servers}

Vous pouvez annuler, arrêter et redémarrer des serveurs.
{:shortdesc}

## Avant de commencer
{: #before-you-begin}

* Accédez au menu de votre console. Pour plus d'informations, voir [Accès aux unités](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Vérifiez que vous disposez des autorisations de compte nécessaires et que vous avez accès à l'unité. Seul le propriétaire du compte, ou un utilisateur avec l'autorisation **Gérer les utilisateurs** de l'infrastructure classique, peut régler les autorisations.

Pour plus d'informations sur les autorisations, voir [Droits d'infrastructure classique](/docs/iam?topic=iam-infrapermission#infrapermission) et [Gestion de l'accès aux terminaux](/docs/bare-metal?topic=virtual-servers-managing-device-access).


<!-- ## Replicating a server instance
{: #bm-replicate-server-instance}

You can copy or clone a bare metal server instance to replicate the server configuration and quickly get a new server up and running.
{:shortdesc}

To clone the instance:
 1. Go to the **Device** menu and highlight the device to be copied.
 2. Click **Actions** and select **Configure Replica**. All configurations are copied. No data or content is not copied.
 3. Enter a unique server name.
 4. Specify the domain name. -->

<!-- ## Reloading the operating system
{: #bm-reload-os}

Occasionally, you might want to reload the operating system on your server.
{:shortdesc}

To reload the operating system, follow these steps.
 1. Back up all data before you start. If you don't back up your data, all data that is on the primary disk is lost. But, secondary disk data stays intact.
 2. Go to the **Devices** menu and highlight the device to be reloaded.
 3. Click **Actions** and select **OS Reload**. You can select one of these options:
  * Change the operating system to a different one and start over with new configurations.
  * Keep the existing operating system with the current configurations, but wipe out the server to start over.

During the OS reload, the server is offline and unavailable for use. Reload time varies based on server capacity and operating system. If you defined a provision script, all configurations are restored after the reload completes. Data was backed up before the OS reload can be uploaded the server when the server is available. -->

## Suppression d'une instance de serveur
{: #bm-delete-server-instance}

Vous pouvez à tout moment supprimer l'instance de serveur bare metal si vous n'en avez plus besoin et ne souhaitez pas être facturé pour cette instance.
{:shortdesc}

1. Accédez au menu **Périphériques** et mettez en évidence l'unité que vous souhaitez supprimer.
2. Cliquez sur **Actions** et sélectionnez **Annuler un serveur**.

## Mise hors tension d'un serveur
{: #bm-power-off}

Vous pouvez créer un serveur à l'avance pour vous préparer à l'utiliser. Une fois le serveur créé, mettez-le hors tension afin que rien ne soit modifié sur ce serveur et que personne ne puisse y accéder. Lorsque vous êtes prêt, vous pouvez mettre le serveur sous tension et le faire démarrer en quelques minutes. {:shortdesc}

1. Accédez au menu **Périphériques** et mettez en évidence l'unité que vous souhaitez mettre sous ou hors tension.
2. Cliquez sur **Actions** et sélectionnez **ON/OFF**.

Le serveur vous est facturé lorsqu'il est éteint. Si le serveur est mis hors tension, il reste éteint et vous devez le mettre sous tension manuellement.
{: note}
