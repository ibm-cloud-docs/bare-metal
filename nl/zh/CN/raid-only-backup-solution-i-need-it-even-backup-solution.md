---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID 是我需要的唯一备份解决方案吗？它甚至是备份解决方案吗？

RAID 不是备份解决方案。RAID 用于创建单个可用数据磁盘，其中多个物理磁盘组合成一个阵列，速度更快和/或容错能力更强。

SoftLayer 提供了一些备份解决方案：

1. [Evault Backup](/infrastructure/backup/index.html) 是一种企业备份解决方案，可以跨多个服务器自动执行备份。数据会存储到企业 SAN（存储区域网络）中。
* [网络连接存储器 (NAS)](/infrastructure/network-attached-storage/nas.html) 是一种业界标准，可在服务器关闭时为关键数据提供存储。数据会存储到企业 SAN（存储区域网络）中。
* [R1Soft CDP](/infrastructure/backup/r1soft.html) 提供高性能磁盘到磁盘服务器备份，支持集中管理和数据存储库。R1Soft CDP 可在块级别保护数据，并且服务器上的唯一磁盘块在所有恢复点中仅存储一次，从而提高存储效率。
