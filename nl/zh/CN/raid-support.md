---

copyright:
  years: 1994, 2019
lastupdated: "2018-5-31"

keywords: raid support, raid help

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# RAID 支持凭单信息
{:# bm-raid-support-ticket}

如果在裸机服务器上使用 RAID 时遇到问题或有疑问，您可以在 [IBM developerWorks dW Answers](https://developer.ibm.com/answers/topics/ibm-cloud/){:new_window} 论坛中查找答案。还可以提交支持凭单。有关支持凭单的信息，请参阅[开具支持凭单](https://test.cloud.ibm.com/docs/get-support?topic=get-support-getting-customer-support#open-ticket){:new_window}。
{:shortdesc}

<!--During a drive or RAID failure, support tickets are automatically created. You can create a support ticket for other problems.--> 创建支持凭单时，需要提供 RAID 日志文件。RAID 日志文件中的信息对于恢复丢失的 RAID 配置至关重要。提供您的日志文件可帮助支持团队识别驱动器订单、阵列成员资格、阵列几何以及连线问题。根据您使用的 RAID 控制器类型（Adaptec 或 LSI），使用以下命令来获取 RAID 日志文件。

**注：**授予在初始更新中重新启动/关闭电源的许可权或者要求驱动器进行热交换，可加快支持凭单过程的处理速度。

<b>Adaptec RAID 卡</b><br>
使用以下命令来获取 Adaptec RAID 卡的日志文件。确保在支持凭单中包含此日志文件的完整输出。

`arcconf getconfig 1/arcconf getlogs 1 device tabular`。

<b>LSI RAID 卡</b><br>
使用以下命令获取 LSI RAID 卡的日志文件。您需要在支持凭单中包含这些日志文件的完整输出。
```/opt/MegaRAID/storcli/storcli64 /c0 show all
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
/opt/MegaRAID/storcli/storcli64 /c0 /eall /sall show all | grep -iE "det|cou|tem|SN|S.M|fir"
/opt/MegaRAID/storcli/storcli64 /c0 show TermLog
```
**重要信息：**请确保在开始故障诊断之前备份任何工作。
