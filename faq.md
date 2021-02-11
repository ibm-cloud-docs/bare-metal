---

copyright:
  years: 2014, 2021
lastupdated: "2021-02-09"

keywords: bare metal, faq, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:note: .note}
{:external: target="_blank" .external}

# FAQs: Bare metal servers
{: #bm-faq}

## What is UEFI boot mode?
{: faq}
The Unified Extensible Firmware Interface (UEFI) is a specification for the software interface between an operating system and firmware.

IBM Cloud support for BIOS boot mode is phasing out in favor of UEFI.

For more information about UEFI, see your hardware manufacturer documentation or go to [https://uefi.org/](https://uefi.org/){: external}.

## Why is my BIOS asking for a password?
{: faq}

Currently, {{site.data.keyword.cloud}} does not provide you with direct access to your BIOS, for various reasons. However, you can change the BIOS. If you need to modify anything in the BIOS, including boot order, create a support case by going to **Support > Create a Case** through the [{{site.data.keyword.cloud_notm}} console](https://cloud.ibm.com/){: external} and request the specific changes that you need.

This change requires a restart of your server, so be ready to approve a restart and provide a timeframe for when you want to implement like the changes.
{:note}

## Do you provide complimentary OS Reloads?
{: faq}

Automated OS reloads are free and can be performed through the [{{site.data.keyword.cloud_notm}} console](https://cloud.ibm.com/){: external}. These include customized OS reloads (changing operating systems, addition or removal of control panels, and partition editing, and so on). For more information about performing an OS Reload, see [OS Reload procedure](/docs/bare-metal?topic=bare-metal-reloading-the-os).


## The primary drive on my bare metal server shows up as /dev/sdb. What is wrong?
{: faq}

This problem can be caused by the IPMI's Virtual Disk taking up the /dev/sda slot. You can safely disable primary drive by connecting to IPMIView and browsing to the Virtual Media tab. Select **Options > Disable** and click **Apply** to make the change. When the {{site.data.keyword.baremetal_short}} is restarted next, the primary drive displays /dev/sda.


## Why is the CPU speed wrong?
{: faq}

If you log in to a server and notice that the speed of the processors is incorrect, this discrepancy might be caused by Enhanced Intel SpeedStep Technology (EIST). EIST is the Intel name for dynamic frequency scaling technology. This technology is also called *CPU throttling* or *bus slewing* in older systems. Some AMD systems use similar technologies that are called *Cool'N'Quiet* or *PowerNow!*. Though these technologies are not all the same, they have the same goal, which is to reduce the power consumption and heat production when the processor is not under heavy use by slowing the CPU speed. When the server is back under load, they raise the clock speed as necessary.

If you want to know whether the Intel processor on your server supports SpeedStep, use this procedure from the customer {{site.data.keyword.cloud}} console:
1. Click **Devices**.
* Identify your server in the list.
* Click the server name to view **Device Details**.
* Locate the subsection entitled **Hardware** to find the model number of your server's processors CPU speed.
* With the server processor model number, go to the [Intel Processor Finder](http://processorfinder.intel.com){: external} and use this number to find more information about the processor and whether it supports Enhanced Intel SpeedStep Technology.

EIST is an established technology. It's not common that you need to turn off EIST. However, if you decide that you do not want to use this feature, open a ticket with the Support Team to disable this feature. The server is restarted when you disable EIST.


## What if my bare metal server has out-of-date firmware?
{: faq}

It is important to keep firmware updated to make sure that your bare metal server has optimal device compatibility and stability. If a {{site.data.keyword.baremetal_short}} firmware version is out of date, firmware can be updated by selecting the bare metal server from the device list and selecting **Update Firmware** from the action menu.

You can initialize a firmware update during the [OS Reload](/docs/bare-metal?topic=bare-metal-reloading-the-os) process within the [{{site.data.keyword.cloud_notm}}](https://cloud.ibm.com/){: external}.

You can't initialize a firmware update when a bare metal server is powered ON. Make sure that the bare metal server is powered OFF before you initialize a firmware update. 
{: important}

## What happens to drives in bare metal servers when a customer is finished with them?
{: faq}

When a server is cancelled, the reclaim processes starts and any associated drives are wiped by using `DOD 5220.22-M` algorithms. The reclaim is tracked through the serial numbers on the drives. After the drives are wiped, the server moves into provisioning for reassignment. 

## What happens to a bare metal drive if it malfunctions?
{: faq}

A drive malfunction prompts manual intervention and the drive is set to end of life. The end of life process initiates when the drive malfunctions or if the age or size is beyond support. When any of these conditions occur, the drive is wiped as described previously. Then, the drive is physically destroyed by breaking, crushing, or shredding. The physical destruction process is tracked by using the serial number on the drive.

## Can I see what bare metal servers are available for purchase?
{: faq}

Yes! You can now see what servers are available in what data center when you provision a bare metal server. But, this option is available for only the hourly offering. You cannot see server availability with the monthly offering. For more information about provisioning a bare metal server, see [Selecting from fast provisioning servers](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers#bm-select-popular-servers).

## How do I use IPMI?
{: faq}

IPMI is a way to manage a server remotely through a network interface. Gather the IPMI address and login information from the {{site.data.keyword.cloud}} console under *Devices* > _your server (device details)_> *Remote Mgmt*. Next, establish a VPN connection to the server. You can then connect by pointing your web browser to the IP address or by using a [Standalone VPN clinet](/docs/iaas-vpn?topic=iaas-vpn-standalone-vpn-clients).
