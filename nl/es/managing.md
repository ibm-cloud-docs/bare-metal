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

# Gestión de servidores nativos
{: #bm-manage-servers}

Puede cancelar, detener y reiniciar servidores.
{:shortdesc}

## Antes de empezar
{: #before-you-begin}

* Navegue hasta el menú del dispositivo de la consola. Para obtener más información, consulte [Navegación a dispositivos](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Asegúrese de tener los permisos de cuenta y el acceso al dispositivo necesarios. Solo el propietario de la cuenta, o un usuario con el permiso de la infraestructura clásica **Gestionar usuarios**, puede ajustar los permisos.

Para obtener más información sobre permisos, consulte [Permisos de la infraestructura clásica](/docs/iam?topic=iam-infrapermission#infrapermission) y [Gestión del acceso a dispositivos](/docs/bare-metal?topic=virtual-servers-managing-device-access).


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

## Supresión de la instancia de servidor
{: #bm-delete-server-instance}

Si ya no necesita la instancia de servidor nativo y no desea pagar por ella, puede suprimirla en cualquier momento.
{:shortdesc}

1. Vaya al menú **Dispositivos** y resalte el dispositivo que desea suprimir.
2. Pulse **Acciones** y seleccione **Cancelar servidor**.

## Apagar un servidor
{: #bm-power-off}

Puede crear un servidor de antemano para prepararse. Tras crear el servidor, apáguelo para asegurarse de que no se modifique nada y de que nadie pueda acceder a él. Cuando esté listo, puede encender el servidor y tenerlo en marcha en minutos.
{:shortdesc}

1. Vaya al menú **Dispositivos** y resalte el dispositivo que desea apagar o encender.
2. Pulse **Acciones** y seleccione **Encender/Apagar**.

Se le factura por el servidor mientras está apagado. Si el servidor está apagado, permanece apagado y tiene que encenderlo manualmente.
{: note}
