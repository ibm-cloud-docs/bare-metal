---

copyright:
  years: 2018, 2023
lastupdated: "2023-12-12"

keywords: bare metal, getting started, {{site.data.keyword.cloud}}, {{site.data.keyword.cloud_notm}}

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Getting started tutorial
{: #getting-started}

IBM Cloud Bare Metal Servers are single-tenant, dedicated physical servers that can be deployed and managed as cloud services with various billing options, including hourly and monthly. You can deploy a bare metal on IBM Cloud Classic infrastructure (see the following table) or [IBM Cloud VPC infrastructure](/docs/vpc?topic=vpc-about-bare-metal-servers).
{: shortdesc}

Table 1 contains steps to help you quickly get your {{site.data.keyword.baremetal_short}} provisioned and configured.

| Task | Details |
|------|------|
| **1.** Review content that can help with your implementation | New to IBM Cloud and bare metal servers? The following sites provide useful information to help you plan your environment.  \n - [What is IBM Cloud](https://www.ibm.com/cloud){: external}  \n - [Getting started with IBM Cloud](https://ibm.com/cloud/get-started){: external}  \n - [Bare Metal Servers](https://www.ibm.com/cloud/bare-metal-servers){: external}  \n - [Network options](/docs/bare-metal?topic=bare-metal-network-options) |
| **2.** Sign up for IBM Cloud | [Signing up for IBM Cloud](/docs/account?topic=account-signup#signing-up-for-ibm-cloud) has the steps on how to set up your IBM Cloud account. |
| **3.** Determine your workload specifications | Before your provision your server, determine how you want to use it and the server size you need to be successful. For example, do you intend to use it for development and testing, or production? Are you testing a user experience, processing lengthy algorithms, backing up and restoring data, or increasing latency speed? |
| **4.** Size and cost out your server | You can use the [bare metal search tool](https://cloud.ibm.com/gen1/infrastructure/provision/bm){: external} to help you size and cost out your server. |
| **5.** Log in to your IBM Cloud account | You can access the Bare Metal Server Order Form from the IBM Cloud catalog or the IBM Cloud console. You need an [IBMid and password](/docs/account?topic=account-account-getting-started#getting-started) to access the IBM Cloud catalog and console.  \n - [IBM Cloud catalog](https://cloud.ibm.com/catalog){: external}  \n - [IBM Cloud console](https://cloud.ibm.com/){: external}
| **6.** Provision your server | You have three options when it comes to provisioning your server: fast provisioning, custom, and SAP-certified. Fast provisioning servers are pre-configured servers that meet the needs of most customers and can be ready to configure 30 - 40 minutes after provisioning.  \n  \n Custom servers are servers that you create by selecting specific compute, connectivity, storage, and network options to meet your needs. Custom servers take longer to provision, usually 2 - 4 hours, and have higher operating costs. You can [Provision an Intel&reg; Optane-compatible bare metal server](/docs/bare-metal?topic=bare-metal-bm-provision-optane-server) or one with an [Intel&reg; SGX architecture](/docs/bare-metal?topic=bare-metal-bm-server-provision-sgx). SAP-certified servers are certified to support SAP HANA and SAP NetWeaver landscapes.  \n  \n Use the following links for provisioning information for that type of server. With SAP-certified servers, you need to select which type of landscape, SAP HANA, or SAP NetWeaver, you are provisioning.  \n - [Fast-provisioned bare metal servers](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers)  \n - [Custom bare metal servers](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server)  \n - [IBM Cloud SAP-Certified Infrastructure](/docs/bare-metal?topic=bare-metal-sap-cert-infrastructure) |
| **7.** Configure your bare metal server | Your server is now ready to be configured. See the topics under **Configuring**. |
{: caption="Table 1. Quick start steps" caption-side="top"}
