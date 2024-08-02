---

copyright:
  years: 2017, 2024
lastupdated: "2024-08-02"

keywords:

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Checking the health of your 3ware&reg; RAID array
{: #bm-check-health-3ware-raid}

With 3ware, you can use a browser interface to check the health of your bare metal server. However, unless you access the interface locally, by using a browser is a security risk. Use the command-line interface instead.
{: shortdesc}

## Quick command reference for 3ware&reg; CLI tools
{: #3ware-quick-cli-command-ref}

These devices must be followed by a number that identifies which devices are being queried.

`tw_cli /c0` show (Output shows information that is needed to know the health of the RAID array)

./tw_cli /c1 show

Example:

    Unit  UnitType  Status         %Cmpl  Stripe  Size(GB)  Cache  AVerify  IgnECC

    ------------------------------------------------------------------------------

    u0    RAID-5    OK             -      64 K     465.641   OFF    OFF      OFF

    Port   Status           Unit   Size        Blocks        Serial

    ---------------------------------------------------------------

    p0     OK               u0     233.76 GB   490234752     WD-WCANY1727093

    p1     OK               u0     233.76 GB   490234752     WD-WCANY1622544

    p2     OK               u0     233.76 GB   490234752     WD-WCANY1657267

    p3     NOT-PRESENT      -      -           -             -

Quick reference notes:

c = controller (Controller can be 0 or 1)

u = unit (Unit number depends on number arrays. It is 0 in most cases.)

p = port (Port denotes port number. In most cases, it is 0-4.)
