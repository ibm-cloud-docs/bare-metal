---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 裸機伺服器上的主要磁碟機顯示為 /dev/sdb。哪裡出錯？

原因可能是 IPMI 中使用 /dev/sda 插槽的「虛擬磁碟」。連接至 IPMIView 並瀏覽至「虛擬媒體」標籤，即可放心地予以停用。選取**選項 > 停用**，然後按一下**套用**按鈕來進行變更。下次將裸機伺服器重新開機時，主要磁碟機會顯示 /dev/sda。
