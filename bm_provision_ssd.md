---



copyright:
  years: 2017, 2018
lastupdated: "2018-04-02"

subcollection: bare-metal


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Provisioning an Intel Optane-compatible bare metal server
To provision a bare metal server with an Intel Optane drive:
1. Use the procedure: [Building a custom bare metal server](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server).
* Select the following options on the order form:

|Section|Option to select
|------|------|
|Region-Data Center|To use the Intel Optane drive, select one of the following data centers:<br>Europe - AMS03, FRA02, LON02, OSL01<br>NA South DAL09, DAL10, DAL12<br>Asia-Pacific - MEL01<br>NA East - MON01, TOR01, WDC04<br>NA West - SJC03<br>|
|Server|1. Select **All servers**<br>2. Select *Dual Processors*<br>3. Select one of the following servers<br>-Intel Xeon 4110, up to 12 drives<br>-Intel Xeon 5120  with up to 12 drives<br>-Intel Xeon 6140  with up to 12 drives<br>-Intel Xeon E5-2620 v4 with GPU Support<br>-Intel Xeon E5-2650 v4 with GPU Support<br>-Intel Xeon E5-2690 v4 with GPU Support<br><br>  **Note**: If you select E5-2620 v4, E5-2650 v4, or E5-2650 v4, the Intel Optane drive replaces your GPU, so you cannot have both a GPU and an Intel Optane drive.|
|Operating system|For Intel-provided Optane drivers the following operating systems are certified by Intel:<br>Windows Server 2016 (all Editions)<br>Windows Server 2012 R2 (all Editions)<br><br>For In-box, open-source, non-Intel drivers, compatibility and functionality is validated but not certified:<br>Red Hat Enterprise Linux 7.x (64 bit)<br>Red Hat Enterprise Linux 6.x (64 bit).
|Image Add-ons| Select an Intel Optane drive for either or both the first and second PCIe Components.|
