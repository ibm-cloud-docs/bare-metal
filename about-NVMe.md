---

copyright:
  years: 2017, 2022
lastupdated: "2022-11-17"

keywords: NVMe
subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}


# NVMe solid-state drives (SSD)
{: #ordering-nvme-ssd}

Non-Volatile Memory Express (NVMe) is a high-performance storage protocol that supports direct connection of the memory subsystem to the CPU through the PCIe interface. The NVMe protocol capitalizes on parallel, low latency data paths to the underlying media. This protocol offers significantly higher performance and less latency compared to traditional SAS and SATA protocols.
{: shortdesc}

NVMe SSDs use the same NAND flash as SATA SSDs but with a faster memory interface. NMVe U.2 SSDs are the same form factor as SATA SSDs (2.5”) and can be used in the same drive bays when hybrid drive bay connectivity is present in the server design.

Check out this [blog post](https://www.ibm.com/cloud/blog/benefits-of-running-high-io-applications-on-ibm-cloud-bare-metal-servers-with-nvme-storage) to see the benefits of running high IO applications with NVMe storage.
{: tip}

## Considerations for NVMe SSDs
{: #NVMe_considerations}

* You can't select an NVMe SSD as the boot disk for a server.

* NVMe SSDs must be selected as individual drives. You cannot select an NVMe SSD from RAID storage groups.

* The number NVMe SSDs that you can provision depends on the server and PCI slots on the system board. Currently, you are limited to three.

* The GPUs share PCI slots with the NVMe SSDs. You can't configure more NVMe SSDs than GPUs. This limit is also dependent on the server's system board.

* Because of compatibility issues, you can’t select NMVe drives if you’re going to install Windows&reg;.

* NVMe drives are installed in the last four slots of the chassis. {{site.data.keyword.cloud}} automation requires that you install the operating system on drives that are in drive bays 0 and 1 or M.2s. So, you can't install an operating system on an NVMe drive.

## Order an NVMe SSD
{: #order-NVMe-ssd}

When you [provision](https://cloud.ibm.com/gen1/infrastructure/provision/bm){: external} a bare metal server, follow the [Building a custom Bare Metal Server](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server) steps and select the NVMe option in the **Storage disks** section.
