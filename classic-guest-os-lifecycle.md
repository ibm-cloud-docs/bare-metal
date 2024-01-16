---

copyright:
  years: 2022, 2024
lastupdated: "2024-01-16"

keywords: operating system end of support (eos), add on end of support (eos)

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Lifecycle for operating systems and add-ons
{: #product-lifecycle-classic}

In the lifecycle of a product, end of support (EOS) is the last date that {{site.data.keyword.cloud}} delivers standard support for a version or release of a product. The end of support date is aligned to the vendor and community support dates. The EOS date is also the effective date that the product ceases to exist (is deprecated) and can no longer be ordered or purchased. See the following sections for operating system and add-on EOS dates for the Classic infrastructure.
{: shortdesc}

Boot disk sizes vary by operating system: Linux OS supports 25 GB and 100 GB. Windows supports only 100 GB.
{: note}

## Operating system lifecycles
{: #os-lifecycles-classic}

### Ciena vRouter (Vyatta)
{: #vrouter-classic}

Ciena vRouter is updated regularly with the previous release deprecating when a new version is released. For more information, see [About the VRA](/docs/virtual-router-appliance?topic=virtual-router-appliance-release-notes-for-ibm-virtual-router-appliance){: external}.

| Operating system | End of support |
|-----------------|----------------|
| 2208 (available only on bare metal servers) | 18 February 2025 |
| 2204 (available only on bare metal servers) | 04 October 2024 |
| 2110 (available only on bare metal servers) | 19 April 2024 |
| 2012 (available only on bare metal servers) | 14 June 2024 |
| 1912 (available only on bare metal servers) | 31 December 2022 |
| 1908 (available only on bare metal servers)  | 31 December 2022 |
{: caption="Table 1. Lifecycle for vRouter operating systems" caption-side="bottom"}

### CentOS
{: #centos-classic}

The following table describes the end of support date for CentOS operating systems. This guest OS is a free operating system. For more information, see [CentOS Linux](https://www.centos.org/about/){: external}.

| Operating system | End of support |
|-----------------|----------------|
| Stream 9 (available only on virtual servers) | [End of RHEL 9 full support phase](https://access.redhat.com/support/policy/updates/errata#Full_Support_Phase){: external}. |
| Stream 8 (available only on bare metal servers) | 31 May 2024 |
| CentOS 8.x | 31 December 2021  |
| CentOS 7.9 | 30 June 2024 |
| CentOS 6 | 30 November 2020 |
{: caption="Table 2. Lifecycle for CentOS operating systems" caption-side="bottom"}

 CentOS 8 doesn't support "Add on" software configurations. CentOS 8 also doesn't support the **Provision script** and **User data** selections for server configuration options. If you're migrating from a server that has "Add on" software configurations, you can choose to migrate to an earlier version.
{: important}

### Citrix XenServer
{: #xenserver-classic}

The following table describes the end of support date for Citrix XenServer operating systems. This guest OS is a free operating system. For more information, see [Citrix product matrix](https://www.citrix.com/support/product-lifecycle/product-matrix.html){: external}.

| Operating system | End of support |
|-----------------|----------------|
| 8.2 LTSR (available only on bare metal servers) | 30 June 2025 |
{: caption="Table 3. Lifecycle for Citrix XenServer operating systems" caption-side="bottom"}

### Debian
{: #debian-classic}

The following table describes the end of support date for Debian operating systems. This guest OS is a free operating system. For more information, see [Debian community](https://www.debian.org/){: external}.

| Operating system | End of support |
|-----------------|----------------|
| Debian 12 | 30 June 2028 |
| Debian 11 | 30 June 2026 |
| Debian 10 | 30 June 2024 |
| Debian 9  | 30 June 2022 |
{: caption="Table 4. Lifecycle for Debian operating systems" caption-side="bottom"}

Debian 10 doesn't support "Add on" software configurations. Debian 10 also doesn't support the **Provision script** and **User data** selections for server configuration options. If you're migrating from a server that has "Add on" software configurations, you can choose to migrate to an earlier version.
{: important}

### OSNEXUS (QuantaStor)
{: #osnexus-classic}

The following table describes the end of support date for OSNEXUS QuantaStor operating systems. This guest OS is a free operating system. For more information, see [OSNEXUS product notifications](https://wiki.osnexus.com/index.php?title=Product_EOL_Notifications){: external}.

| Operating system | End of support |
|-----------------|----------------|
| 5.x (available only on bare metal servers) | 30 April 2025 |
{: caption="Table 5. Lifecycle for OSNEXUS QuantaStor operating systems" caption-side="bottom"}

### Red Hat Enterprise Linux (RHEL)
{: #rhel-classic}

The following table describes the end of support date for RHEL operating systems. This guest OS is a paid operating system. For more information, see [Red Hat Enterprise Linux](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux){: external}.

| Operating system | End of support |
|-----------------|----------------|
| RHEL 9.2  | 31 May 2025 |
| RHEL 9.0  | 31 May 2024 |
| RHEL 8.8  | 31 May 2025 |
| RHEL 8.6  | 31 May 2024 |
| RHEL 8.4  | 31 May 2023 |
| RHEL 8.3  | 30 April 2021 |
| RHEL 8.2  | 30 April 2022 |
| RHEL 8.1  | 30 November 2021 |
| RHEL 7.9  | 30 June 2024 |
| RHEL 6 | 30 November 2020 |
{: caption="Table 6. Lifecycle for RHEL operating systems" caption-side="bottom"}

RHEL 8 and 9 don't support "Add on" software configurations. RHEL 8 and 9 also don't support the **Provision script** and **User data** selections for server configuration options. If you're migrating from a server that has "Add on" software configurations, you can choose to migrate to an earlier version.
{: important}

### Rocky Linux
{: #rocky-linux-classic}

Rocky Linux is updated regularly, with the previous release deprecating when a new version is released. This guest OS is a free operating system. For more information, see [Rocky Linux](https://rockylinux.org/){: external}.

| Operating system | End of support |
|-----------------|----------------|
| Rocky Linux 8.x | 31 May 2029 |
{: caption="Table 7. Lifecycle for Rocky Linux operating systems" caption-side="bottom"}

### Ubuntu LTS
{: #ubuntu-lts-classic}

The following table describes the end of support date for Ubuntu LTS operating systems. This guest OS is a free operating system. For more information, see [Ubuntu](https://ubuntu.com/){: external}.

| Operating system | End of support |
|-----------------|----------------|
| Ubuntu 22.04 minimal | 30 April 2027 |
| Ubuntu 20.04 minimal | 30 April 2025 |
| Ubuntu 18.04 minimal | 31 May 2023  |
| Ubuntu 16.04 minimal | 01 April 2021  |
{: caption="Table 8. Lifecycle for Ubuntu LTS operating systems" caption-side="bottom"}

### VMware
{: #vmware-classic}

The following table describes the end of support date for VMware operating systems. This guest OS is a free operating system. For more information, see [VMware lifecycle matrix](https://lifecycle.vmware.com/#/){: external}.

| Operating system | End of support |
|-----------------|----------------|
| 7 _all versions_ (available only on bare metal servers) | 02 April 2025 |
| 6.7 _all versions_ (available only on bare metal servers) | 15 October 2022 |
| 6.5 _all versions_ (available only on bare metal servers) | 15 October 2022 |
{: caption="Table 9. Lifecycle for VMware operating systems" caption-side="bottom"}

### Windows Server
{: #windows-server-classic}

The following table describes the end of support date for Windows Server operating systems. This guest OS is a paid operating system. For more information, see [Microsoft Windows Server](https://www.microsoft.com/en-us/windows-server){: external}.

| Operating system | End of support |
|-----------------|----------------|
| Windows Server 2022 | 14 October 2031 |
| Windows Server 2019 core | 09 January 2029 |
| Windows Server 2019 full standard | 09 January 2029 |
| Windows Server 2016 core | 11 January 2027 |
| Windows Server 2016 full standard  | 11 January 2027  |
| Windows Server 2012 full standard | 10 October 2023 |
| Windows Server 2012 R2 full standard | 10 October 2023 |
{: caption="Table 10. Lifecycle for Windows Server operating systems" caption-side="bottom"}

## Add-on software and hypervisor lifecycles
{: #add-on-lifecycles-classic}

The following table describes the end of support date for product add-ons and hypervisors.

| Add-on or hypervisor | End of support |
|--------|----------------|
| [Citrix Hypervisor 8.x](https://www.citrix.com/support/product-lifecycle/product-matrix.html){: external} | 25 June 2030 |
| [Citrix XenServer 7.x](https://www.citrix.com/support/product-lifecycle/product-matrix.html){: external} | 15 August 2022 |
| [cPanel 11.x](https://endoflife.software/applications/control-panels/cpanel){: external} | No EOS date announced |
| [Microsoft SQL Server 2022](https://learn.microsoft.com/en-us/lifecycle/products/sql-server-2022){: external} | 11 January 2033 |
| [Microsoft SQL Server 2019](https://learn.microsoft.com/en-us/lifecycle/products/sql-server-2019){: external} | 8 January 2030 |
| [Microsoft SQL Server 2017](https://learn.microsoft.com/en-us/lifecycle/products/sql-server-2017){: external} | 12 October 2027 |
| [Microsoft SQL Server 2014](https://learn.microsoft.com/en-us/lifecycle/products/sql-server-2014){: external} | 9 July 2024 |
| [Microsoft SQL Server 2012 Web](https://learn.microsoft.com/en-us/sql/sql-server/end-of-support/sql-server-end-of-support-overview?view=sql-server-ver16){: external} | 12 July 2022 |
| [Microsoft SQL Server 2012 Standard](https://learn.microsoft.com/en-us/sql/sql-server/end-of-support/sql-server-end-of-support-overview?view=sql-server-ver16){: external} | 12 July 2022 |
| [Microsoft SQL Server 2012 Enterprise](https://learn.microsoft.com/en-us/sql/sql-server/end-of-support/sql-server-end-of-support-overview?view=sql-server-ver16){: external} | 12 July 2022 |
| [MongoDB Community Edition 1.0](/docs/bare-metal?topic=bare-metal-product-lifecycle-classic#classic-mongodb-eos) | 20 November 2023 |
| [MySQL 5.7 on IBM Cloud Bare Metal](/docs/bare-metal?topic=bare-metal-product-lifecycle-classic#classic-mysql-eos) | 20 November 2023 |
| [Plesk Obsidian (Windows, Linux)](https://www.plesk.com/lifecycle-policy/){: external} | No EOS date announced |
| [R1Soft Server Backup Manager 6.x Enterprise](http://wiki.r1soft.com/display/ServerBackupManager/Server+Backup+6.16+Release+Notes){: external} | No EOS date announced |
| [Veeam Backup (Windows) 11.x](https://www.veeam.com/product-lifecycle.html){: external} | 29 February 2024 |
| [Veeam Backup (Windows) 9.x](https://www.veeam.com/product-lifecycle.html){: external} | 31 January 2022 |
{: caption="Table 11. Lifecycle for add-ons" caption-side="bottom"}

## End of Support (EOS) announcements
{: #classic-eos-announcements}

End of Support (EOS) is the last date that {{site.data.keyword.cloud}} delivers standard support for a version or release of a product. The end of support date is aligned to the vendor and community support dates. The EOS date is also the effective date that the product ceases to exist (is deprecated) and can no longer be ordered or purchased.

### MongoDB Community Edition 1.0 EOS
{: #classic-mongodb-eos}

MongoDB Community Edition 1.0 is free software available as an add-on to IBM Bare Metal Servers. Support for this software discontinues on 20 November 2023.

This deprecation has no impact on IBM Cloud Databases for MongoDB.
{: note}

Review the following details for this deprecation:

* After 20 November 2023, MongoDB Community Edition 1.0 is no longer supported. Which includes updates, bug fixes, and technical support for the product. After deprecation, clients can't download the software.
* If you are using MongoDB Community Edition 1.0, the software will continue to run after the EOS date. However, after this date, IBM will not provide support, including bug fixes or security updates.
* If you don't upgrade to the latest version, you do so at your own risk. The lack of support and updates can expose your systems and apps to security vulnerabilities and compatibility issues. See the following details about upgrading to the latest version.

For existing customers, upgrade to the latest version.

* To continue using MongoDB on IBM Cloud Bare Metal Servers, it is recommended that you upgrade to the latest supported version of MongoDB. By doing so, you can take advantage of new features, performance improvements, and security patches.
* To upgrade to the latest version of MongoDB, you can use either the open source version of MongoDB or bring your licensed copies to IBM Cloud Bare Metal servers. Alternatively, you can choose to migrate your databases to the IBM Cloud Databases for MongoDB service. By using IBM Cloud Databases, you can make sure that your database service remains supported and secure.
* For more information, see the following resources:
   * [BYOL: Install MongoDB](https://www.mongodb.com/docs/manual/installation/){: external}
   * [Upgrading to a new Major Version](/docs/databases-for-mongodb?topic=databases-for-mongodb-upgrading&interface=ui)
* IBM partners can [provide migration support](https://wanclouds.net/ibm-request){: external} to help you smoothly transition to the latest version of MongoDB. However, this migration support does come with a cost.

### MySQL 5.7 on IBM Cloud Bare Metal EOS
{: #classic-mysql-eos}

MySQL 5.7 on IBM Bare Metal Classic is free software available as an add-on to IBM Bare Metal Servers. Support for this software discontinues on 20 November 2023. The service will be removed from the IBM Cloud catalog on 21 September 2023.

This deprecation has no impact on IBM Cloud Databases for MySQL.
{: note}

Review the following details for this deprecation.

* After 20 November 2023, MySQL 5.7 on IBM Bare Metal Servers is no longer supported. Which includes updates, bug fixes, and technical support for the product. After this date, clients can't download the software.
* If you are using MySQL 5.7, the software will continue to run after the end-of-support date. However, after this date, IBM will not provide support, including bug fixes or security updates.
* If you don't upgrade to the latest version of MySQL and continue using MySQL 5.7, you do so at your own risk. The lack of support and updates can expose your systems and apps to security vulnerabilities and compatibility issues. See the following details about upgrading to the latest version.

For existing customers, upgrade to the latest version.

* To continue using MySQL, it is recommended that you upgrade to the latest supported version of MySQL, Version 8.0. By doing so, you can take advantage of new features, performance improvements, and security patches.
* To upgrade to the latest version of MySQL, you can use either the open source version of MySQL or bring your licensed copies to IBM Cloud Bare Metal. Alternatively, you can choose to migrate your databases to the IBM Cloud Databases for MySQL service. By using IBM Cloud Databases, you can make sure that your database service remains supported and secure.
* For more information, see the following resources:
   * [BYOL: Upgrading MySQL](https://dev.mysql.com/doc/refman/8.0/en/upgrading.html){: external}
   * [Migrating to Databases for MySQL](/docs/databases-for-mysql?topic=databases-for-mysql-migrating)
* IBM partners can [provide migration support](https://wanclouds.net/ibm-request){: external} to help you smoothly transition to the latest version of MySQL. However, this migration support does come with a cost.

### Microsoft SQL Server 2014 EOS
{: classic-ms-sql-server-2014-eos}

Microsoft SQL Server 2014 is a database software that is available as an add-on to IBM Bare Metal Servers. Support for this software ends on 9 July 2024. Which includes updates, bug fixes, and technical support for the product. After this date, clients can't download the software.

Review the following details for this deprecation:

* If you are using MS SQL Server 2014, the software will continue to 
run after the EOS date. However, after this date, IBM will not 
provide support, including bug fixes or security updates.
* If you don't upgrade to the latest version of Microsoft SQL Server 2022, the 
lack of support and updates can expose your systems and apps to 
security vulnerabilities and compatibility issues.

For existing customers, upgrade to the latest version.

* To continue using MS SQL Server on IBM Cloud Bare Metal and VSI 
Servers, it is recommended that you upgrade to the latest 
supported version of MS SQL Server 2022. By doing so, you can 
take advantage of new features, performance improvements, and 
security patches.
* IBM partners can provide [migration support](https://wanclouds.net/ibm-request){: external} to help you smoothly 
transition to the latest version of Microsoft SQL Server 2014. However, 
this migration support does come with a cost.
