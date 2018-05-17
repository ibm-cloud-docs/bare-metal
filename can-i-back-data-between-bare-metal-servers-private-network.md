---

copyright:
  years: 1994, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Back up and recovery

{{site.data.keyword.Bluemix_notm}} provides a variety of scalable [backup and storage solutions](https://www.softlayer.com/cloud-storage) to meet your backup requirements. However, {{site.data.keyword.Bluemix_notm}} does not complete backups of customer devices. A user on your account must initiate all scheduled and one-time backups on your devices.

If two or more {{site.data.keyword.baremetal_short}} exist on an account, data from one device can be backed up on another. No bandwidth limit is enforced for Private Network traffic, so data can be transferred between or backed up to any device that shares an account at any time. Several backup solutions are available for {{site.data.keyword.baremetal_short}}, including the following solutions:

1. [Evault Backup](../infrastructure/backup/index.html) is an enterprise backup solution that can automate backups across multiple servers. Data is stored to an enterprise SAN (storage area network).
* [Network Attached Storage (NAS)](../infrastructure/network-attached-storage/nas.html) is an industry standard, and provides off-server storage for critical data. Data is stored to an enterprise SAN (storage area network).
* [R1Soft CDP](../infrastructure/backup/r1soft.html) provides high-performance disk-to-disk server backup that features a central management and data repository. R1Soft CDP protects data at block level, and unique disk blocks on the server are stored only once across all recovery points, increasing storage efficiency.
