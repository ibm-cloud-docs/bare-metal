---
copyright:
  years: 2017, 2018
lastupdated: "2018-09-25"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# About RAID

RAID (Redundant Array of Independent Disks) creates a single usable data disk, where several physical disks are combined into an array for better speed and fault tolerance. Following are the three key concepts in RAID:
* **Mirroring**: copying data to more than one disk
* **Striping**: splitting data across more than one disk
* **Error correction** (fault tolerance): redundant data is stored to allow problems to be detected and possibly fixed.

Although many different levels of RAID exist, IBM chooses to support the most common raid types: 0, 1, 5, and 10. The different RAID levels use one or more of the following techniques, depending on the system requirements. The main purpose of using RAID is to improve reliability by using either 3Ware 9550SX Raid SATA or an Adaptec SA-SCSI RAID controller for all RAID solutions deployed.

RAID is not a backup solution. Rather, RAID creates a single usable data disk, where several physical disks are combined into an array for better speed and fault tolerance.


**RAID 0** (Striped set without parity/Non-Redundant Array) Implements data striping, where file blocks are written across multiple drives in fragments that requires a minimum of two disks. The advantage of a RAID 0 is that the read/write speed is dramatically increased. The more disks that are in the array, the greater the bandwidth. The disadvantage to a RAID 0 is that it has no fault tolerance. If a single drive fails, the array is broken. Also, RAID 0 does not implement error checking. So, any error is also unrecoverable. A common solution for fault tolerance is to have a drive outside of the array that is used as backup storage in a hardware failure.

**RAID 1** (Mirrored set without parity) Implements data mirroring. Data is duplicated on 2 or 4 drives through a hardware raid controller and provides some fault tolerance. The array is recoverable if at least one drive does not fail. It provides faster read performance than a single drive and provides drive redundancy if a drive failure occurs. Write speed is slightly reduced.

**RAID 5** (Striped set with dual distributed parity) Implements data striping at a block level and distributes parity among the drives. The parity information allows recovery from the failure of any single drive because any following reads can be calculated from the distributed parity. RAID 5 also allows for increased read/write speeds and allows the most efficient use of disk space. RAID 5 requires a minimum of three disks.

**RAID 10** (RAID 1 + 0) Creates multiple mirrors, where data is organized as stripes across multiple disks and then the striped disk sets are mirrored. RAID 10 offers the same fault tolerance as RAID 1 with increased read/write speeds over a single Raid 1 volume or single drive. RAID Level 10 requires four drives to implement.
