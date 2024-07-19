---

copyright:
  years: 2023, 2024
lastupdated: "2024-07-19"

keywords: troubleshoot, tips, error, problem, troubleshoot bare metal, bare metal troubleshooting

subcollection: bare-metal

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Firmware upgrade issues
{: #bm-firmware-upgrade-issues}
{: troubleshoot}
{: support}

Firmware upgrade fails to complete successfully.
{: tsSymptoms}

One of the following issues can occur while you upgrade the firmware on a bare metal server.

- Firmware version mismatch
- Firmware update not running or not completing
- Hardware problem
- Server down after firmware update
{: tsCauses}

These issues can be fixed by using the following guidance.

Firmware version mismatch
   A known issue can occur after a firmware upgrade. The version in the portal does not update and shows the need for a firmware upgrade and displays the previous version.

   If you believe that the firmware was upgraded successfully, then compare the firmware version that is in the portal with the version that is in IPMI/IMM/xClarity system information.

   If the firmware version that is in IPMI/IMM/xClarity is different from what is in the portal, then [contact {{site.data.keyword.cloud}} Support](/docs/get-support?topic=get-support-using-avatar). You need to include a screenshot of the portal that shows the current and recommended firmware versions and a screenshot from IPMI, IMM, xClarity that shows the current firmware version that is on the server.

   If the versions match, then the firmware upgrade was probably unsuccessful. Retry the firmware upgrade. If the issue persists, [contact IBM Cloud Support](/docs/get-support?topic=get-support-using-avatar).

Firmware updates not running or not completing

   A firmware update might fail if the automation can't access the necessary server ports.
   For more information, see [tService network (on back-end/private network)](/docs/cloud-infrastructure?topic=cloud-infrastructure-ibm-cloud-ip-ranges#service-network).

Hardware problem

   If your server has a hardware fault, the firmware upgrade might not complete successfully.

   Check the IPMI/IMM/xClarity event log to determine whether it has hardware error messages. Also, check the health of the disks as described in [RAID commands](/docs/bare-metal?topic=bare-metal-bm-raid-controller-commands). If your server has a hardware or disk fault [contact {{site.data.keyword.cloud}} Support](/docs/get-support?topic=get-support-using-avatar).

Server down after firmware update

   On rare occasions, firmware updates can change the default boot disk. If your server cannot start after the firmware update, and you see an error in the remote console that no boot device was found, then most likely the boot order changed. Because you probably do not have access to the server BIOS, you can't change the boot order. So, you need to [contact {{site.data.keyword.cloud}} Support](/docs/get-support?topic=get-support-using-avatar) to review and change the boot order.

If you still can't upgrade the firmware [contact {{site.data.keyword.cloud}}Support](/docs/get-support?topic=get-support-using-avatar).
{: tsResolve}
