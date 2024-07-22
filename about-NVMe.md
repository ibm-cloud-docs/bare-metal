---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-22"

keywords: NVMe
subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# NVMe solid-state drives (SSD)
{: #ordering-nvme-ssd}

Non-Volatile Memory Express (NVMe) is a high-performance storage protocol that supports direct connection of the memory subsystem to the CPU through the PCIe interface. The NVMe protocol uses parallel, low latency data paths to the underlying media. This protocol offers significantly higher performance and less latency compared to traditional SAS and SATA protocols.
{: shortdesc}

NVMe SSDs use the same NAND flash as SATA SSDs but with a faster memory interface. NMVe U.2 SSDs are the same form factor as SATA SSDs (2.5”) and can be used in the same drive bays when hybrid drive bay connectivity is present in the server design.

## Considerations for NVMe SSDs
{: #NVMe_considerations}

Keep the following considerations in mind when you are selecting NVMe drives.

* You can't use an NVMe SSD as the boot disk for a server.
* NVMe SSDs must be selected as individual drives. You can't select an NVMe SSD from RAID storage groups.
* The number NVMe SSDs that you can provision depends on the server and PCI slots on the system board. You are limited to three NVMe SSDs.
* The GPUs share PCI slots with the NVMe SSDs. You can't configure more NVMe SSDs than GPUs.
* Because of compatibility issues, you can’t use NMVe drives with Windows&reg;.
* NVMe drives are installed in the last four slots of the chassis. {{site.data.keyword.cloud}} automation requires that you install the operating system on drives that are in drive bays 0 and 1 or M.2s. So, you can't install an operating system on an NVMe drive.

### Intel Optane SSDs
{: #optane-ssd}

Intel® Optane™ SSD DC P4800X is a solid-state drive that combines the attributes of storage and memory to create a new storage tier. The drives are available for a selection of {{site.data.keyword.cloud}} {{site.data.keyword.baremetal_long}}.
{: shortdesc}

Keep in mind that you can either [order](https://cloud.ibm.com/gen1/infrastructure/provision/bm){: external} an Intel® Optane™ SSD DC P4800X disk or a GPU for your server. You can't order both an Optane drive and GPU on the same server.
{: important}

## Ordering an NVMe SSD
{: #order-NVMe-ssd}

When you [provision](https://cloud.ibm.com/gen1/infrastructure/provision/bm){: external} a bare metal server, follow the [Building a custom Bare Metal Server](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server) steps and select the NVMe option in the **Storage disks** section.
