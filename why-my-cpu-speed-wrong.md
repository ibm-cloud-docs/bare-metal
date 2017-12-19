---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Why is the CPU speed wrong?

If you log in to a server to check the CPU information and notice that the speed of the processors was incorrect. This discrepancy can be due to Enhanced Intel SpeedStep Technology (EIST). EIST is the Intel name for dynamic frequency scaling technology.  This technology is also called *CPU throttling* or *bus slewing* in older systems.  On some AMD systems, there are similar technologies that are called *Cool'N'Quiet* or *PowerNow!*.  Though these technologies are not all the same, they have the same goal, which is to lower the power consumption and heat production when the processor is not under heavy use by slowing the CPU speed.  When the server is back under load, they raise the clock speed as necessary.

If you would like to know whether the Intel processor on your server supports SpeedStep, customer portal: 
1. Click **Devices**.
* Identify your server in the list.
* Click the server name to view **Device Details**.
* Locate the subsection entitled **Hardware** to find the model number of your server's processors CPU speed.
* With the server processor model number, go to the [Intel Processor Finder](http://processorfinder.intel.com/) and use this number to find more information about the processor and whether it supports Enhanced Intel SpeedStep Technology.

EIST is an established technology. You should not have a reason to turn off EIST. However, if you decide that you do not want to use this feature, open a ticket with the Support Team to disable this feature.  To disable this this feature, the server will be rebooted.
