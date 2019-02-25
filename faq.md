---

copyright:
  years: 2014, 2019
lastupdated: "2018-04-02"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}

# FAQs: Bare metal servers

## Why is my BIOS asking for a password?
{: faq}

Currently, {{site.data.keyword.cloud}} does not provide you with direct access to your BIOS, for a variety of reasons. However, you can change the BIOS. If you need anything to be modified in the BIOS, including boot order, create a ticket under Support > Add Ticket through the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window} and request the specific changes that you need.

\*\*NOTE\*\* This requires a reboot of your server to do, so be ready to approve a reboot and/or provide a time frame for when you would like the change made.

## Do you provide complimentary OS Reloads?
{: faq}

<<<<<<< HEAD
Automated OS reloads are free and can be performed through the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window}. These include customized OS reloads (changing operating systems, addition/removal of control panels/partition editing, and so on).  For more information on performing an OS Reload, refer to the [OS Reload procedure](/docs/infrastructure/software?topic=software-reloading-the-os).
=======
Automated OS reloads are free and can be performed through the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window}. These include customized OS reloads (changing operating systems, addition/removal of control panels/partition editing, and so on).  For more information on performing an OS Reload, refer to the [Reloading the OS](/docs/infrastructure/software?topic=software-reloading-the-os#reloading-the-os).
>>>>>>> origin/master


## The primary drive on my bare metal server shows up as /dev/sdb. What is wrong?
{: faq}

This can be caused by the IPMI's Virtual Disk taking up the /dev/sda slot. You can safely disabled by connecting to IPMIView and browsing to the Virtual Media tab. Select **Options > Disable** and click the **Apply** button to make the change. When the {{site.data.keyword.baremetal_short}} is rebooted next, the primary drive will display /dev/sda.


## Why is the CPU speed wrong?
{: faq}

If you log in to a server to check the CPU information and notice that the speed of the processors was incorrect. This discrepancy can be due to Enhanced Intel SpeedStep Technology (EIST). EIST is the Intel name for dynamic frequency scaling technology.  This technology is also called *CPU throttling* or *bus slewing* in older systems.  Some AMD systems have  similar technologies that are called *Cool'N'Quiet* or *PowerNow!*.  Though these technologies are not all the same, they have the same goal, which is to reduce the power consumption and heat production when the processor is not under heavy use by slowing the CPU speed.  When the server is back under load, they raise the clock speed as necessary.

If you would like to know whether the Intel processor on your server supports SpeedStep, use this procedure from the customer portal:
1. Click **Devices**.
* Identify your server in the list.
* Click the server name to view **Device Details**.
* Locate the subsection entitled **Hardware** to find the model number of your server's processors CPU speed.
* With the server processor model number, go to the [Intel Processor Finder ![External link icon](../icons/launch-glyph.svg "External link icon")](http://processorfinder.intel.com/){: new_window} and use this number to find more information about the processor and whether it supports Enhanced Intel SpeedStep Technology.

EIST is an established technology. It's not common that you need to turn off EIST. However, if you decide that you do not want to use this feature, open a ticket with the Support Team to disable this feature.  To disable this feature, the server is rebooted.


## What if my bare metal server has out-of-date firmware?
{: faq}

Like software updates, it is important to keep firmware updated to ensure optimal device compatibility and stability. If a {{site.data.keyword.baremetal_short}} firmware is out of date, a firmware update may be initiated during the [OS Reload](/docs/infrastructure/software?topic=software-reloading-the-os) process within the [{{site.data.keyword.slportal}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://control.softlayer.com/){: new_window}.

You can also update the firmware by selecting the bare metal server from the device list and selecting **Update Firmware** from the action menu.

## What happens to drives in bare metal servers when a customer is finished with them?
{: faq}

Upon cancellation, a server is automatically moved to a reclaim VLAN for a set hold time. Once complete, the reclaim processes start and the drive are wiped by using DOD 5220.22-M algorithms.  The reclaim is tracked by using the serial number on the drive. After completion, the server is moved into provisioning for reassignment. A drive malfunction prompts manual intervention and the drives are then set to end of life.

The end of life process is initiated when there is a malfunction or if the age or size is beyond support. Once any of these conditions occur, the drives are wiped as described earlier. Upon completion of the wiping process, the drive is physically destroyed by breaking, crushing, or shredding the device.  The physical destruction process is tracked by using the serial number on the drive.
