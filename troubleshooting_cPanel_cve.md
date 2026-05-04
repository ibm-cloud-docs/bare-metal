---

copyright:
  years: 2026, 2026
lastupdated: "2026-05-04"

keywords: troubleshoot bare metal, bare metal troubleshooting, cPanel CVE

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# What do I do if I suspect my server is affected by a cPanel vulnerability?
{: #troubleshoot-cPanel-cve}
{: troubleshoot}
{: support}

If you suspect that an {{site.data.keyword.baremetal_long}} is affected by a cPanel security vulnerability, you should update to the latest cPanel version, change the server password. If the server is compromised, you should also perform an OS Reload or restore from backup.
{: shortdesc}

You received a notification from {{site.data.keyword.cloud}} alerting you to a CVE from cPanel that might compromise your server. Or you discover that you are unable to access the server, unable to log in to root, or with WHM.
{: tsSymptoms}

cPanel, a third-party vendor that provides an add-on for {{site.data.keyword.baremetal_long}}, published a critical CVE on 28 April 2026 for an authentication bypass vulnerability that could compromise your root password and cPanel environment.
{: tsCauses}

Review the article provided by cPanel: [Security: CVE-2026-41940 - cPanel & WHM / WP2 Security Update 04/28/2026](https://support.cpanel.net/hc/en-us/articles/40073787579671-Security-CVE-2026-41940-cPanel-WHM-WP2-Security-Update-04-28-2026){: external}.
{: tsResolve}

Follow its instructions to update your environment immediately with the latest patch and to determine if your server is compromised. As a best practice, change the root password for the server. If you determine that the server is compromised, then perform an OS Reload or restore from backup to recover the server.

## Update to the latest cPanel version
{: #update-latest-cpanel-version}

Follow the instructions in the [CVE-2026-41940 article](https://support.cpanel.net/hc/en-us/articles/40073787579671-Security-CVE-2026-41940-cPanel-WHM-WP2-Security-Update-04-28-2026){: external} to update your environment immediately with the latest patch. The version of cPanel currently available through the {{site.data.keyword.cloud}} portal is the latest patched version.

## Access the server and change the password
{: #access-server-and-change-password}

To maintain a secure environment, change the root password. If you cannot log in as root, reset the password from the {{site.data.keyword.cloud}} console.

To reset the password, follow these steps:

1. Launch rescue mode on the device. Refer to [Starting rescue mode](/docs/bare-metal?topic=bare-metal-launching-rescue) for steps.
1. Connect to the {{site.data.keyword.cloud}} SSL VPN.
1. Access the server using KVM. Follow the steps for your device type.
    - Bare Metal Servers for Classic: [How do I use IPMI?](/docs/bare-metal?topic=bare-metal-bm-faq#how-do-i-use-ipmi) or [Why can't I access IPMI with my browser?](/docs/bare-metal?topic=bare-metal-bm-IPMI-not-accessible)

1. Run the following commands in rescue mode using KVM or KVM IPMI console:

   ```bash
   mount /dev/xvda2 /mnt
   mount /dev/xvda1 /mnt/boot/
   mount --bind /dev /mnt/dev
   mount --bind /sys /mnt/sys
   mount --bind /proc /mnt/proc
   chroot /mnt
   passwd
   ```
   {: codeblock}

1. When you run the `passwd` command, you can set a new password for the device. Make sure to record your password. You can also update it on the details screen in the {{site.data.keyword.cloud}} console. For more information, see [Managing software passwords](/docs/bare-metal?topic=bare-metal-cp_bpmanacctresp).

## Recover the server if compromised
{: #recover_server_compromised}

If you determine that the server is compromised, you can restore from a backup or perform an OS Reload. Refer to the [CVE-2026-41940 article](https://support.cpanel.net/hc/en-us/articles/40073787579671-Security-CVE-2026-41940-cPanel-WHM-WP2-Security-Update-04-28-2026){: external} for how to review if the server is compromised.  See also the cPanel article [What do I do if I believe my server has been hacked?](https://support.cpanel.net/hc/en-us/articles/360057223334-What-do-I-do-if-I-believe-my-server-has-been-hacked){: external}.

To restore from backup, follow the instructions for the [Back up and recovery](/docs/bare-metal?topic=bare-metal-sm-back-up-recovery) solution that you selected.

To reload the OS, you go to the **Device list**, select the server to show the _Device details_ page, then select **Actions** > **OS reload**. For details, refer to [Reloading the OS](/docs/bare-metal?topic=bare-metal-reloading-the-os).

   - Be aware that you might need to change the operating system version during OS Reload if your current one is past its end of life.  See [End of support for operating systems considerations](/docs/bare-metal?topic=bare-metal-eos-os-considerations-bm-classic-intro) for more information.
   - To use the latest cPanel version on Linux systems, select Ubuntu 22.04 during the OS Reload because CentOS and Rockly Linux are no longer supported by cPanel.
   - OS reloads clear all data from the device. If needed, use a backup of the server to restore it following an OS reload.

## Getting help
{: #getting-help}

If you require assistance with recovery, visit the IBM Cloud Support Center to [get support](/docs/support?topic=support-using-avatar&interface=ui#getting-support) by creating a case or reporting an issue, as defined by your support plan.
