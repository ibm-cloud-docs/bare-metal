---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# 備份及回復

{{site.data.keyword.Bluemix_notm}} 提供各種可擴充[備份及儲存解決方案](https://www.softlayer.com/cloud-storage)，以符合您的備份需求。不過，我們不會完成客戶裝置的備份。帳戶上的使用者必須在您的裝置上起始所有已排定及一次性備份。

如果帳戶上有兩個以上的 {{site.data.keyword.baremetal_short}}，則可以將某個裝置中的資料備份到另一個裝置。「專用網路」資料流量沒有頻寬限制，因此，隨時可以將資料傳送或備份至共用帳戶的任何裝置。
{{site.data.keyword.baremetal_short}} 有數個備份解決方案，包括：

1. [Evault Backup](../infrastructure/backup/index.html) 是可在多部伺服器之間自動備份的企業備份解決方案。資料會儲存至企業 SAN（儲存區域網路）。
* [網路連接儲存空間 (NAS)](../infrastructure/network-attached-storage/nas.html) 是一種業界標準，提供重要資料的離線伺服器儲存空間。資料會儲存至企業 SAN（儲存區域網路）。
* [R1Soft CDP](../infrastructure/backup/r1soft.html) 提供高效能的磁碟對磁碟伺服器備份，其具有中央管理及資料儲存庫。R1Soft CDP 可保護區塊層次的資料，而伺服器上的唯一磁碟區塊只會在所有回復點上儲存一次，從而提高儲存空間效率。
