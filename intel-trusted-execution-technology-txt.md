---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-31"

keywords: bare metal, intel txt

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Hardware monitoring and security controls
{: #bm-hardware-monitroing-security-controls}

The escalation and sophistication of malicious threats has you employing more stringent security requirements and scrutinizing every aspect of your execution environment. You're looking to your cloud providers to offer hardware monitoring and security controls that can determine whether a workload is running on trusted hardware in a known location. {{site.data.keyword.cloud}} is leading the way by enabling you to deploy hybrid and cloud environments with enhanced security verification of your launch environment by using Intel&reg; Trusted Execution Technology (Intel&reg; TXT). {: shortdesc}

## How it works

Intel TXT provides hardware monitoring and security controls that help assure businesses that a workload that is deployed on or migrated to the {{site.data.keyword.cloud_notm}} infrastructure is running on trusted hardware in a known location. {{site.data.keyword.cloud_notm}} supports Intel TXT on a range of {{site.data.keyword.baremetal_short}}. See [Intel Trusted Execution Technology](https://www.ibm.com/cloud/bare-metal-servers/intel-txt) for a complete list.

Intel TXT analyzes and measures the components of a computing system from the operating system or hypervisor to the computing system’s boot firmware and hardware. The analysis includes the system’s basic input/output system (BIOS), master boot record (MBR), and boot loader. The measurements are compared to a standard baseline to determine if the system is trusted or untrusted. System software and local or remote management software can use the trust decision to permit or deny a workload from running on that a computing system. Since Intel TXT performs the analysis and measuring during boot up, the added security doesn’t add any performance overhead to applications.

The baseline measurements are stored on a Trusted Platform Module (TPM) hardware device. The TPM device is integrated within the server system and provides a range of Intel TXT security-related functions.

## What it does for you

Intel TXT is especially advantageous for large enterprises subject to compliance and audit regulations, such as healthcare, financial services, and government organizations. It helps assure that tracking of all trusted resources can be integrated, managed, and reported on with the relevant compliance organizations (HIPAA, PCI, FedRAMP, ISO, FISMA, and SSAE 16). For the first time, these organizations are able to certify that a cloud computing system is appropriately secured for workloads such as

* Governance and enterprise risk
* Information and life-cycle management
* Compliance and audit
* Application security
* Identity and access management
* Incident response

For more information about Intel TXT on {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}, see [Intel Trusted Execution Technology](https://www.ibm.com/cloud/bare-metal-servers/intel-txt).

The following link has more information about adding more security and compliance to your workloads with a [trusted secure cloud solution with IBM, VMware, and HyTrust](http://wpc.c320.edgecastcdn.net/00C320/DeploymentGuide_IBM_Intel_HyTrust_VMware_v1%200.pdf).

**Special Technical Notice** Intel Trusted Execution Technology (Intel TXT) is provided by Intel&reg; and operates on the {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} that require specific technical knowledge to support and manage. The {{site.data.keyword.cloud_notm}} current delivery model can turn Intel TXT either on or off; **{{site.data.keyword.cloud_notm}} cannot assist with configuration of Intel TXT settings due to the sensitivity of customer environments and data**. It is recommended that you either include staff who are trained in Intel TXT technologies or engage with a consulting firm with proven expertise in orchestrating root of trust and measured launch environment (MLE) architecture.
