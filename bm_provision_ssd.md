---

copyright:
  years: 2017, 2023
lastupdated: "2023-06-19"

keywords: Intel Optane, optane

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Provisioning an Intel Optane-compatible bare metal server
{: #bm-provision-optane-server}

You can provision a bare metal server with an Intel&reg; Optane drive.
{: shortdesc}

To provision a bare metal server with an Intel Optane drive, follow these steps:

1. Use the procedure: [Building a custom bare metal server](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server).
2. Select the following options on the order form:

| Field | Value |
|------|------|
| Region-Data Center | To use the Intel Optane drive, select from the available data centers.
| Server | Click **All servers** and select *Dual processors*. Then, select one of the following servers:  \n Intel Xeon 4110, up to 12 drives  \n Intel Xeon 5120 with up to 12 drives  \n Intel Xeon 6140 with up to 12 drives |
| Operating system | For Intel-provided Optane drivers the following operating systems are certified by Intel:  \n Windows Server 2016 (all Editions)  \n Windows Server 2012 R2 (all Editions).  \n For In-box, open source, non-Intel drivers, compatibility, and functionality is validated but not certified: RHEL 7.x (64 bit). |
| Image add-ons | Select an Intel Optane drive for either or both the first and second PCIe Components.|
{: caption="Provisioning an Intel Optane-compatible bare metal server" caption-side="top"}
