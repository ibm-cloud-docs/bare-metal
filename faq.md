---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# FAQs: Bare metal servers

## Why is my BIOS asking for a password?

Currently {{site.data.keyword.cloud}} does not provide you with direct access to your BIOS. This is for a various number of reasons, but that is not to say you cannot make changes to the BIOS. If you need anything modified in the BIOS, including boot order, create a ticket under Support > Add Ticket through the [Customer Portal](control.softlayer.com) and request the specific changes you need.

\*\*NOTE\*\* This will require a reboot of your server to do, so please be ready to approve a reboot and/or provide a time frame for when you would like the change made.

## Do you provide complimentary OS Reloads?

Automated OS reloads are free and can be performed through the [Customer Portal](control.softlayer.com). These include customized OS reloads (changing operating systems, addition/removal of control panels/partition editing, and so on).  For detailed information on performing an OS Reload, refer to the [OS Reload procedure](../vsi/vsi_perform_os_reload.html).


## The primary drive on my bare metal server shows up as /dev/sdb. What is wrong?

This may be caused by the IPMI's Virtual Disk taking up the /dev/sda slot. This can be safely disabled by connecting to IPMIView and browsing to the Virtual Media tab. Select **Options > Disable** and click the **Apply** button to make the change. When the {{site.data.keyword.baremetal_short}} is rebooted next, the primary drive will display /dev/sda.


## Why is the CPU speed wrong?

If you log in to a server to check the CPU information and notice that the speed of the processors was incorrect. This discrepancy can be due to Enhanced Intel SpeedStep Technology (EIST). EIST is the Intel name for dynamic frequency scaling technology.  This technology is also called *CPU throttling* or *bus slewing* in older systems.  On some AMD systems, there are similar technologies that are called *Cool'N'Quiet* or *PowerNow!*.  Though these technologies are not all the same, they have the same goal, which is to lower the power consumption and heat production when the processor is not under heavy use by slowing the CPU speed.  When the server is back under load, they raise the clock speed as necessary.

If you would like to know whether the Intel processor on your server supports SpeedStep, customer portal: 
1. Click **Devices**.
* Identify your server in the list.
* Click the server name to view **Device Details**.
* Locate the subsection entitled **Hardware** to find the model number of your server's processors CPU speed.
* With the server processor model number, go to the [Intel Processor Finder](http://processorfinder.intel.com/) and use this number to find more information about the processor and whether it supports Enhanced Intel SpeedStep Technology.

EIST is an established technology. You should not have a reason to turn off EIST. However, if you decide that you do not want to use this feature, open a ticket with the Support Team to disable this feature.  To disable this this feature, the server will be rebooted.


## What if my bare metal server has out of date firmware?

Like software updates, it is important to keep firmware updated to ensure optimal device compatibility and stability. If a {{site.data.keyword.baremetal_short}} firmware is out of date, a firmware update may be initiated during the [OS Reload](../infrastructure/software/vsi_reload_os.html) process within the [Customer Portal](https://control.softlayer.com).

You can also update the firmware by selecting the bare metal server from the device list and selecting **Update Firmware** from the action menu drop down.
