---

copyright:
  years: 2023, 2025
lastupdated: "2025-07-17"

keywords:

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# End of support add-ons considerations
{: #eos-os-addon-bm-classic-intro}

If you have software add-ons that are at or past its end-of-support (EOS) date, security and stability risks are possible. The vendor no longer provides updates or security fixes for deprecated add-on versions.
{: short-desc}

Follow the guidance from your software add-on vendor on when to upgrade. IBM® doesn't require you to use supported software add-ons, but you assume the risks that are associated with using outdated software add-ons. Unsupported add-ons don't receive security updates or fixes. Risks with using outdated software addons can include security vulnerabilities and compatibility issues. Plan to modernize your instances' software add-ons before the EOS date. For more information, see [Lifecycle for operating systems and add-ons](/docs/bare-metal?topic=bare-metal-product-lifecycle-classic).

## Wanclouds&reg; partnership
{: #partner-bm-classic}

IBM has a partnership with Wan clouds. Contact [Wanclouds&reg;](https://wanclouds.net/ibm/request){: external} for more information. Using Wanclouds&reg; support incurs extra costs.

## End of Support (EOS) announcements
{: #bm-classic-eos-announcements}

End of Support (EOS) is the last date that {{site.data.keyword.cloud}} delivers standard support for a version or release of a product. The end of support date is aligned to the vendor and community support dates. The EOS date is also the effective date that the product ceases to exist (is deprecated) and can no longer be ordered or purchased.



### QuantaStor v6.x
{: classic-quantastor}

QuantaStor is a licensed software available as an add-on to IBM Bare Metal Servers. Support for this software discontinues on 31 July 2025. {{site.data.keyword.cloud}} is removing this service from the catalog on 31 July 2025.

You have the following options when QuantaStor is discontinued.

1. You can migrate to a different storage offering on your own. Other offerings include {{site.data.keyword.cloud}} Object Storage, {{site.data.keyword.cloud}} Block Storage, or {{site.data.keyword.cloud}} File Storage.
1. You can use the assistance of an IBM partner to migrate to a different storage offering.
1. You can continue with QuantaStor on {{site.data.keyword.cloud}} at your own risk.
1. You can purchase the QuantaStor license directly from the vendor, OSNEXUS, for access to the most recent updates, bug fixes, security updates, and support.

If you switch to another storage offering, you must first migrate data from S3 compatible buckets on QuantaStor VSAs as a source directly to {{site.data.keyword.cloud}} Object Storage, {{site.data.keyword.cloud}} Block Storage, or {{site.data.keyword.cloud}} File Storage. For more information, see the following pages:

* [Getting started with {{site.data.keyword.cloud}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage)
* [Getting started with Block Storage for Classic](/docs/BlockStorage?topic=BlockStorage-getting-started)
* [Getting started with File Storage for Classic](/docs/FileStorage?topic=FileStorage-getting-started)

**{{site.data.keyword.cloud}} Object Storage**
The following are two options to migrate data from Quantastor s3 compatible buckets to {{site.data.keyword.cloud}} Object Storage.

1. Komprise&reg; Elastics Data Migration tool
   The Komprise&reg; Elastics Data Migration tool is available through the {{site.data.keyword.cloud}} catalog as pat of Komprise&reg; Intelligent Data Management or as a stand-alone tool.

   For more information, see [Komprise&reg; Elastic Data Migration](https://cloud.ibm.com/catalog/services/komprise-elastic-data-migration?catalog_query=aHR0cHM6Ly9jbG91ZC5pYm0uY29tL2NhdGFsb2c%2Fc2VhcmNoPWtvbXByaXNlI3NlYXJjaF9yZXN1bHRz#about), [Komprise&reg; Intelligent Data Management Suite](https://cloud.ibm.com/catalog/services/komprise-intelligent-data-management-suite?catalog_query=aHR0cHM6Ly9jbG91ZC5pYm0uY29tL2NhdGFsb2c%2Fc2VhcmNoPWtvbXByaXNlI3NlYXJjaF9yZXN1bHRz#about).
1. Rclone&reg; is an open source tool. {{site.data.keyword.cloud}} does not support Rclone&reg;. The Rclone&reg; tool can be used for migrating from s3 sources to s3 targets. Rclone&reg; can be used for migrating from s3 sources to s3 targets, or migrating data from NAS file shares to s3 Cloud Object Storage buckets.

   For more information, see [Using Rclone&reg;](/docs/cloud-object-storage?topic=cloud-object-storage-rclone) and [Rclone&reg; documentation](https://rclone.org/docs/){: external}.

### MySQL 8.0 for Linux on {{site.data.keyword.cloud}} Classic EOS
{: #classic-mysql-eos-bm-classic}

MySQL 8.0 on {{site.data.keyword.cloud}} Classic servers is a free software that is available as an add-on to {{site.data.keyword.cloud}} Classic servers. Support for this software discontinues on 30 April 2026. MySQL 8.0 is planned for removal from the {{site.data.keyword.cloud}} catalog on 30 April 2026.

This deprecation has no impact on {{site.data.keyword.cloud}} Databases for MySQL.
{: note}

Review the following details for this deprecation.

* When MySQL 8.0 is removed from the IBM Cloud Classic Catalog, you can't provision new servers with MySQL 8.0.
*	All support that includes security updates and bug fixes for MySQL 8.0, stops after 30 April 2026, but you can keep using it at your own risk. 
*	Support for existing servers with MySQL 8.0 ends on 30 April 2026.

To plan for this deprecation, see the following recommendations.

* To make sure that you have uninterrupted usage of this software, we recommend the following actions. By using these alternatives, you can continue using MySQL without interruption.
   - DIY Installation. MySQL packages are available on Linux distributions.
   - Opting for the BYOL (Bring Your Own License) option to upgrade to MySQL 8.4.
*	You can use the following documentation for seamless self-installation and upgrades [Installing MySQL on Linux by using the MySQL Yum Repository](https://dev.mysql.com/doc/mysql-installation-excerpt/8.0/en/linux-installation-yum-repo.html){: external}.
* You can connect with any partner of your choice or choose an IBM partner with paid support to help with migration by using [Wanclouds IBM request]([https://wanclouds.net/ibm](https://wanclouds.net/ibm/request)){: external}. If you have any questions or need assistance, open a [support case](/docs/account?topic=account-open-case) in the customer portal.

### MSSQL Server 2016
{: #classic-mysql-server-2016-eos-bm-classic}

MSSQL Server 2016 on IBM Cloud® Classic servers is a Database software that is available as an add-on to IBM Cloud® Classic servers. Support for this software discontinues on 14 July 2026. MSSQL Server 2016 is planned for removal from the IBM Cloud® catalog on 14 June 2026.

All support that includes security updates and bug fixes for MSSQL Server 2014 stops on 14 July 2026, but you can continue with MSSQL Server 2014 at your own risk. 

To plan for this deprecation, see the following recommendations.

* To make sure that you have uninterrupted usage of this software, we recommend that you upgrade to most recent version of MSSQL Server that is available on IBM Cloud.
* 	To upgrade, you need to perform an OS reload with the latest version of the software.
* 	You can connect with any partner of your choice or choose an IBM partner such as [Wanclouds] ([https://wanclouds.net/ibm](https://wanclouds.net/ibm/request)){: external}. If you have any questions or need assistance, open a [support case](/docs/account?topic=account-open-case) in the customer portal.
