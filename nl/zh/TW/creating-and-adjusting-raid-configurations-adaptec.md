---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 建立及調整 Adaptec RAID 配置

Adaptec RAID Bios 可讓您配置及管理 RAID 設定。如果您要使用[無 OS](introduction-no-os.html) 選項，而且想要設定特定磁碟機配置，請使用此 Bios。

## 存取 IPMI 裝置以與 RAID Bios 互動

不論您的機器是否有 Adaptec 控制器或 LSI 控制器，您都需要使用 IPMI 來存取伺服器，才能與 RAID Bios 互動。若要與 IPMI 互動，您需要先連接至 Adaptec {{site.data.keyword.IBM&reg; Cloud}} VPN。
1. 透過 [SSL](/infrastructure/vpn/ssl-vpn-connections.html) 或 PPTP，登入 VPN。請參閱 [VPN 主題頁面](/infrastructure/vpn/index.html)。
* 在[客戶入口網站](https://control.softlayer.com/)中，存取「裝置清單」。請參閱[存取裝置清單](/vsi/vsi_managing.html)。
* 按一下您要存取的裝置。
* 選取「遠端管理」標籤，以尋找您的伺服器 IPMI 存取詳細資料。
* 將 IPMI 裝置的 IP 放入瀏覽器中，並且登入。
* 若要開始與遠端主控台互動，請按一下「遠端控制」>「主控台重新導向」。

## 建立 RAID 陣列

在開機處理程序期間，按一下 Ctrl+A 以存取 Raid BIOS。

若要開始配置 RAID，請跳至「邏輯裝置配置」（第一個選項）。這會掃描您磁碟機的拓蹼，並顯示功能表，供您管理陣列、建立陣列，以及完成其他磁碟機管理作業。

下列範例顯示如何建立陣列。您會看到一份可用的磁碟機清單，供您用於建立「RAID 陣列」。

1. 若要選取磁碟機，請按空格鍵來移入*選取的磁碟機* 方框。
* 選取要在陣列中使用的所有磁碟機之後，請按 ENTER 鍵以移至 RAID 配置步驟。
* 選擇您要的 RAID 類型。如果您需要協助瞭解哪個 RAID 設定最符合您的需求，請參閱下列 [Adaptec 常見問題](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm)。
* 在配置期間，提供「陣列標籤」。最好在標籤中包括 RAID 類型（例如：RAID10-A）。
* 按 Enter 鍵，以導覽其餘的設定。使用預設值。

完成配置之後，選取「完成」即會建立 RAID。您可以從「主功能表」中選取「管理陣列」來查看新「陣列」。若要結束配置公用程式，請在系統提示您結束 Adaptec BIOS 之前 ESC 鍵。

## 移除現有陣列

如果您需要移除現有陣列，則會移至「管理陣列」>「選取要移除的陣列」，然後按「刪除」並確認。

## 範例配置

1. 在共有 6 個磁碟機的伺服器上，您可以在 RAID0 中針對作業系統設定 2 個 SSD，而在 RAID10 中針對實際資料設定 4 個額外磁碟機。這可讓您快速重新載入伺服器 OS，而不需要還原您的網站或服務資料（如果其位於次要陣列上）。

* 在 cPanel 伺服器上，您可以在個別「SSD RAID 陣列」上具有 /var 及 /home。因為這些是 cPanel 伺服器上 2 個 IO 最密集的目錄，所以您可能可以使用下列設定來減少網站回應時間：
  * RAID0（2 個 SATA 磁碟機）- /
  * RAID0（2 個 SSD 磁碟機）- /var
  * RAID0（2 個 SSD 磁碟機）- /home
  * RAID10（4 個 SATA 磁碟機）- /backup

* 使用單一 RAID 陣列來設定多個邏輯分割區。例如，使用 RADI1 中所設定的兩個 4TB 磁碟機。您可以分割 RAID，以符合您的需求。例如：
  * 作業系統的主要分割區：100GB
  * 資料的第二個分割區：500GB 
  * 備份的第三個分割區：剩餘空間
