---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-25"

keywords: bare metal, 3ware 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Checking the health of your 3ware RAID array
{: #bm-check-health-3ware-raid}

With 3ware, you can use a browser interface. However, unless you access the interface locally, it can be a security risk. Therefore, you use the command line interface.

You can download the 3ware CLI utilities from the [IBM Cloud CLI Plug-in Repository
](https://plugins.cloud.ibm.com/ui/repository.html#cf-plugins). For more information about the CLI utility, see [VPN CLI Plug-in for cf CLI](https://cloud.ibm.com/docs/cli?topic=cloud-cli-vpn_cli_for_cf).

**Quick command reference for 3ware CLI tools**

These devices must be followed by a number that identifies which devices is being queried.

tw_cli /c0 show (Output shows information that is needed to know the health of the RAID array)

./tw_cli /c1 show

Example:

    Unit  UnitType  Status         %Cmpl  Stripe  Size(GB)  Cache  AVerify  IgnECC

    ------------------------------------------------------------------------------

    u0    RAID-5    OK             -      64K     465.641   OFF    OFF      OFF    

    Port   Status           Unit   Size        Blocks        Serial

    ---------------------------------------------------------------

    p0     OK               u0     233.76 GB   490234752     WD-WCANY1727093

    p1     OK               u0     233.76 GB   490234752     WD-WCANY1622544

    p2     OK               u0     233.76 GB   490234752     WD-WCANY1657267

    p3     NOT-PRESENT      -      -           -             -

*note the following:

c = controller<br/>
Controller can be 0 or 1<br/>
u = unit<br/>
Unit number depends on number arrays. It is 0 in most cases.<br/>
p = port<br/>
Port denotes port number. In most cases, it is 0-4.
