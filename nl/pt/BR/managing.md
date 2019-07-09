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

# Gerenciando servidores bare metal
{: #bm-manage-servers}

É possível cancelar, parar e reiniciar servidores.{:shortdesc}

## Antes de Come╬ar
{: #before-you-begin}

* Navegue para o menu de dispositivos do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Assegure-se de que você tenha as permissões de conta e o acesso ao dispositivo necessários. Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões.

Para obter mais informações sobre as permissões, consulte [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/bare-metal?topic=virtual-servers-managing-device-access).


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

## Excluindo a instância do servidor
{: #bm-delete-server-instance}

A qualquer momento, é possível excluir a instância do Bare Metal Server caso você não precise mais dela e não queira ser
cobrado.
{:shortdesc}

1. Acesse o menu **Dispositivos** e destaque o dispositivo a ser excluído.
2. Clique em **Ações** e selecione **Cancelar
servidor**.

## Desligando um servidor
{: #bm-power-off}

É possível criar um servidor antecipadamente para a preparação do uso. Depois de
criar o servidor, desligue-o para certificar-se de que nada seja mudado e que ninguém
possa acessá-lo. Quando você estiver pronto, será possível ligar o servidor e tê-lo
pronto em minutos.{:shortdesc}

1. Acesse o menu **Dispositivos** e destaque o dispositivo a
ser desligado ou ligado.
2. Clique em **Ações** e selecione **Ligar/Desligar**.

Você será cobrado pelo servidor enquanto ele estiver desligado. Se o servidor for
desligado, ele permanecerá desligado e você precisará ligá-lo manualmente.
{: note}
