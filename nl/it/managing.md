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

# Gestione dei server bare metal
{: #bm-manage-servers}

Puoi annullare, arrestare e riavviare i server.
{:shortdesc}

## Prima di iniziare
{: #before-you-begin}

* Passa al menu del dispositivo della tua console. Per ulteriori informazioni, vedi [Passaggio ai dispositivi](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Assicurati di disporre di tutte le autorizzazioni di account necessarie e dell'accesso al dispositivo. Solo il proprietario dell'account o un utente con l'autorizzazione di **Gestione utenti** dell'infrastruttura classica può modificare le autorizzazioni.

Per ulteriori informazioni sulle autorizzazioni, vedi [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gestione dell'accesso al dispositivo](/docs/bare-metal?topic=virtual-servers-managing-device-access).


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

## Eliminazione dell'istanza del server
{: #bm-delete-server-instance}

Puoi eliminare l'istanza del server bare metal in qualsiasi momento se non ti serve più e non vuoi ricevere alcun addebitato.
{:shortdesc}

1. Vai al menu **Dispositivi** ed evidenzia il dispositivo da eliminare.
2. Fai clic su **Azioni** e seleziona **Annulla server**.

## Spegnimento di un server
{: #bm-power-off}

Puoi creare un server in anticipo per prepararti all'utilizzo. Dopo aver creato il server, spegnilo per assicurarti che non venga modificato nulla e che nessuno possa accedervi. Quando sei pronto, puoi accendere il server e averlo a tua disposizione in pochi minuti.
{:shortdesc}

1. Vai al menu **Dispositivi** ed evidenzia il dispositivo da spegnere o accendere.
2. Fai clic su **Azioni** e seleziona **Accensione/Spegnimento**.

Ti viene addebitato il costo del server anche mentre è spento. Se il server è spento, rimane spento e devi accenderlo manualmente.
{: note}
