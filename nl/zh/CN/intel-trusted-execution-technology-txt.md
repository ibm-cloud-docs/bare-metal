---



copyright:
  years: 1994, 2017
lastupdated: "2017-11-24"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 硬件监视和安全性控制

随着恶意威胁的升级和日趋复杂，您应采用更严格的安全需求，并仔细检查执行环境的各个方面。您期待云供应商提供硬件监视和安全性控制，用于确定工作负载是否在已知位置的可信硬件上运行。{{site.data.keyword.cloud}} 在此方面始终走在前列，支持您在部署混合环境和云环境时，使用 Intel&reg; 可信执行技术 (Intel&reg; TXT) 增强启动环境的安全性验证。
{:shortdesc}

## 工作方式

Intel TXT 提供了硬件监视和安全性控制，可帮助向企业确保部署或迁移到 {{site.data.keyword.cloud_notm}} 基础架构的工作负载在已知位置的可信硬件上运行。{{site.data.keyword.cloud_notm}} 在一定范围的 {{site.data.keyword.baremetal_short}} 上提供 Intel TXT 支持。要获取完整列表，请参阅 http://www.softlayer.com/intel-txt。

Intel TXT 会分析并度量计算系统组件，从操作系统或系统管理程序一直到计算系统的引导固件和硬件。分析包括系统的基本输入/输出系统 (BIOS)、主引导记录 (MBR) 和引导装入程序。度量值会与标准基线进行比较，以确定系统是可信还是不可信。系统软件和本地或远程管理软件可以使用信任决策来允许或拒绝工作负载在计算系统上运行。由于 Intel TXT 是在引导过程中执行分析和度量，因此增强的安全性不会使应用程序增加任何性能开销。

基线度量值存储在可信平台模块 (TPM) 硬件设备上。TPM 设备集成在服务器系统中，并提供一系列与 Intel TXT 安全性相关的功能。

## 提供的功能

对于遵守合规性和审计法规的大型企业（例如，医疗保健机构、金融服务机构和政府机构），Intel TXT 尤其有利。它有助于确保对所有可信资源的跟踪可以在相关合规性组织（HIPAA、PCI、FedRAMP、ISO、FISMA 和 SSAE 16）中集成、管理和报告。这是这些机构头一次能够验证云计算系统是否得到相应保护，适合运行工作负载，例如：

* 治理和企业风险
* 信息和生命周期管理
* 合规性和审计
* 应用程序安全性
* 身份和访问权管理
* 事件响应

有关 {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} 上的 Intel TXT 的更多信息，请访问 http://www.softlayer.com/intel-txt。

以下链接提供了有关使用 [IBM、VMware 和 HyTrust 的可信安全云解决方案](http://wpc.c320.edgecastcdn.net/00C320/DeploymentGuide_IBM_Intel_HyTrust_VMware_v1%200.pdf)向工作负载添加额外安全性和合规性的更多信息。

**特别技术声明**：Intel 可信执行技术 (Intel TXT) 由 Intel&reg; 提供，并在需要特定技术知识来支持和管理的 {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}} 上运行。通过 {{site.data.keyword.cloud_notm}} 当前交付模型，我们能够启用或禁用 Intel TXT；但**由于客户环境和数据的敏感性，{{site.data.keyword.cloud_notm}} 无法帮助配置 Intel TXT 设置**。建议您为员工提供 Intel TXT 技术培训，或者与掌握成熟专业知识，能编排可信根和度量的启动环境 (MLE) 体系结构的咨询公司合作。
