---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} 中的 POWER8 - 常见问题

|1.|产品详细信息||
|---|---|---|
|1.1|产品是什么情形？|<ul><li>SoftLayer 扩展了其产品，现在包含基于 POWER8 的裸机系统。这些系统采用 IBM 全新的 POWER8 处理器和一个基于 OpenPOWER 的平台进行构建，该平台已专门针对在 Linux 上基于云部署数据、认知和 Web 工作负载而调整。</li><li>“虚拟机即服务”正在进行 beta 测试，预计在不久的将来提供。</li></ul>|
|1.2|什么是 OpenPOWER？为什么要关注 OpenPOWER？|<ul><li>基于 OpenPOWER 的服务器是一种功能强大且可定制的新一代开放式系统，基于 POWER8 体系结构而构建；唯一针对数据密集型工作负载从头设计的处理器。</li><li>OpenPOWER Foundation (OPF) 于 2013 年 8 月成立，一开始规模并不大，仅仅是拥有大胆构想的五家公司的联盟：通过使 POWER 硬件和软件可供开放式开发使用来支持新的技术和创新方法，并建立全行业联盟以在平台上拓展创新者生态系统。OPF 迅速发展壮大，现已拥有 190 多家企业参与。这种快速增长反映了整个行业迫切希望参与到“重新构想数据中心”的工作中。</li><li>OpenPOWER 平台将 POWER8 功能以及因 OpenPOWER 中的开放式协作而产生的创新供应到 SoftLayer 公共云。</li></ul>|
|1.3|SoftLayer 中的 POWER8 平台有哪些优势？|<ul><li>POWER8 提供了替代传统云平台的独特方法，其体系结构针对数据工作负载进行了优化。性能测试表明，POWER8 在处理数据工作负载方面的性能平均为可比 x86 系统的 2 倍。基准测试表明 SoftLayer 中的 POWER8 可交付以下内容：<ul><li>对于 Db2 with BLU，每小时查询数提高到 1.76 倍，每次查询的成本降低 20%。</li><li>云中 POWER8 上的 Db2 with BLU Acceleration 在相同时长内交付认知洞察的速度提高 43%，并且交付的洞察数多 65%。</li><li>对于数据分类和预测分析中使用的 Spark Machine Learning，性能提高 64%。</li><li>对于大数据集群中广泛使用的 Spark SQL 处理，速度快 66%。</li><li>基于 Spark 图形工作负载完成社交连接和产品推荐的速度快 83%。</li></ul></li></ul>|
|1.4|该产品的详细信息有哪些？|<ul><li>POWER8 系统的第一阶段可供按月租用，安装有 Ubuntu 操作系统，并包含 4 个固定配置的裸机部署：小型、中型、大型、大型（带 SSD）。</li><li>这些产品包含标准 SoftLayer API 支持以及大多数附属服务产品，如存储器、联网功能和防火墙。</li><li>POWER8 系统初始位于 DAL09 数据中心，将在 2016 年扩展到其他地区。</li></ul>|
|||![POWER8 C81](images/power8_fig1.png)<br /><br />![POWER8 图 2](images/power8_fig2.png)|
||||
|1.5|命名的含义是什么？|新的 POWER8 命名格式为 C812L，其中：<ul><li>“C”= 云</li><li>“8”= POWER8</li><li>“1”= 内核数</li><li>“2”= 2U</li><li>“L”= Linux</li></ul>|
|1.6|支持哪些操作系统？可以运行 AIX 或 IBM i 吗？|<ul><li>SoftLayer 初始将提供 Ubuntu Linux 14.04 LTS 操作系统，日后将添加其他 Linux 分发版。</li><li>这些系统无法运行 AIX 或 IBM i。“AIX 即服务”可通过 IBM Cloud Managed Services 获取，托管的 IBM i 可通过我们的许多全球业务合作伙伴提供。</li></ul>|
||可以租用使用 AIX 或 IBM i 操作系统的系统吗？|<ul<li>IBM 将继续通过 IBM Cloud Managed Services 和其他合作伙伴在云中提供 AIX。基于 IBM i 的云服务还可通过我们的许多 MSP 合作伙伴提供。</li></ul>|
|**2.**|**推向市场**||
|2.1|谁将从使用 POWER8 受益呢？|<ul><li>SoftLayer 中 POWER8 产品的初始套件非常适合希望针对混合云解决方案扩展其现有系统价值的现有 Power 客户。</li><li>这些系统已针对数据工作负载优化，可以轻松用于云中的开发/测试；快速 POC 可证明 Power 的性能优势，还可以<a href="https://www.ibm.com/developerworks/library/l-port-linux-on-x86-application/">轻松移植应用程序</a>到 Power 或 <a href="https://www-304.ibm.com/partnerworld/wps/servlet/ContentHandler/stg_com_sys_power-development-platform">Power Developer Cloud</a> 和 <a href="https://www-304.ibm.com/webapp/set2/sas/f/lopdiags/sdklop.html">SDK for Linux on Power</a>。</li><li>SoftLayer 云中的 POWER8 还可用于支持同时利用私有云和公共云资源的集成应用程序。</li><li>POWER8 裸机系统还可以作为新应用程序（例如，Genomics、财务或认知服务）的卓越托管平台。</li></ul>|
|2.2|最常见的用例有哪些？|<ul><li>在 Ubuntu 操作系统上运行的数据和分析密集型工作负载，例如 Db2 with BLU、Cognos 或 WebSphere。</li><li>开放式源代码应用程序（例如，Apache Spark 和 MariaDB）和支持 LAMP 的应用程序（例如，电子商务或内容管理系统）。</li><li>针对 Linux on Power 工作负载的开发/测试、移植和调整。</li><li>对竞争性 UNIX 工作负载和其他应用程序堆栈的概念证明。</li></ul>|
|2.3|对客户有哪些好处？|<ul><li>POWER8 是专门针对数据设计的唯一处理器，是 IBM Power Systems 系列服务器的核心。对于希望在云中运行要求苛刻的数据密集型工作负载和认知工作负载的企业而言，{{site.data.keywords_baremetal_short}} 是理想之选。</li><li>针对数据和分析工作负载，POWER8 在线程、内存带宽和速度方面均有所提升，交付的吞吐量和性能高于基于 x86 的可比系统。</li></ul>|
|2.4|如何订购 POWER8 {{site.data.keywords_baremetal_short}}？|<ul><li>“POWER8 裸机即服务”可像其他任何 SoftLayer 服务一样，通过“目录”提供和订购。</li><li>POWER8 裸机还可作为标准 IBM Cloud 产品提供，并可由 IBM 和 BP 销售商将其写入任何 IBM Cloud 合同中。</li></ul>|
|2.5|POWER8 系统如何定价？|<ul><li>根据所交付的性能，POWER8 裸机系统的价格与 x86 系统差不多。</li><li><strong>小型：</strong>8 核，64 GB RAM，1 个 1 TB SATA，10 Gbps，冗余电源。</li><li><strong>中型：</strong>10 核，256 GB RAM，2 个 4 TB SATA，10 Gbps，冗余电源。</li><li><strong>大型：</strong>10 核，512 GB RAM，2 个 6 TB SATA，10 Gbps，冗余电源。</li><li><strong>大型/SSD：</strong>10 核，256 GB RAM，2 个 960 SSD，10 Gbps，冗余电源。</li></ul>|
|**3.**|**在 SoftLayer 中实施 Power**|||
|3.1|可以将这些新的 POWER8 系统连接到 SoftLayer 中用于分层应用程序环境的相邻 x86 平台吗？|<ul><li>可以，这些系统可以配置用于同时需要 Power 和 x86 技术的分层应用程序环境中的其他相邻 SoftLayer 产品和应用程序。</li></ul>|
|3.2|可以供应不带操作系统的 POWER8 系统吗？|<ul><li>用于运行“无操作系统”的选项目前不可用。</li></ul>|
|3.3|可以安装自己的 Linux 操作系统（如 RHEL 或 SUSE）吗？|<ul><li>可以，但不支持也不会验证这些配置。客户应自行负责联系软件供应商来处理许可管理、补丁、特许使用权费和维护等事宜。SoftLayer 将继续支持硬件，在发生硬件问题的情况下，可能会要求客户提供访问权来获取与硬件故障相关的系统日志和错误消息。</li></ul>|
|3.4|POWER8 上的虚拟机 (VMaaS) 体系结构何时可用？|<ul><li>POWER8 上的“VM 即服务”将在 2016 年一般可用。</li></ul>|
|3.5|哪些自动化和供应工具可用于 POWER8？|<ul><li>Canonical 的 JuJu Charms 可以自动部署到 Ubuntu 操作系统。它们拥有许多预建软件包，可用于在 Ubuntu 上自动部署许多 IBM 和开放式源代码软件包。JuJu Charms 在 Canonical 的 <a href="https://jujucharms.com/store">JuJu Charm 商店</a>中提供。</li></ul>|
|3.6|专为快速供应而设计的这些系统可以升级吗？未来将提供可配置的裸机吗？|<ul><li>SoftLayer 将在未来添加配置选项、附加组件服务、操作系统选项和每小时定价。</li></ul>|
|**4.**|**未来方向和更多信息**||
|4.1|这些新的 POWER8 系统将提供哪些额外的数据中心基础架构和服务？|<ul><li>SoftLayer 为 POWER8 系统提供的数据中心选项与目前为 x86 提供的相同，只有几点例外（eVault 和基于软件的防火墙）。</li><li>SoftLayer 将继续逐渐扩展 POWER8 配置和产品，包括更多配置和存储选项、操作系统、扩展到其他数据中心、GPU 和其他产品，以增强产品的选择和功能。</li></ul>|
