---

copyright:
  years: 2017, 2020
lastupdated: "2020-05-18"

keywords: NVMe, bare metal, SSD, U.2

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# NVMe solid-state drives
{: #ordering-nvme-ssd}

Non-Volatile Memory Express (NVMe) is a high-performance storage protocol that supports direct connection of the memory subsystem to the CPU via the PCIe interface. The NVMe protocol capitalizes on parallel, low latency data paths to the underlying media. This protocol offers significantly higher performance and lower latencies compared to legacy SAS and SATA protocols.

NVMe SSDs use the same NAND flash as SATA SSDs but with a faster memory interface. NMVe U.2 SSDs are the same form factor as SATA SSDs (2.5”) and can be use in the same server drive bays when hybrid drive bay connectivity is present in the server design.

## Considerations for NVMe SSD drives
{: #NVMe_considerations}

You cannot select an NVMe SSD drive as the boot disk for a server.

NVMe SSD drives must be selected as individual drives. You cannot select NVMe SSD drives from RAID storage groups.

No limitations exist on the number of NVMe SSDs you can provision. The number depends on the server and PCI slots on the system board. Currently, you are limited to 3.

The GPUs share PCI slots with the NVMe SSDs. You cannot configure more NVMe SSDs than GPUs. This limit is also dependent on the server's system board.
