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

# Bare-Metal-Server verwalten
{: #bm-manage-servers}

Sie können Server stornieren, stoppen und erneut starten.
{:shortdesc}

## Vorbereitungen
{: #before-you-begin}

* Navigieren Sie zum Einheitenmenü Ihrer Konsole. Weitere Informationen finden Sie unter [Zu Einheiten navigieren](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Stellen Sie sicher, dass Sie über die erforderlichen Berechtigungen für das Konto und den Gerätezugriff verfügen. Nur der Kontoeigner oder ein Benutzer mit der Berechtigung **Benutzer verwalten** für die klassische Infrastruktur kann die Berechtigungen anpassen.

Weitere Informationen zu Berechtigungen finden Sie unter [Berechtigungen für die klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission) und [Gerätezugriff verwalten](/docs/bare-metal?topic=virtual-servers-managing-device-access).


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

## Die Serverinstanz löschen
{: #bm-delete-server-instance}

Sie können die Bare-Metal-Server-Server-Instanz jederzeit löschen, wenn Sie die Instanz nicht mehr benötigen und keine Rechnung mehr erhalten möchten.
{:shortdesc}

1. Rufen Sie das Menü **Geräte** auf und heben Sie die zu löschende Einheit hervor.
2. Klicken Sie auf **Aktionen** und wählen Sie **Server stornieren** aus.

## Einen Server ausschalten
{: #bm-power-off}

Sie können einen Server im Voraus erstellen, um ihn für die Verwendung vorzubereiten. Nach der Erstellung des Servers können Sie ihn ausschalten, um sicherzustellen, dass nichts geändert wird und niemand darauf zugreifen kann. Wenn Sie bereit sind, können Sie den Server einschalten, der in wenigen Minuten betriebsbereit ist.
{:shortdesc}

1. Rufen Sie das Menü **Geräte** auf und heben Sie die Einheit hervor, die ein- oder ausgeschaltet werden soll.
2. Klicken Sie auf **Aktionen** und wählen Sie **Ein-/ausschalten** aus.

Der Server wird Ihnen in Rechnung gestellt, während er ausgeschaltet ist. Wenn der Server ausgeschaltet ist, bleibt er im ausgeschalteten Zustand und muss manuell eingeschaltet werden.
{: note}
