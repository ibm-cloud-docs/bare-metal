---

copyright:
  years: 1994, 2024
lastupdated: "2024-08-01"

keywords: back up, recovery, IBM Cloud Backup, r1soft

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Back up and recovery
{: #sm-back-up-recovery}

{{site.data.keyword.cloud_notm}} provides various scalable [backup and storage solutions](https://www.ibm.com/cloud/storage){: external} to meet your backup requirements. However, {{site.data.keyword.cloud_notm}} does not complete backups of customer devices. A user on your account must initiate all scheduled and one-time backups on your devices.

If two or more {{site.data.keyword.baremetal_short}} exist on an account, data from one device can be backed up on another. No bandwidth limit is enforced for Private Network traffic, so data can be transferred between or backed up to any device that shares an account at any time. Several backup solutions are available for {{site.data.keyword.baremetal_short}}, including the following solutions:

* [IBM Cloud Backup](/docs/Backup?topic=Backup-getting-started#getting-started) is an enterprise backup solution that can automate backups across multiple servers. Data is stored to an enterprise SAN (storage area network).
* [Veeam on IBM Cloud](https://www.ibm.com/cloud/products/veeam){: external} delivers reliable backup and predicable disaster recovery for virtual and physical workloads.
* [R1Soft CDP](/docs/bare-metal?topic=bare-metal-ordering-r1soft) provides a high-performance disk-to-disk server backup that features a central management and data repository. R1Soft CDP protects data at block level, and a special disk blocks on the server are stored only once across all recovery points, increasing storage efficiency.
