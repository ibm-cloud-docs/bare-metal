---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Is RAID the only backup solution that I need? Is it even a backup solution?

RAID is not a Backup solution.  RAID creates a single usable data disk, where several physical disks are combined into an array for better speed and/or fault tolerance.

SoftLayer provides a few backups solutions:

1. [Evault Backup](/infrastructure/backup/index.html) is an enterprise backup solution that can automate backups across multiple servers. Data is stored to an enterprise SAN (storage area network).
* [Network Attached Storage (NAS)](/infrastructure/network-attached-storage/nas.html) is an industry standard, and provides off-server storage for critical data. Data is stored to an enterprise SAN (storage area network).
* [R1Soft CDP](../infrastructure/backup/r1soft.html) provides high-performance disk-to-disk server backup featuring a central management and data repository. R1Soft CDP protects data at block level, and unique disk blocks on the server are stored only once across all recovery points, increasing storage efficiency.
