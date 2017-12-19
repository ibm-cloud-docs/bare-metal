---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# The primary drive on my bare metal server shows up as /dev/sdb. What is wrong?

This may be caused by the IPMI's Virtual Disk taking up the /dev/sda slot. This can be safely disabled by connecting to IPMIView and browsing to the Virtual Media tab. Select **Options > Disable** and click the **Apply** button to make the change. When the bare metal server is rebooted next, the primary drive will display /dev/sda.
