---

copyright:
  years: 2017, 2019
lastupdated: "2018-07-10"

keywords: raid, adaptec, ipmi, raid bios, raid array, RAID configuration

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 建立及調整 Adaptec RAID 配置
{: #bm-create-raid-config}

Adaptec RAID BIOS 可讓您配置及管理 RAID 設定。如果您要使用[無 OS](/docs/bare-metal?topic=bare-metal-the-no-os-option) 選項，而且想要設定特定磁碟機配置，請使用此 BIOS。

## 存取 IPMI 裝置以與 RAID BIOS 互動
{: #bm-access-ipmi}

不論您的機器是否有 Adaptec 控制器或 LSI 控制器，您都需要存取使用 IPMI 的伺服器，才能與 RAID BIOS 互動。若要與 IPMI 互動，您需要先連接至 Adaptec {{site.data.keyword.cloud}} VPN。
1. 透過 [SSL](/docs/infrastructure/iaas-vpn?topic=VPN-setup-ssl-vpn-connections#setup-ssl-vpn-connections) 或 PPTP，登入 VPN。
* 存取 [{{site.data.keyword.slportal}} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/){: new_window} 中的「裝置清單」。請參閱[存取裝置清單](/docs/infrastructure/vsi?topic=virtual-servers-managing-virtual-servers)。
* 按一下您要存取的裝置。
* 選取「遠端管理」標籤，以尋找您伺服器的 IPMI 存取詳細資料。
* 將 IPMI 裝置的 IP 放入瀏覽器中，並且登入。
* 若要開始與遠端主控台互動，請按一下**遠端控制 > 主控台重新導向**。

## 建立 RAID 陣列
{: #bm-create-raid-array}

在啟動程序期間，按下 **Ctrl+A** 以存取 RAID BIOS。

若要開始配置 RAID，請開啟「邏輯裝置配置」（第一個選項）。這個選項會掃描您磁碟機的拓蹼，並顯示功能表，供您管理陣列、建立陣列，以及完成其他磁碟機管理作業。

下列範例顯示如何建立陣列。您會看到一份可用的磁碟機清單，供您用於建立「RAID 陣列」。

1. 若要選取磁碟機，請按空格鍵來移入*選取的磁碟機* 方框。
* 選取要在陣列中使用的所有磁碟機之後，請按 ENTER 鍵以移至 RAID 配置步驟。
* 選擇您要使用的 RAID 類型。如果您需要協助以瞭解哪個 RAID 設定最符合您的需求，請參閱下列 [Adaptec 常見問題 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm){: new_window}。
* 在配置期間，提供「陣列標籤」。最好在標籤中包括 RAID 類型（例如：RAID10-A）。
* 按 **Enter** 鍵，以前往其餘的設定。使用預設值。

完成配置之後，選取「完成」即會建立 RAID。您可以從主功能表中選取「管理陣列」來查看新「陣列」。若要結束配置公用程式，請在系統提示您結束 Adaptec BIOS 之前 ESC 鍵。

## 移除現有的 RAID 陣列
{: #bm-remove-raid-array}

如果您需要移除現有陣列，請移至**管理陣列**、選取要移除的陣列，然後按**刪除**並確認。

## 範例配置
{: #bm-example-config}

1. 在共有六個磁碟機的伺服器上，您可以在 RAID 0 中針對作業系統設定兩個 SSD，而在 RAID 10 中針對實際資料再多設定四個磁碟機。使用此配置可讓您快速重新載入伺服器的 OS，而不需要還原您的網站或服務資料（如果其位於次要陣列上）。

* 在 cPanel 伺服器上，您可以在個別「SSD RAID 陣列」上具有 /var 及 /home。因為目錄是 cPanel 伺服器上兩個 IO 最密集的目錄，所以您可能可以使用下列設定來減少網站回應時間：
  * RAID0（2 個 SATA 磁碟機）- /
  * RAID0（2 個 SSD 磁碟機）- /var
  * RAID0（2 個 SSD 磁碟機）- /home
  * RAID10（4 個 SATA 磁碟機）- /backup

* 使用單一 RAID 陣列來設定多個邏輯分割區。例如，使用在 RAID 1 中設定的兩個 4 TB 磁碟機。您可以分割 RAID 以符合您的需求。請參閱下列範例：
  * 作業系統用的主要分割區：100 GB
  * 資料用的第二個分割區：500 GB
  * 備份用的第三個分割區：剩餘空間
