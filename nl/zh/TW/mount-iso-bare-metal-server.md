---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# 在裸機伺服器上裝載 ISO

## 概觀

雖然大部分 {{site.data.keyword.Bluemix_notm}} 客戶都會使用我們的伺服器所隨附的其中一個標準「作業系統」，但是您可以在伺服器上裝載自訂 ISO（磁碟映像檔）。有三個選項可讓您用來裝載自訂 ISO。

為了讓方法能夠正常運作，您需要透過 SL VPN 服務（例如：https://vpn.ams01.softlayer.com/）或透過您已連接至網路的另一部伺服器來連接至專用網路。

## 選項 1（偏好）：使用 IPMI（CIFS 共用上的 ISO）

如果您已在 {{site.data.keyword.Bluemix_notm}} 上部署基礎架構，則可以配置現有伺服器，以向內部網路提供 CIFS 共用。然後，您可以將該處的任何 ISO 裝載至裸機伺服器。

這是在裸機伺服器上安裝自訂 OS 的偏好方法，因為它會安裝在本端網路上，這十分快速，而且仍然會裝載 ISO，即使您登出或中斷與管理介面的連線。

請遵循下列步驟，以從「CIFS 共用」安裝「自訂 OS」：

1. 確定您已將 ISO 放置在「CIFS 共用」上。
* 藉由將 Web 瀏覽器指向 control.softlayer.com 中所指定的 IP，以及在「裝置」-> 您的伺服器（裝置詳細資料）->「遠端管理」下所指定的 IP，來登入 IPMI 管理主控台。這裡也會指定使用者名稱及密碼。
* 將游標移至**虛擬媒體**上方，然後按一下 **CD-ROM 映像檔**
* 填寫適當的詳細資料，然後按一下**儲存並裝載**。
* 並非所有使用者都有權變更伺服器的 BIOS。必要的話，您可以開啟問題單來支援要求：
  * IPMI 的 root 使用者管理者專用權（能夠變更「虛擬媒體連接」模式）
  * 將開機順序變更為「IPMI 虛擬磁碟」作為第一個開機選項。
* 進行這些變更之後，請回到 IPMI 管理主控台，並移至「配置」->「遠端階段作業」，然後將連接模式變更為 **attach**。在某些較舊的 IPMI 主控台中，您可以跳過此選項。
* 將伺服器重新開機，並從虛擬媒體開機。


## 選項 2：使用 IPMIView（CIFS 共用上的 ISO）

必要條件：<br/>
* 您有可開機的 ISO
* 用來儲存「可開機 ISO」的「Windows CIFS 伺服器」或「NAS 儲存空間」
* ISO 已上傳至與伺服器相關聯的「檔案儲存空間 (NAS)」。
* 已安裝 IPMIView 或存取「KVM 主控台」
* 可使用 wget 下載「ISO 檔案」
* 您的 SSH 存取權具有存取/安裝套件以及建立裝載的專用權


