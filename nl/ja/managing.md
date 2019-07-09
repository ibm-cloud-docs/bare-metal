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

# ベア・メタル・サーバーの管理
{: #bm-manage-servers}

サーバーをキャンセル、停止、および再始動できます。
{:shortdesc}

## 始める前に
{: #before-you-begin}

* コンソールのデバイス・メニューに移動します。詳しくは、[デバイスへのナビゲート](/docs/bare-metal?topic=virtual-servers-navigating-devices)を参照してください。
* 必要なアカウント権限とデバイス・アクセス権限があることを確認します。アカウントの所有者、またはクラシック・インフラストラクチャーの**「ユーザーの管理」**権限を持つユーザーのみが、権限を調整できます。

権限について詳しくは、[クラシック・インフラストラクチャーの権限](/docs/iam?topic=iam-infrapermission#infrapermission)および[デバイス・アクセス権限の管理](/docs/bare-metal?topic=virtual-servers-managing-device-access)を参照してください。


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

## サーバー・インスタンスの削除
{: #bm-delete-server-instance}

ベア・メタル・サーバーのサーバー・インスタンスが不要になり、課金されないようにする場合は、いつでも、そのインスタンスを削除できます。
{:shortdesc}

1. **「デバイス」**メニューに移動し、削除するデバイスを強調表示します。
2. **「アクション」**をクリックし、**「サーバーのキャンセル」**を選択します。

## サーバーの電源オフ
{: #bm-power-off}

使用準備のためにサーバーを前もって作成します。 サーバーの作成後に、サーバーを電源オフすることで、何も変更されず、誰もアクセスできないようにすることができます。 準備ができた時点で、サーバーの電源をオンすると、数分で作動可能な状態になります。
{:shortdesc}

1. **「デバイス」**メニューに移動し、電源をオフまたはオンにするデバイスを強調表示します。
2. **「アクション」**をクリックし、**「パワーオン/オフ」**を選択します。

電源がオフになっている間も、サーバーに対する請求は行われます。サーバーの電源をオフにした場合、サーバーは電源オフ状態のままになるため、手動で電源オンする必要が生じます。
{: note}
