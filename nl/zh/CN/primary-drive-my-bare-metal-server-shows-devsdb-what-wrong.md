---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 裸机服务器上的主驱动器显示为 /dev/sdb。出了什么问题？

导致此问题的原因可能是 IPMI 的“虚拟盘”占用 /dev/sda 槽。可以通过连接到 IPMIView 并浏览到“虚拟介质”选项卡来安全禁用此功能。选择**选项 > 禁用**，然后单击**应用**按钮以进行更改。下次重新引导裸机服务器时，主驱动器将显示 /dev/sda。
