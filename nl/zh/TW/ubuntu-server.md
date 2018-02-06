---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 在裸機伺服器上安裝 Ubuntu 伺服器

如果您要使用 {{site.data.keyword.IBM&reg; Cloud}} 未提供的作業系統，則可以藉由裝載自訂 ISO（磁碟映像檔）來將它們安裝至裸機伺服器。若要裝載 ISO 上傳，則會將它上傳至與伺服器相關聯的「檔案儲存空間 (NAS)」。若要將 ISO 上傳至 NAS，請使用下列程序，以使用 IPMI 來裝載 ISO。
1. 使用**無作業系統**來訂購「裸機伺服器」 
* 您也可以選取免費可用 OS（例如 CentOS）作為可用來連接至 NAS 的作業系統。
* 訂購 NAS 儲存空間，以儲存「可開機 ISO」。如果您已有任何 Windows CIFS 伺服器，則可以使用它來共用 ISO 映像檔。使用此 Windows CIFS 伺服器，您將取得含 20GB 容量的舊式 NAS。佈建 NAS 之後，即可從客戶入口網站中查看 NAS 的說明。
* 從 https://www.ubuntu.com/download/server 下載 ISO 映像檔。
* 將 ISO 映像檔上傳至 NAS 或「Windows CIFS 伺服器」。如果您有 NAS 儲存空間，則可以使用 FTP 來上傳 ISO 映像檔。

  範例 FTP 程序：
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
  
* 使用 IPMI 建立與 {{site.data.keyword.Bluemix_notm}} 的「VPN 連線」。您可以從「支援」功能表或下列 URL 來啟動 VPN 功能表：[VPN 存取](http://www.softlayer.com/VPN-Access)
* 使用「透過管理 IP 連接至 IPMI」，以從「IPMI 虛擬媒體功能表」裝載 ISO 映像檔。
  1. 檢視 IPMI 認證
  * 記載 IPMI 視圖
  * 開啟「虛擬媒體」標籤
  * 您需要具有 IPMI「管理者」專用權的 root 使用者。如果專用權顯示為*操作員*，請開立支援問題單，以將專用權變更為「管理者」。
  * 填寫 ISO 映像檔連線詳細資料
    共用主機 = NAS 的 IP 位址<br/範例：10.3.x.x
    映像檔的路徑 = ISO 檔案的名稱，格式如下：\NASusername\imagefilesname.iso（即 \SLNxxxxxx\SLE-12-SP1-Server-DVD-x86_64-GM-DVD1.iso）
    使用者 = NAS 的使用者名稱
    密碼 = NAS 的密碼
  * 按一下**裝載**按鈕
  * 確認裝置
* 按一下並啟動「KVM 檢視器」，然後從「虛擬媒體」功能表中開啟「虛擬儲存空間」頁面。如果您成功將 ISO 映像檔裝載為 CDROM 裝置，則會在**連線狀態歷程**中看到裝置說明。
* 透過 SoftLayer 問題單，要求您的伺服器將其「虛擬 CD-ROM」作為第一個裝置開機。針對每一部伺服器完成此要求。您可以在安裝 OS 之後變更開機設定。
  **附註**：您可能不需要聯絡支援中心，即可變更 BIOS 中的開機順序。這視您的伺服器而定。請嘗試重新開機一次，以確認開機順序。
* 從 KVM 視圖將伺服器重新開機。
* 從裝載的 ISO 映像檔安裝 OS。
* 將 Ubuntu OS 從 ISO 安裝至裸機伺服器。
* 配置網路設定（IP 位址/子網路/閘道/DNS 等等）。如果您未在安裝步驟期間正確地配置它，則在重新開機之後，只能透過 KVM 主控台連接至此伺服器。

* 卸載「虛擬媒體」。您應該透過「IPMI 虛擬媒體」標籤，從伺服器卸載虛擬媒體。
* 將伺服器重新開機。
* 重新開機之後，即可透過 SSH 存取伺服器。
