---

copyright:
  years: 2023, 2025
lastupdated: "2025-10-24"

keywords:

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# End of support for operating systems considerations
{: #eos-os-considerations-bm-classic-intro}

If you use an operating system (OS) that is at or past its end-of-support (EOS) date, security and stability risks are possible. The vendor no longer provides updates or security fixes for deprecated OS versions.
{: short-desc}

Follow the guidance from your OS vendor on when to upgrade. IBM® doesn't require you to migrate your active instances to a supported OS, but you assume the risks that are associated with using an outdated OS. Unsupported operating systems don't receive security updates or fixes and can't be used to deploy new instances. Plan to modernize the instances' OS before the EOS date. For more information, see [Lifecycle for operating systems and add-ons](/docs/bare-metal?topic=bare-metal-product-lifecycle-classic).
Available options when you modernize your OS.

When you plan for an OS EOS, keep the following information in mind:
-You can use the assistance of an IBM partner.
-You can upgrade your instances on your own.
-Continue with your EOS OS (at your own risk).


## Available options when you modernize your OS
{: #options-when-upgrading-os-bm-classic}

When you plan for an OS EOS, keep the following information in mind:

* You can use the assistance of an IBM partner. 
* You can upgrade your instances on your own.
* Continue with your EOS OS (at your own risk).

### Wanclouds partnership
{: #partner-bm-classic}

IBM has a partnership with Wan clouds. Contact [Wan clouds]() for more information.

### Upgrade your OS on your own
{: #upgrade-os-bm-classic}

If you decide to upgrade your OS yourself, you can use one of three options:
- Side-by-side upgrade (migration).
- OS Reload

Follow your OS vendor's guidance when you upgrade your OS.

#### Side-by-side upgrades
{: #side-by-side-upgrade-bm-classic}

When you upgrade with the side-by-side method, you create a new instance with the new OS version. You must migrate data and applications from the old instance after the new instance is created. Extra charges are incurred if both instances are active in a side-by-side upgrade.

If your server is over 5 years old, you can encounter issues when you upgrade your OS. To avoid potential hardware issues, you can replace your server with a newer option.
{: important}

Best practices for side-by-side upgrades:
-Read your OS vendor's documentation to understand the differences between the old and new OS versions.
-Consider the instance downtime that is required for the upgrade.
-Create a backup of your original instance. For more information, see [Getting started with IBM Cloud backup for Classic](/docs/Backup?topic=Backup-getting-started).
-Test that the new instance with the updated OS works properly before you migrate data or delete your original instance.

#### OS Reload
{: #os-reload-bm-classic}

With OS Reload, you can reconfigure a device with a different operating system. Along with the OS reload feature, you can use the OS reload with disk preservation option.

**OS reload with disk preservation**
OS reload with disk preservation option configures your current primary disk as a secondary disk while all data is retained and creates a new primary disk. 
Disk preservation converts the primary drive to a portable storage device. This option is available only on virtual devices and incurs charges based on the billing patterns of the device. Charges can be canceled by canceling the portable storage device anytime after it was created.

**Best practices for OS Reload upgrades:**
- Read your OS vendor's documentation to understand the differences between the old and new OS versions.
- See [Reloading the OS](/docs/bare-metal?topic=bare-metal-reloading-the-os).
- Consider the instance downtime that is required for the upgrade.
- Create a backup of your original instance. For more information, see [Getting started with IBM Cloud Backup for Classic](/docs/Backup?topic=Backup-getting-started).

### Continue with your EOS OS at your own risk
{: #continue-eos-os-bm-classic}

If you choose to continue with an EOS OS, consider the following information:

- The EOS OS can't receive security updates.
- The OS isn't tested for hardware, drivers, or firmware.
- Support isn't available for performance or operational issues on the server with an EOS OS.
   - Vendor support is unavailable for an EOS OS.
   - EOS operating systems are not supported by {{site.data.keyword.Bluemix_notm}} Technical Support.

## End of Support (EOS) announcements
{: #bm-classic-eos-announcements}

End of Support (EOS) is the last date that {{site.data.keyword.cloud}} delivers standard support for a version or release of a product. The end of support date is aligned to the vendor and community support dates. The EOS date is also the effective date that the product ceases to exist (is deprecated) and can no longer be ordered or purchased.

### SUSE Linux Enterprise Server (SLES) 12 
{: sles-12-eos-bm-clasic}

SUSE Linux Enterprise Server (SLES) 12 EOS date is 31 October 2024. After deprecation, clients can't download the software.

Clients are encouraged to upgrade to the most recent version for continued support. If an upgrade isn't possible, SUSE Long-Term Support Service (LTSS) is available that offers extended security updates and bug fixes for three more years. LTSS requires an extra monthly fee per instance.

For more information about upgrading, see [SUSE documentation](https://documentation.suse.com/sles/15-SP6/single-html/SLES-upgrade/#sec-upgrade-paths-supported){: external} or contact [IBM support](/docs/account?topic=account-using-avatar).

### Debian 10
{: debian-ten-eos-bm-clasic}

Debian 10 EOS date is 30 June 2024. Support for this software discontinues on 30 June 2024. After deprecation, clients can't download the software. For existing customers, upgrade to the latest version. For more information, see the [Debian documentation](https://www.debian.org/releases/bookworm/amd64/release-notes/ch-upgrading.en.html){: external}.

### Red Hat Enterprise Linux 7
{: #upgrading-rhel-7-os-bm-classic}

Red Hat Enterprise Linux 7 EOS date is 30 June 2024. Support for this software discontinues on 30 June 2024. After deprecation, clients can't download the software.

For existing customers, upgrade to the latest version. For more information, see the [Red Hat Enterprise Linux documentation](https://access.redhat.com/support/policy/updates/errata).

### Windows 2012 and Windows 2012 R2 EOS
{: #windows-2012-bm-clssic}

Windows Server 2012 and Windows Server 2012 R2 EOS date is 10 October 2023. For more information, see [Overview of Windows Server upgrades](https://learn.microsoft.com/en-us/windows-server/get-started/upgrade-overview){: external}.
No additional licensing costs are incurred to move to a newer software version when you use IBM’s License Included options. IBM Cloud® is governed by the Service Provider License Agreement (SPLA) with Microsoft. For more information, see [License Mobility Deployment Process](/docs/microsoft?topic=microsoft-microsoft-license-mobility-process).

### CentOS 7 and CentOS Stream 8
{: #upgrading-centos-7}

CentOS 7 EOS date is 30 June 2024. Support for this software discontinues on 30 June 2024. After deprecation, clients can't download the software.

CentOS Stream 8 EOS date is 31 May 2024. Support for this software discontinues on 31 May 2024. After deprecation, clients can't download the software.

To migrate workloads from CentOS, you can switch to a compatible OS distribution, or choose a different operating system. Compatible distributions include CentOS Stream 9, Rocky Linux 8 and 9, and RHEL 8 and 9. You can also migrate to a different OS such as Debian or Ubuntu LTS. Options when you migrate includes an OS reload, a side-by-side upgrade, or you can migrate to a new server.

### Ubuntu 20.04
{: ubuntu-twenty-eos-bm-clasic}

Ubuntu 20.04 EOS date is 31 May 2025. Support for this software discontinues on 31 May 2025. After deprecation, clients can't download the software. 

For existing customers, upgrade to the latest version. For more information, see the [Ubuntu documentation](https://ubuntu.com/20-04){external}.

### Debian 11
{: #debian-11-eos-bk-classic}

Debian 11 EOS date is 31 August 2026. Support for this software discontinues on 31 August 2026. On 31 July 2026, Debian 11 reaches its End of Marketing (EOM) and can't be downloaded. For existing customers, upgrade to the latest version. For more information, see the [Debian documentation]([https://ubuntu.com/20-04](https://www.debian.org/releases/stable/i386/release-notes/ch-upgrading.html)){: external}.
