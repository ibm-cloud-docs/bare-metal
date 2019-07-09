---

copyright:
  years: 2016, 2019
lastupdated: "2018-11-06"

keywords: activity tracker, bare metal, {{site.data.keyword.Bluemix}}

subcollection: bare-metal

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Activity Tracker 事件
{: #bm-at-events}

作为安全主管、审计员或管理员，您可以使用 {{site.data.keyword.cloudaccesstrailfull}} 服务跟踪用户和应用程序如何与 {{site.data.keyword.Bluemix}} 中的裸机服务器进行交互。帐户所有者和与帐户链接的用户可以触发在 {{site.data.keyword.cloudaccesstrailshort}} 中记录的裸机服务器事件。
{:shortdesc}

{{site.data.keyword.cloudaccesstrailshort}} 服务会记录用户发起的用于在 {{site.data.keyword.Bluemix_notm}} 中更改服务状态的活动。有关更多信息，请参阅[关于 {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov )。

要开始监视用户的操作，请参阅 [IBM Cloud Activity Tracker 使用入门](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started#getting-started)。

发起方可以是用户、服务或应用程序。
要使用户能够生成事件，该用户必须具有 {{site.data.keyword.Bluemix}} 控制台中**基础架构**资源的访问权。
{: tip}

## 裸机服务器实例事件
{: #bare-metal-events}

您可以使用 {{site.data.keyword.cloudaccesstrailshort}} 服务通过其生命周期来审计裸机服务器。

下表列出了生成事件的操作：

|操作|描述|
|----------|---------|
| `audit-log.bare-metal.provision`             | 当发起方供应裸机服务器时，将生成事件。|
| `audit-log.bare-metal-port.disable`          | 当发起方禁用裸机服务器中的端口时，将生成事件。 |
| `audit-log.bare-metal-port.enable`           | 当发起方启用裸机服务器中的端口时，将生成事件。 |
| `audit-log.bare-metal-port-speed.update`     | 当发起方更新裸机服务器中的端口速度时，将生成事件。 |
| `audit-log.bare-metal.power-off`             | 当发起方关闭裸机服务器的电源时，将生成事件。  |
| `audit-log.bare-metal.reboot`                | 当发起方重新引导裸机服务器时，将生成事件。 |
| `audit-log.bare-metal.soft-reboot`           | 当发起方在裸机服务器上执行软重新引导时，将生成事件。 |
| `audit-log.bare-metal.hard-reboot`           | 当发起方在裸机服务器上执行硬重新引导时，将生成事件。 |
| `audit-log.bare-metal.power-on`              | 当发起方开启裸机服务器的电源时，将生成事件。  |
| `audit-log.bare-metal.rename`                | 当发起方重命名裸机服务器时，将生成事件。 |
| `audit-log.bare-metal.rescue`                | 当发起方对裸机服务器进行急救时，将生成事件。 |
| `audit-log.bare-metal.reload`                | 当发起方对裸机服务器执行操作系统 (OS) 重装时，将生成事件。 |
{: caption="表 2. 裸机操作" caption-side="top"}


## 查看事件
{: #bm-view-events}

{{site.data.keyword.cloudaccesstrailshort}} 事件在生成这些事件的 {{site.data.keyword.Bluemix_notm}} 区域中可用的 {{site.data.keyword.cloudaccesstrailshort}} **帐户域**中提供。有关更多信息，请参阅[查看帐户事件](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events)。

{{site.data.keyword.cloudaccesstrailshort}} 事件将自动转发到执行操作的相同区域中的 {{site.data.keyword.cloudaccesstrailshort}} 服务。
