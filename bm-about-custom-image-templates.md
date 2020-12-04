---

copyright:
  years: 2020
lastupdated: "2020-11-11"

keywords: custom image template, bare metal image, image template

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:important: .important}
{:tip: .tip}
{:note: .note}
{:beta: .beta}

# About bare metal custom image templates
{: #getting-started-bm-custom-image-templates}

With {{site.data.keyword.baremetal_long}} custom image templates, you can capture an image of a bare metal server to replicate its configuration with minimal changes in the order process. Image templates provide an imaging option for all {{site.data.keyword.baremetal_short}}, regardless of operating system. 
{:shortdesc}

Image templates are not intended for backing up your data.
{: important}

## How bare metal custom image template work
{: #how-bm-custom-image-templates-work}

The two main actions for any image template are _create_ and _deploy_. When you request to create an image a compressed backup of your data is created. The configuration information is recorded and the image template is stored on the {{site.data.keyword.cloud_notm}}. During the deployment stage of the image template, the automated system constructs a new server that is based on the data that is gathered from the selected image. The deployment process makes adjustments for volume, restores the copied data, and then makes final configuration changes (for example, network configurations) for the new host.

## Prerequisites 
{: #bm-custom-image-prereqs}

* Compatible system configurations 
  - UEFI and BIOS server images must be deployed on respective servers
  - Only available for X10, X11, and Lenovo systems
  - Supports single drives up to 2 TB drives
  - vGPU support
  - RAID 0, 1, 10 
  
* Supported OSs
  - CentOS 6.10 and 7.6 <!--8-->
  <!--- Debian 9-->
  <!--- RHEL 6.10, 7.6, 8-->
  - Ubuntu 16.04 and 18.04
  <!--- Windows 2012 r2, 2016, 2019-->

## Limitations
{: #bm-custom-image-limitations}

  - No multiple RAID configurations
  - No multiple drive capture
  - No RAID 5 and 6
  - UEFI boot mode not supported
    - No TPM support
    - No LVM support
  - Custom and non-IBM kernels not supported

## Next steps
{: #next-steps-bm-custom-image}

* If you're ready to create an image template, see [Creating a custom bare metal server image template](/docs/bare-metal?topic=bare-metal-bm-create-custom-image-template).
* If you want to order and deploy a bare metal server from a custom image, see [Ordering a bare metal server from an image template](/docs/bare-metal?topic=bare-metal-ordering-bm-from-image-template).
* If you want to delete an image template, see [Deleting a custom image](/docs/bare-metal?topic=bare-metal-delete-bm-custom-image).
* If you want to import a custom image, see [Importing a custom image](/docs/bare-metal?topic=bare-metal-import-bm-custom-image).
