---
copyright:
  years: 2017, 22018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# RAID controller commands

You use the Adapatec Command Line Utility to run RAID controller commands.
The following are the most common RAID controller commands that you might use.
{:shortdesc}

<code><b>/usr/Adaptec_Event_Monitor/arcconf getstatus 1</b></code> <br>
_GETSTATUS_ lists the type of operation, logical drive number, logical
drive size, and progress of the operation. You can also see the status of any background commands that are running, such as the following items:
<ul>
  <li> Most recent rebuild
  <li> Synchronization
  <li> Logical-drive migration
  <li> Compaction/expansion
</ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getconfig 1<code></b>
_GETCONFIG_ lists information about controllers, logical drives, and physical drives. You can see information such as the following items:
<ul>
  <li> Controller type
  <li> BIOS, boot block, device driver, and firmware versions 
  <li> Physical device type, device ID, presence of PFA 
  <li> Physical device state 
  <li> Enclosure information: fan, power supply, and temperature
  </ul>

<code><b>/usr/Adaptec_Event_Monitor/arcconf getlogs 1 device tabular<code></b>
_GETLOGS_ gives you access to the status and event logs of a controller. _DEVICE xxx_ lists a log of any device errors that the controller encounters.

See the following example for output that is made by using the _GETLOGS_ command:
```
driveErrorEntry
smartError.. ............................ false 
vendorID ................................ WDC
serialNumber ............................ WD-XXX
wwn ..................................... xxxxxxxxxxxxxxxx - CC_FILTER
deviceID ................................ 10
productID ............................... WD1003FB
numParityErrors ......................... 0
linkFailures ............................ 0
hwErrors ................................ 0
abortedCmds ............................. 7
mediumErrors ............................ 20
smartWarning ............................ 0
```

## Common drive errors
