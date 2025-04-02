---

copyright:
  years: 2017, 2025
lastupdated: "2025-04-02"

keywords: bare metal security patches, security patch

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Operating system updates and security patches
{: #bm-system-updates-patches}

To maintain a secure and stable cloud environment, you need to regularly check for updates and apply patches to your operating systems. Keeping your environment up to date helps protect your systems from vulnerabilities, security threats, and performance issues.
{: shortdesc}

To help maintain the security and performance of your server, you need to check for and apply updates immediately after the server completes a provision or reload.

Your server operating system and applications do not automatically install new packages or security updates. As the server owner or system administrator, you are responsible for maintaining security by regularly updating and patching your system.
{: important}

Ignoring updates can expose your server to security vulnerabilities. Always verify and install the most recent updates to keep your system secure.

{{site.data.keyword.cloud}} Classic infrastructure provides access to the following internal-hosted update services through a private network.

* Locally hosted repository mirrors for multiple Linux distributions
* Microsoft Server Update Services (WSUS)
* Red Hat Satellite infrastructure
* Locally hosted SUSE for SAP repository

Keep in mind that you aren't required to use the {{site.data.keyword.cloud}} Classic update services. You can receive updates directly from vendors.

## Security patches
{: #bm-security-patches}

The {{site.data.keyword.IBM}} Private Network uses dedicated services (Microsoft Server Update Services and Red Hat Network) for security updates. Upon delivery, all {{site.data.keyword.baremetal_short}} are set, by default, to automatically update for security patches.

## Operating system update information
{: #bm-os-update-information}

Use the following table to help you prepare for updates and security patches.

| Operating system | Update information |
| -----------------|-----|
| VMware | Make sure that your VMware environment is up to date by checking for security patches and updates. See the official [VMware Security Advisories](https://www.broadcom.com/support/vmware-security-advisories){: external} page for the latest updates. |
| Red Hat Enterprise Linux (RHEL) | Red Hat frequently releases security updates to address vulnerabilities. Stay updated by going to [Red Hat Security Advisories](https://access.redhat.com/security/security-updates/){: external}. |
| Microsoft Windows | Microsoft provides regular security updates for Windows operating systems. Check for updates through Windows Update or see the [Microsoft Security Update Guide](https://msrc.microsoft.com/update-guide/){: external}. |
| CentOS Stream|  CentOS Stream provides a continuously delivered distribution. Make sure that you are using a supported version and check for updates by going to the [CentOS Download](https://www.centos.org/download/){: external} page. |
| Rocky Linux | Rocky Linux provides security patches and updates to keep your system protected. Make sure that you are using a supported version and check for updates by in the [Rocky Linux Release and Version Guide](https://wiki.rockylinux.org/rocky/version/){: external}. |
| Debian | Debian regularly releases security updates to maintain system stability and security. Stay updated by going to the Rocky Linux [Security Information](https://www.debian.org/security/){: external} page. |
| Ubuntu | Ubuntu provides frequent security patches and updates for both LTS and non-LTS releases. Check for updates by going to the [Ubuntu Security Notices](https://ubuntu.com/security/notices){: external}. |
{: caption="Table 1: Opetating system update and security patch information " caption-side="bottom"}

## Recommended actions
{: #bm-recommended-actions-security}

By keeping your operating systems updated, you can reduce the risk of security breaches and help maintain a more stable cloud environment. If you need more help, see to the official vendor documentation.

See the following tips and recommended actions.

* **Regularly check for updates**. Make sure that you enable automatic updates where possible or manually check vendor websites for critical patches.
* **Promptly apply security patches**. Delayed updates expose your system to security risks.
* **Review any vendor advisory notices**. Make sure that you subscribe to security advisories from each vendor to stay informed about potential vulnerabilities.
* **Perform compatibility testing**. Before you apply major updates, test them in a controlled environment to make sure that they are stable.
* **Schedule regular maintenance**. Establish a routine patch management process to keep systems secure and up to date.
