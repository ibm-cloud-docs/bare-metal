---

copyright:
  years: 2017, 2019
lastupdated: "2018-04-02"

keywords: provision Intel Optane compatible bare metal server, Intel Optane, optane 

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 供应与 Intel Optane 兼容的裸机服务器
{: #bm-provision-optane-server}

要供应采用 Intel Optane 驱动器的裸机服务器，请执行以下操作：
1. 使用以下过程：[构建定制裸机服务器](/docs/infrastructure/bare-metal?topic=bare-metal-ordering-baremetal-server)。
* 在订购表单上选择以下选项：

|部分|要选择的选项
|------|------|
|区域-数据中心|要使用 Intel Optane 驱动器，请选择以下其中一个数据中心：<br>欧洲 - AMS03、FRA02、LON02、OSL01<br>北美南部 - DAL09、DAL10、DAL12<br>亚太地区 - MEL01<br>北美东部 - MON01、TOR01、WDC04<br>北美西部 - SJC03<br>|
|服务器|1. 选择**所有服务器**<br>2. 选择*双处理器*<br>3. 选择下列其中一个服务器<br>-Intel Xeon 4110，最多 12 个驱动器<br>-Intel Xeon 5120，最多 12 个驱动器<br>-Intel Xeon 6140，最多 12 个驱动器<br>-Intel Xeon E5-2620 v4，支持 GPU <br>-Intel Xeon E5-2650 v4，支持 GPU <br>-Intel Xeon E5-2690 v4，支持 GPU<br><br>  **注**：如果选择 E5-2620 V4、E5-2650 V4 或 E5-2650 V4，那么 Intel Optane 驱动器将替换 GPU，因此不能同时拥有 GPU 和 Intel Optane 驱动器。|
|操作系统|对于 Intel 提供的 Optane 驱动器，以下操作系统已通过 Intel 认证：<br>Windows Server 2016（所有 Edition）<br>Windows Server 2012 R2（所有 Edition）<br><br>对于随附的开放式源代码非 Intel 驱动器，兼容性和功能已验证，但未经认证：<br>Red Hat Enterprise Linux 7.x（64 位）<br>Red Hat Enterprise Linux 6.x（64 位）。
|映像附加组件|为第一个和/或第二个 PCIe 组件选择 Intel Optane 驱动器。|