### Linux 及 Windows
請遵循下列步驟，以使用 IPMIView 來裝載 ISO。
1. 透過支援問題單，要求您的伺服器將其「虛擬 CD-ROM」作為第一個裝置開機。每一個裝置都必須從其關聯的虛擬 CD-ROM 開機。您可以在安裝 OS 之後回復此設定。
* 建立與 [VPN](http://www.softlayer.com/VPN-Access) 的「VPN 連線」。如果您是使用 Microsoft Internet Explorer，請務必在「信任的網站」清單中包括 .softlayer.com，並讓您的 JAVA 保持最新狀態。
* 將「ISO 媒體」複製到 NAS 或「Windows CIFS 伺服器」。
  * 使用 SSH 連接至 Linux jumpbox。
  * 在 Linux jumpbox 上裝載 NAS 共用：

        mkdir /mnt/nasmount
        mount -t cifs //NAS_SERVER_NAME_ORIP/SLN#####-2 -o username=SLN#####-2,
        password=NAS_STORAGE_PW,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755 /mnt/nasmount
  * 裝載指令參數鍵：
        NAS_SERVER_NAME_ORIP = NAS 儲存空間的名稱或 IP。
        /SLN#####-2 = 用來連接至 NAS 儲存空間的使用者名稱及資料夾名稱。
        NAS_STORAGE_PW = NAS 儲存空間的密碼。
        /mnt/nasmount = 用來裝載 NAS 儲存空間的資料夾。
  * 將目錄切換至新的 NAS 裝載資料夾。
        cd /mnt/nasmount
  * 使用 wget 來下載 iso 檔案。
        wget http://www.linktoyouriso.com/isofilename.iso
  您會看到下載成功的確認。
* 在這裡下載「IPMI 視圖」：
      http://knowledgelayer.softlayer.com/procedure/download-ipmiview
* 透過「管理 IP」連接至「伺服器」。
      http://knowledgelayer.softlayer.com/procedure/log-ipmiview
      http://knowledgelayer.softlayer.com/procedure/view-ipmi-credentials
* 開啟「虛擬媒體」標籤
* 完成「CD-ROM 映像檔」連線詳細資料。
  *
    * 共用主機 =「NAS 儲存空間」的「IP 位址」。您可以對 NAS 儲存空間伺服器名稱進行連線測試，來找到此值。例如，
    ```
    ping nas501.service.softlayer.com
    ```
    * 共用名稱 = NAS 儲存空間的「使用者名稱」
    * 映像檔的路徑 = ISO 檔案的名稱，格式如下：
          \NASusername\isoname.iso（即 \SLN123456\centos6.iso）
    * 使用者 = NAS 儲存空間的使用者名稱
    * 密碼 = NAS 儲存空間的「密碼」
* 將伺服器重新開機
* 開啟「KVM 主控台」視圖
* 遵循系統提示，以將「可開機 ISO」開機
* 安裝 OS
* 卸載「虛擬媒體」
* 重新啟動伺服器

## 選項 3：從本端電腦裝載 ISO
<a name="option3"></a>

您可以使用 Java iKVM 檢視器（主控台），從本端電腦裝載 ISO。這可讓您在連接至主控台時裝載 ISO。安裝進行的速度會隨著網際網路連線的上傳速度及延遲、Java 及電腦的效能而不同。

如果您無權變更伺服器上的 BIOS，請開啟問題單，以支援要求下列變更：
* IPMI 的 root 使用者管理者專用權（能夠變更「虛擬媒體連接」模式）
* 將開機順序變更為「IPMI 虛擬磁碟」作為第一個開機選項（因為尚未裝載 ISO，所以支援現在應該只會變更開機裝置優先順序）。


1. 藉由將 Web 瀏覽器指向 control.softlayer.com 中所指定的 IP，來登入 IPMI 管理主控台。
* 按一下「裝置」> 您的伺服器（裝置詳細資料）>「遠端管理」。指定使用者名稱及密碼。
* 按一下「配置」>「遠端階段作業」，然後將連接模式變更為 **attach**。在某些較舊的 IPMI 主控台中，無法使用此選項，因此您可以跳過此步驟。
* 按一下「系統」>「系統資訊」，回到系統資訊頁面。您會看到主控台視窗圖示。
* 按一下主控台圖示，以開啟主控台。接受所有安全警告。
* 連接主控台時，您會看到登入提示。
* 按一下「虛擬媒體」>「虛擬儲存空間」
* 移至 **CDROM&ISO** 標籤，然後選取**邏輯磁碟機類型**下的「ISO 檔案」
* 按一下**開啟映像檔**，然後在本端電腦上選取 ISO
* 按一下**外掛程式**，以將 ISO 插入至虛擬 CD-ROM 光碟機。
* 按一下**確定**。
* 將伺服器重新開機，並使用**從虛擬 CD-ROM 光碟機開機**選項。您可能需要在 iKVM 檢視器中使用虛擬鍵盤，才能選取開機裝置。

## 疑難排解

* 並非所有使用者都具有裝載「虛擬媒體」的預設存取權。如果發生許可權錯誤，請聯絡「支援中心」以取得「Root IPMI 使用者」許可權的更新。
* 如果已裝載 ISO，則會出現一則錯誤訊息，其文字為**已裝載磁碟**。您必須卸載現有磁碟，並將它取代為新的 ISO。可能無法同時裝載兩個 ISO。
* 您可能需要聯絡支援中心，以變更 BIOS 中的開機順序。
* 裝載 ISO 時，請使用 SSL VPN (http://vpn.softlayer.com)，而非 PPTP VPN。在連接至 VPN 網路之後，您也可以透過 IPMI 位址存取系統的 IPMI (https://<private-ip-IPMI-management>)。
* 當您輸入 ISO 的路徑時，請使用「UNC 名稱語法」（一般命名慣例）的路徑，例如：
  ```
  \\<NAS username>\<isoname>.iso
  ```
