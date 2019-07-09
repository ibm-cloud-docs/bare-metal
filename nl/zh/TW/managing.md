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

# 管理裸機伺服器
{: #bm-manage-servers}

您可以取消、停止及重新啟動伺服器。
{:shortdesc}

## 開始之前
{: #before-you-begin}

* 導覽至主控台的裝置功能表。如需相關資訊，請參閱[導覽至裝置](/docs/bare-metal?topic=virtual-servers-navigating-devices)。
* 確保您具有任何必要的帳戶許可權及裝置存取權。只有帳戶擁有者或具有**管理使用者**標準基礎架構許可權的使用者可以調整許可權。

如需許可權的相關資訊，請參閱[標準基礎架構許可權](/docs/iam?topic=iam-infrapermission#infrapermission)和[管理裝置存取](/docs/bare-metal?topic=virtual-servers-managing-device-access)。


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

## 刪除伺服器實例
{: #bm-delete-server-instance}

您隨時可以刪除裸機伺服器實例（如果您不再需要實例，且不想付費）。
{:shortdesc}

1. 移至**裝置**功能表，並強調顯示要刪除的裝置。
2. 按一下**動作**，然後選取**取消伺服器**。

## 關閉伺服器電源
{: #bm-power-off}

您可以事先建立伺服器來準備使用。建立伺服器之後，請關閉電源以確保未變更任何項目，且沒有人可以存取它。當您準備妥當時，即可開啟伺服器電源，讓它在幾分鐘內就緒。
{:shortdesc}

1. 前往**裝置**功能表，並強調顯示要關閉或開啟電源的裝置。
2. 按一下**動作**，然後選取**開啟/關閉電源**。

在已關閉電源的情況下，仍會針對伺服器向您收費。如果已關閉伺服器電源，則會保持為關閉電源狀態，您需要手動開啟電源。
{: note}
