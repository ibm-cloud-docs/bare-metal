---

copyright:
  years: 2018, 2024
lastupdated: "2024-07-22"

keywords: provision, sgx, provision server Intel SGX architecture, Intel SGX architecture, confidential computing,

subcollection: bare-metal

---


{{site.data.keyword.attribute-definition-list}}

# Provisioning a bare metal server with Intel&reg; Software Guard Extension architecture
{: #bm-server-provision-sgx}

Intel Software Guard Extensions (SGX) can protect data that uses hardware-based server security. With Intel SGX applications, you can protect select code and data from disclosure or modification. By using trusted execution environments (TEE), known as enclaves, you can encrypt the pieces of your application memory that contains sensitive data while it is in use.
{: shortdesc}

## Provisioning your bare metal server with SGX
{: #provision-sgx}

To provision a bare metal server with SGX, use the following steps:

1. Create a custom server by following the procedure [Build a custom bare metal server](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server)
2. On the [bare metal provisioning page](https://cloud.ibm.com/gen1/infrastructure/provision/bm), select the following options.

| Field | Value |
|------|------|
| Server | Select either Intel Sapphire Rapids processor or Intel Xeon&reg; 2174. |
| Image | Select an available image. For more information about Classic-supported operating systems, see [Lifecycle for operating systems and add-ons](/docs/bare-metal?topic=bare-metal-product-lifecycle-classic).|
| Image Add-ons | Select Software Guard Extensions (SGX). |
{: caption="Table 1. SGX order form options" caption-side="top"}

## Installing Intel SGX platform software and drivers
{: #install-intel}

Make sure that you install the SGX platform software and drivers.

1. Go to the [Get started](https://www.intel.com/content/www/us/en/developer/tools/software-guard-extensions/get-started.html{: external} and select the option for installation that matches your operating system.
2. Download the binary installation option. This option helps make sure that you use a stable version of SGX in your workloads.
3. For specific instructions for each type of installation, see the [Intel SGX Installation Guide for Windows](https://downloadcenter.intel.com/product/80895/Intel-Software-Guard-Extensions-Intel-SGX-for-Windows-){: external} or the [Intel SGX Installation Guide for Linux](https://download.01.org/intel-sgx/linux-2.1.2/docs/Intel_SGX_Installation_Guide_Linux_2.1.2_Open_Source.pdf){: external}.
