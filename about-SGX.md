---


copyright:
  years: 2019, 2024
lastupdated: "2024-06-17"

keywords: intel sgx, sgx, Intel Software Guard Extension

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Confidential computing with Intel® Software Guard Extensions (SGX)
{: #bm-intel-sgx}

Confidential computing with Intel® Software Guard Extensions (SGX) protects your data through hardware-based server security by using isolated memory regions that are known as encrypted enclaves. This hardware-based computation helps protect your data from disclosure or modification. Which means that your sensitive data is encrypted while it is in virtual server instance memory by allowing applications to run in private memory space. To use SGX, you must install the SGX drivers and platform software on SGX-capable worker nodes. Then, design your app to run in an SGX environment. For more information about confidential computing and {{site.data.keyword.cloud}}, see [Getting started with confidential computing](/docs/confidential-computing?topic=confidential-computing-about).
{: shortdesc}

## Confidential computing with SGX
{: #confidential-computing-sgx-classic-bm}

When you use confidential computing with SGX, your data is protected through the entire compute lifecycle. Which means that your data is accessible only to authorized code and is invisible to anyone or anything else, including the operating system and even {{site.data.keyword.cloud}}.

### SGX is a trusted execution environment (TEE)
{: #tee-sgx-classic-bm}

SGX uses a trusted execution environment (TEE). TEE is a secure area of the main processor that provides a higher level of data security for trusted data and applications.

A TEE sets up an isolated, secure area of the main processor on a device that is dedicated to processing and storing sensitive data. The secure environment is protected from unauthorized access - even if the operating system is compromised. While your sensitive data is inside an encrypted enclave, your data is split into trusted and untrusted parts. The trusted parts are used in the encrypted enclave while the CPU denies all other access to the enclave regardless of access privileges. The data is inaccessible to internal and external threats and can't be removed or modified.

So, all Intel SGXs are TEEs, but not all TEEs are Intel SGXs.

### Attestation
{: #attestation-sgx-classic-bm}

When you develop a confidential computing application, you must design it so you can segment the information that needs encryption. At run time, the segmented information is kept confidential through attestation. When a request for information from the segmented code or app data is received, the encrypted enclave verifies that the request comes from the part of the application that exists outside of the enclave within the same application before it shares any information. Through the attestation process, information is kept confidential and data leakage is prevented.

### Confidential computing with SGX use cases
{: #scenarios-sgx-classic-bm}

The following are some of the use cases for confidential computing with SGX.

* **Confidentiality and Privacy of Workloads and Applications** within a confidential computing environment make sure that data privacy and security applications are always protected.

* **Confidential AI and Analytics** enable data and business analytics applications, machine learning models, and applications within secure enclaves, which include SMPC applications that also help gain data insights.

* **Secure Multi-party Compute** enables distributed SMPC that helps make sure that participant data and insights are protected even when calculated outside their direct control.

* **Digital Assets** is the trusted platform for digital custody solutions, for storing and transferring high-value digital assets in highly secure wallets, reliable at scale.

## Limitations
{: #limitations-confidential-computing-sgx-classic-bm}

Keep the following limitations in mind if you want to use SGX.

* SGX doesn't protect against side-channel attacks.
* Available on only third-generation Sapphire Rapids-based servers.
* Only the following operating systems support SGX. Keep in mind that operating systems with kernel versions 5.11 and prior don't support SGX.
   - Red Hat 8.6, 8.8, 9.0, 9.2
   - Ubuntu 20.04, 22.04
   - CentOS Stream 8, 9
   - Rocky Linux 8.8, 9.2
   - SLES 15 SP4, SP5

## Next steps
{: #intel-sgx-next-steps-classic-bm}

To provision a bare metal server with Intel SGX, see [Provisioning a bare metal server with Intel SGX](/docs/bare-metal?topic=bare-metal-bm-server-provision-sgx#bm-server-provision-sgx).
