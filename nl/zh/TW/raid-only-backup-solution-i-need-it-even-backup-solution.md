---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID 是唯一需要的備份解決方案嗎？它是備份解決方案嗎？

RAID 不是「備份」解決方案。RAID 會建立單一可用的資料磁碟，其中有數個實體磁碟會結合至一個陣列，以達到更好的速度及（或）容錯。

SoftLayer 提供一些備份解決方案：

1. [Evault Backup](../infrastructure/backup/index.html) 是可在多部伺服器之間自動備份的企業備份解決方案。資料會儲存至企業 SAN（儲存區域網路）。
* [網路連接儲存空間 (NAS)](../infrastructure/network-attached-storage/nas.html) 是一種業界標準，提供重要資料的離線伺服器儲存空間。資料會儲存至企業 SAN（儲存區域網路）。
* [R1Soft CDP](../infrastructure/backup/r1soft.html) 提供高效能的磁碟對磁碟伺服器備份，其具有中央管理及資料儲存庫。R1Soft CDP 可保護區塊層次的資料，而伺服器上的唯一磁碟區塊只會在所有回復點上儲存一次，從而提高儲存空間效率。
