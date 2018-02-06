---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-27"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 为什么 CPU 速度不正确？

您登录到服务器来检查 CPU 信息，并注意到处理器速度不正确。导致这种差异的原因可能是增强型 Intel SpeedStep 技术 (EIST)。EIST 是 Intel 对动态频率调整技术的叫法。这种技术在较旧系统中也称为 *CPU 调速*或*总线压摆*。在某些 AMD 系统上，也存在类似技术，但称为 *Cool'N'Quiet* 或 *PowerNow!*。虽然这些技术并不完全一样，但目标一致，都是要在处理器工作量不大时，通过降低 CPU 速度来减少功耗和产热量。在服务器恢复大工作量时，可根据需要提高时钟速度。

如果您希望了解服务器上的 Intel 处理器是否支持 SpeedStep，请登录客户门户网站： 
1. 单击**设备**。
* 在列表中识别您的服务器。
* 单击服务器名称以查看**设备详细信息**。
* 找到标题为**硬件**的子部分，以找到服务器处理器 CPU 速度对应的型号。
* 有了服务器处理器型号后，转至 [Intel Processor Finder](http://processorfinder.intel.com/)，使用此型号来查找有关处理器的更多信息，并了解此型号是否支持增强型 Intel SpeedStep 技术。

EIST 是一种完善的技术。您没有理由禁用 EIST。不过，如果您决定不想使用此功能，请向支持团队开具凭单以请求禁用此功能。要禁用此功能，需要重新引导服务器。
