---

copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Checking the health of your 3ware RAID array

With 3ware, you can use a browser interface. However, unless you access the interface locally, it can be a security risk. Therefore, you use the command line interface.

<!--You can download the 3ware CLI utilities the software Library, located in the bottom of Customer Portal.  Please check http://downloads.service.softlayer.com for the latest version (VPN access required to access the downloads page). -->

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
