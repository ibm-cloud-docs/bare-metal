---

copyright:
  years: 2017, 2022
lastupdated: "2022-04-13"

keywords: 

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

The escalation and sophistication of malicious threats has you employing more stringent security requirements and scrutinizing every aspect of your execution environment. You're looking to your cloud providers to offer hardware monitoring and security controls that can determine whether a workload is running on trusted hardware in a known location. {{site.data.keyword.cloud}} is leading the way to help you deploy hybrid and cloud environments with enhanced security verification of your launch environment by using Intel&reg; Trusted Execution Technology (Intel TXT). 
{: shortdesc}

## How Intel TXT works
{: #bm-how-txt-works}

Intel TXT provides hardware monitoring and security controls that help assure businesses that a workload that is deployed on or migrated to the {{site.data.keyword.cloud_notm}} infrastructure is running on trusted hardware in a known location. {{site.data.keyword.cloud_notm}} supports Intel TXT on a range of {{site.data.keyword.baremetal_short}}. See [Intel&reg; Trusted Execution Technology](https://www.ibm.com/cloud/bare-metal-servers/intel-txt) for a complete list.

Intel TXT analyzes and measures the components of a computing system from the operating system or hypervisor to the computing system’s boot firmware and hardware. The analysis includes the system’s basic input/output system (BIOS), master boot record (MBR), and boot loader. The measurements are compared to a standard baseline to determine whether the system is trusted or untrusted. System software and local or remote management software can use the trust decision to allow or deny a workload from running on that a computing system. Since Intel&reg; TXT performs the analysis and measuring during boot up, the added security doesn’t add any increased processor usage to applications.

The baseline measurements are stored on a Trusted Platform Module (TPM) hardware device. The TPM device is integrated within the server system and provides a range of Intel TXT security-related functions.

## What does Intel TXT does for you
{: #bm-what-txt-does-for-you}

Intel TXT is especially advantageous for large enterprises subject to compliance and audit regulations, such as healthcare, financial services, and government organizations. It helps assure that tracking of all trusted resources can be integrated, managed, and reported on with the relevant compliance organizations (HIPAA, PCI, FedRAMP, ISO, FISMA, and SSAE 16). For the first time, these organizations are able to certify that a cloud computing system is secured for workloads such as

* Governance and enterprise risk
* Information and lifecycle management
* Compliance and audit
* Application security
* Identity and access management
* Incident response

For more information about Intel TXT on {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}, see [Intel&reg; Trusted Execution Technology](https://www.ibm.com/cloud/bare-metal-servers/intel-txt).

## Special technical notice
{: #bm-special-txt-technical-notice}

Intel TXT is provided by Intel&reg; and operates on the {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} that require specific technical knowledge to support and manage. The {{site.data.keyword.cloud_notm}} current delivery model can turn Intel&reg; TXT either on or off. {{site.data.keyword.cloud_notm}} can't assist with configuration of Intel TXT settings because of the sensitivity of customer environments and data. The recommendation is that you either include staff who is trained in Intel TXT technologies or engage with a consulting firm with expertise in orchestrating root of trust and measured launch environment (MLE) architecture.
