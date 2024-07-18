---

copyright:
  years: 2023, 2024
lastupdated: "2024-07-11"

keywords:

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# End of support add-ons considerations
{: #eos-os-addon-bm-classic-intro}

If you have a software add-on that is at or past its end-of-support (EOS) date, security and stability risks are possible. The vendor no longer provides updates or security fixes for deprecated add-on versions.
{: short-desc}

Follow the guidance from your software add-on vendor on when to upgrade. IBM® doesn't require you to use supported software add-ons, but you assume the risks that are associated with using outdated software add-ons. Unsupported add-ons don't receive security updates or fixes. Risks with using outdated software addons can include security vulnerabilities and compatibility issues. Plan to modernize your instances' software add-ons before the EOS date. For more information, see [Lifecycle for operating systems and add-ons](/docs/bare-metal?topic=bare-metal-product-lifecycle-classic).

## Wanclouds partnership
{: #partner-bm-classic}

IBM has a partnership with Wan clouds. Contact [Wanclouds](https://wanclouds.net/ibm/request){: external} for more information. Using Wanclouds support incurs additional costs.

## End of Support (EOS) announcements
{: #bm-classic-eos-announcements}

End of Support (EOS) is the last date that {{site.data.keyword.cloud}} delivers standard support for a version or release of a product. The end of support date is aligned to the vendor and community support dates. The EOS date is also the effective date that the product ceases to exist (is deprecated) and can no longer be ordered or purchased.


  
### QuantaStor v6.x
{: classic-quantastor}

QuantaStor is a free software available as an add-on to IBM Bare Metal Servers. Support for this software discontinues on 31 July 2025. The service will be removed from the IBM Cloud catalog on 31 July 2025.

You have the following options when QuantaStor is discontinued.
1. You can migrate to a different storage offering on your own. Other offerings include IBM Cloud Object Storage, IBM Cloud Block Storage, or IBM Cloud File Storage.
2. You can use the assistance of an IBM partner to migrate to a different storage offering.
3. You can continue with QuantaStor on IBM Cloud at your own risk.
4. You can purchase the QuantaStor license directly from the vendor, OSNEXUS, for access to the latest updates, bug fixes, security updates, and support.

If you switch to another storage offering, you must first migrate data from S3 compatible buckets on QuantaStor VSAs as a source directly to IBM Cloud Object Storage, IBM Cloud Block Storage, or IBM Cloud File Storage. For more information, see [Getting started with IBM Cloud Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage), [Getting started with Block Storage for Classic](/docs/BlockStorage?topic=BlockStorage-getting-started), [Getting started with File Storage for Classic](/docs/FileStorage?topic=FileStorage-getting-started).

**IBM Cloud Object Storage**
The following are two options to migrate data from Quantastor s3 compatible buckets to IBM Cloud Object Storage.

1. Komprise Elastics Data Migration tool
   The Komprise Elastics Data Migration tool is available through the IBM Cloud Catalog as pat of Komprise Intelligent Data Management or as a stand-alone tool.
   
   For more information, see [Komprise Elastic Data Migration](https://cloud.ibm.com/catalog/services/komprise-elastic-data-migration?catalog_query=aHR0cHM6Ly9jbG91ZC5pYm0uY29tL2NhdGFsb2c%2Fc2VhcmNoPWtvbXByaXNlI3NlYXJjaF9yZXN1bHRz#about), [Komprise Intelligent Data Management Suite](https://cloud.ibm.com/catalog/services/komprise-intelligent-data-management-suite?catalog_query=aHR0cHM6Ly9jbG91ZC5pYm0uY29tL2NhdGFsb2c%2Fc2VhcmNoPWtvbXByaXNlI3NlYXJjaF9yZXN1bHRz#about).

2. Rclone is an open source tool. IBM does not support rclone. The Rclone tool can be used for migrating from s3 sources to s3 targets. Rclone can be used for migrating from s3 sources to s3 targets, or migrating data from NAS file shares to s3 Cloud Object Storage buckets.
   
   For more information, see [Using rclone](/docs/cloud-object-storage?topic=cloud-object-storage-rclone), [Rclone documentation](https://rclone.org/docs/){: external}.
