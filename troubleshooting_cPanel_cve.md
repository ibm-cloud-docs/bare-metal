---

copyright:
  years: 2026, 2026
lastupdated: "2026-07-13"

keywords: troubleshoot bare metal, bare metal troubleshooting, cPanel CVE

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# What do I do if I suspect my server is affected by a cPanel vulnerability?
{: #troubleshoot-cPanel-cve}
{: troubleshoot}
{: support}

If you suspect that an {{site.data.keyword.baremetal_long}} is affected by a cPanel security vulnerability, you need update to the current cPanel version and change the server password. If the server is compromised, you need to reload the operating system or restore from backup.
{: shortdesc}

You received a notification from {{site.data.keyword.cloud}} alerting you to a CVE from cPanel that might compromise your server. Or, you discover that you can't access the server, unable to log in as root, or with WHM.
{: tsSymptoms}

cPanel, a third-party vendor that provides an add-on for {{site.data.keyword.baremetal_long}}, published a critical CVE on 28 April 2026 for an authentication bypass vulnerability that might compromise your root password and cPanel environment.
{: tsCauses}

Review the article that is provided by cPanel: [Security: CVE-2026-41940 - cPanel and WHM / WP2 Security Update 28 April 2026](https://support.cpanel.net/hc/en-us/articles/40073787579671-Security-CVE-2026-41940-cPanel-WHM-WP2-Security-Update-04-28-2026){: external}.
{: tsResolve}

Follow its instructions to update your environment immediately with the most recent patch and to determine whether your server is compromised. As a best practice, change the root password for the server. If you determine that the server is compromised, then reload the operating system or restore from backup to recover the server.

## Update to the most recent cPanel version
{: #update-latest-cpanel-version}

Follow the instructions in the [CVE-2026-41940 article](https://support.cpanel.net/hc/en-us/articles/40073787579671-Security-CVE-2026-41940-cPanel-WHM-WP2-Security-Update-04-28-2026){: external} to update your environment immediately with the most recent patch. The version of cPanel currently available through the {{site.data.keyword.cloud}} portal is the most recent fixed version.

## Access the server and change the password
{: #access-server-and-change-password}

To maintain a secure environment, change the root password. If you can't log in as root, reset the password from the {{site.data.keyword.cloud}} console.

To reset the password, follow these steps:

1. Start rescue mode on the device. Refer to [Starting rescue mode](/docs/bare-metal?topic=bare-metal-launching-rescue) for steps.
1. Connect to the {{site.data.keyword.cloud}} SSL VPN.
1. Access the server by using KVM. Follow the steps for your device type.
    - Bare Metal Servers for Classic: [How do I use IPMI?](/docs/bare-metal?topic=bare-metal-bm-faq#how-do-i-use-ipmi) or [Why can't I access IPMI with my browser?](/docs/bare-metal?topic=bare-metal-bm-IPMI-not-accessible)

1. Run the following commands in rescue mode by using KVM or KVM IPMI console:

   ```bash
   mount /dev/sda2 /mnt
   mount /dev/sda1 /mnt/boot/
   mount --bind /dev /mnt/dev
   mount --bind /sys /mnt/sys
   mount --bind /proc /mnt/proc
   chroot /mnt
   passwd
   ```
   {: codeblock}

1. When you run the `passwd` command, you can set a new password for the device. Make sure that you record your password. You can also update it on the details screen in the {{site.data.keyword.cloud}} console. For more information, see [Managing software passwords](/docs/bare-metal?topic=bare-metal-cp_bpmanacctresp).

## Recover the server if compromised
{: #recover_server_compromised}

If you determine that the server is compromised, you can restore from a backup or reload the operating system. Refer to the [CVE-2026-41940 article](https://support.cpanel.net/hc/en-us/articles/40073787579671-Security-CVE-2026-41940-cPanel-WHM-WP2-Security-Update-04-28-2026){: external} for how to review if the server is compromised. See also the cPanel article [What do I do if I believe that my server was hacked?](https://support.cpanel.net/hc/en-us/articles/360057223334-What-do-I-do-if-I-believe-my-server-has-been-hacked){: external}.

To restore from backup, follow the instructions for the [Back up and recovery](/docs/bare-metal?topic=bare-metal-sm-back-up-recovery) solution that you selected.

To reload the OS, go to the **Device list**, select the server to show the _Device details_ page, then select **Actions** > **OS reload**. For more information, see [Reloading the OS](/docs/bare-metal?topic=bare-metal-reloading-the-os).

   - You might need to change the operating system version during the operating system reload if your current one is past its end of support. For more information, see [End of support for operating systems considerations](/docs/bare-metal?topic=bare-metal-eos-os-considerations-bm-classic-intro).
   - To use the most recent cPanel version on Linux systems, select the most recent Ubuntu version as the operating system during reload. CentOS and Rocky Linux are no longer supported by cPanel.
   - OS reloads clear all data from the device. If needed, use a backup of the server to restore it if you reload the operating system.

## Getting help
{: #getting-help}

If you need help with recovery, you can [get support](/docs/support?topic=support-using-avatar&interface=ui#getting-support) by creating a case or reporting an issue, as defined by your support plan.
