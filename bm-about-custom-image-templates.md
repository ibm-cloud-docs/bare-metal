---

copyright:
  years: 2020, 2022
lastupdated: "2021-12-02"

keywords: custom image template, image template

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

Image templates provide an imaging option for {{site.data.keyword.baremetal_long}}. With {{site.data.keyword.baremetal_short}} custom image templates, you can capture an image of a bare metal server to replicate its configuration with minimal changes in the order process. 
{: shortdesc}

Image templates are not intended for backing up your data.
{: important}

## How bare metal custom image templates work
{: #how-bm-custom-image-templates-work}

The two main actions for any image template are _create_ and _deploy_. When you request to create an image, a compressed backup of your data is created. The configuration information is recorded and the image template is stored on the {{site.data.keyword.cloud_notm}}. During the deployment stage of the image template, the automated system constructs a new server that is based on the data that is gathered from the selected image. The deployment process makes adjustments for volume, restores the copied data, and then makes final configuration changes (for example, network configurations) for the new host.

Make sure that your image works fine during deployment before you reclaim the source server.
{: tip}

### Compatible system configurations
{: #bm-image-template-compatible-system-configurations}

The following features and configurations are supported when you create an image template. 

- Full traditional BIOS boot mode support and limited UEFI boot mode support (images must be deployed on their respective servers)
- Only available for X10, X11, and Lenovo systems
- Supports multiple drives up to 2 TB 
- vGPU support
- RAID 0, 1, 10 
  
### Supported operating systems
{: #bm-image-template-supported-os}

The following operating systems are supported when you create an image template. 

- CentOS 7, 8
- RHEL 7, 8
- Ubuntu 16, 18
- Windows 2012 R2, 2016, 2019

### Supported add-ons
{: #bm-image-template-supported-addons}

The following add-ons are compatible with image templates. 

- McAfee (free license add-on) 
- MySQL (free license add-on) 
- Microsoft SQL Server 
- R1Soft client 

If your bare metal server has add-on software such as cPanel, MS SQL Server, Plesk, or R1Soft Backup Agent, you need to follow the vendor migration guidelines instead of capturing and deploying a custom image. For more information, see [Migrating bare metal servers with add-on software](/docs/bare-metal?topic=bare-metal-bm-migrate-with-add-on-software).
{: note}

#### Notes for add-ons
{: #bm-image-template-addon-notes}

Keep the following notes in mind when you capture an image and deploy a server from an image.

- When a MySQL server is deployed from an image, the administrator user keeps the same password as the original server when the image was captured.
- If an R1soft client is installed and you capture and deploy an image and deploy a new server from that image, you need to reinstall, configure, and add the client again to the R1soft server because the new server has a different IP address.

### Limitations
{: #bm-custom-image-limitations}

Customs images have some limitations that you need to be aware of before you create an image template. 

- No multiple RAID configurations
- No RAID 5 and 6
- No Trusted Platform Module (TPM) encryption support
- Logical Volume Management (LVM) not supported
- Custom and non-IBM kernels not supported
- CentOS with UEFI not supported 
- Control panels (for example cPanel and Plesk) are not supported 
- R1Soft Backup Agent isn't supported for image capture

Any software (for example MySQL) that maintains its own internal password files and database stays unmodified on provision. Access to the software on a provisioned server from the image uses the same username and passwords as the source server that the image was created from.
{: important}

## Next steps
{: #next-steps-bm-custom-image}

* If you're ready to create an image template, see [Creating a custom bare metal server image template](/docs/bare-metal?topic=bare-metal-bm-create-custom-image-template).
* If you want to order and deploy a bare metal server from a custom image, see [Ordering a bare metal server from an image template](/docs/bare-metal?topic=bare-metal-ordering-bm-from-image-template).
* If you want to delete an image template, see [Deleting a custom image](/docs/bare-metal?topic=bare-metal-delete-bm-custom-image).
* If you want to import a custom image, see [Importing a custom image](/docs/bare-metal?topic=bare-metal-import-bm-custom-image).
* If you want to migrate a bare metal server with add-on software, see [Migrating bare metal servers with add-on software](/docs/bare-metal?topic=bare-metal-bm-migrate-bare-metal-add-on-software).
