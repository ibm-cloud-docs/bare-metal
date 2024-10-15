---

copyright:
  years: 2014, 2024
lastupdated: "2024-10-15"

subcollection: bare-metal

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQs: Bare metal servers
{: #bm-faq}

## What is UEFI boot mode?
{: #what-is-uefi}

The Unified Extensible Firmware Interface (UEFI) is a specification for the software interface between an operating system and firmware.

{{site.data.keyword.cloud}} is phasing out support for BIOS boot mode in favor of UEFI.

For more information about UEFI, see your hardware manufacturer documentation or go to [https://uefi.org/](https://uefi.org/){: external}.

## Why is my BIOS asking for a password?
{: #why-is-bios-asking-password}

{{site.data.keyword.cloud}} does not provide you with direct access to your BIOS. However, you can change the BIOS. If you need to modify anything in the BIOS, including boot order, open a [support case](/docs/get-support?topic=get-support-open-case) and request the changes that you need.

This change requires a restart of your server, so be ready to approve a restart and provide a time frame for when you want to implement like the changes.
{: note}

## Do you provide complimentary OS Reloads?
{: #do-you-provide-comp-os-reloads}

Automated OS reloads are free and are performed through the [{{site.data.keyword.cloud_notm}} console](https://cloud.ibm.com/){: external}. Customized OS reloads (such as changing operating systems, addition or removal of control panels, and partition editing) are included. For more information about performing an OS Reload, see [OS Reload procedure](/docs/bare-metal?topic=bare-metal-reloading-the-os).

## The primary drive on my bare metal server shows up as /dev/sdb. What is wrong?
{: #primary-drive-dev-sdb}

This problem can be caused by the IPMI's Virtual Disk taking up the _/dev/sda_ slot. You can safely disable the primary drive by connecting to IPMIView and clicking the **Virtual Media** tab. Select **Options > Disable** and click **Apply** to make the change. When the {{site.data.keyword.baremetal_short}} is restarted next, the primary drive displays _/dev/sda_.

## Why is the CPU speed wrong?
{: #why-cpu-speed-wrong}

If you log in to a server and notice that the speed of the processors is incorrect, this discrepancy might be caused by Enhanced Intel SpeedStep Technology (EIST). EIST is the Intel&reg; name for dynamic frequency scaling technology. This technology is also called **CPU throttling** or _bus slewing_ in older systems. Some AMD systems use similar technologies that are called **Cool'N'Quiet** or **PowerNow**. Though these technologies are not all the same, they have the same goal. They reduce the power consumption and heat production when the processor isn't under heavy use by slowing the CPU speed. When the server is back under load, the clock speed is raised as necessary.

If you want to know whether the Intel processor on your server supports SpeedStep, use the following procedure from the {{site.data.keyword.cloud}} console:

1. Click **Devices**.
1. Identify your server in the list.
1. Click the server name to view **Device Details**.
1. Locate the **Hardware** subsection to find the model number of your server's processors CPU speed.
1. With the server processor model number, go to the [Intel processor finder](https://ark.intel.com/content/www/us/en/ark.html){: external} and use this number to find more information about the processor and whether it supports Enhanced Intel SpeedStep Technology.

EIST is an established technology. It's not common that you need to turn off EIST. However, if you decide that you don't want to use this feature, open a [support case](/docs/get-support?topic=get-support-using-avatar) to disable this feature. The server is restarts when you disable EIST.

## How do I update my out-of-date bare metal server firmware?
{: #bm-out-of-date-firmware}

It's important to keep the firmware updated to make sure that your bare metal server has optimal device compatibility and stability. If a {{site.data.keyword.baremetal_short}} firmware version is out of date, you can update the firmware by selecting the bare metal server from the device list and click **Update firmware** from the action menu. Make sure that you back up your data before you update the firmware.

You can also initialize a firmware update during the [OS Reload](/docs/bare-metal?topic=bare-metal-reloading-the-os) process within the [{{site.data.keyword.cloud_notm}}](https://cloud.ibm.com/){: external}.

You can't initialize a firmware update when a bare metal server is powered ON. Make sure that the bare metal server is powered OFF before you initialize a firmware update.
{: important}

Firmware updates take up to 4 hours to complete. If the update takes longer than 4 hours, check for an open support case. If a support case isn't open, [contact support or open a case](/docs/get-support?topic=get-support-using-avatar).

## What happens to drives in bare metal servers when I cancel the server?
{: #what-happens-bm-drive-when-cancel}

When a server is cancelled, the reclaim process starts, and any associated drives are wiped by using `DOD 5220.22-M` algorithms. These algorithms use a 3-pass overwrite process to securely erase data. The reclaim is tracked through the serial numbers on the drives. After the drives are wiped, the server moves into provisioning for reassignment.

## What happens to a bare metal drive if it malfunctions?
{: #what-happens-drive-if-bm-malfunctions}

A drive malfunction prompts manual intervention and the drive is set to end of life. The end of life process initiates when the drive malfunctions or if the age or size is beyond support. When any of these conditions occur, the drive is wiped as mentioned in the previous section. Then, the drive is physically destroyed by breaking, crushing, or shredding. The physical destruction process is tracked by using the serial number on the drive.

## Can I see what bare metal servers are available for purchase?
{: #can-see-available-bms}

Yes! You can now see what servers are available in what data center when you provision a bare metal server. But, this option is available for only the hourly offering. You cannot see server availability with the monthly offering. For more information about provisioning a bare metal server, see [Selecting from fast provisioning servers](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers#bm-select-popular-servers).

## How do I use IPMI?
{: #how-do-i-use-ipmi}

IPMI is a way to manage a server remotely through a network interface. Gather the IPMI address and login information from the {{site.data.keyword.cloud}} console under **Devices** > _your server (device details)_> **Remote Mgmt**. Next, establish a VPN connection to the server. You can then connect by pointing your web browser to the IP address or by using a [Stand-alone VPN client](/docs/iaas-vpn?topic=iaas-vpn-standalone-vpn-clients).

## What operating system tasks are my responsibility?
{: #what-os-tasks-are-my-responsibility}

Operating system tasks are the exclusive responsibility of the customer in the infrastructure as a service (IaaS) model. For details on which tasks are the responsibility of {{site.data.keyword.cloud}}, the customer, or shared, see the Infrastructure as a service section in [Shared responsibilities for using IBM Cloud products](/docs/overview?topic=overview-shared-responsibilities#iaas-services-responsibilities) and [Understanding IaaS basics](/docs/cloud-infrastructure?topic=cloud-infrastructure-getting-started-tutorial#cloud-svc-models-2).

{{site.data.keyword.cloud}} support assists with basic questions about instructions or considerations for product use in the {{site.data.keyword.cloud}} environment. For extensive operating system questions beyond the scope of {{site.data.keyword.cloud}} support, refer to the vendor-specific software documentation.
