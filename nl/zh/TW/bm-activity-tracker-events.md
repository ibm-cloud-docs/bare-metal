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

身為安全主管、審核員或管理員，您可以使用 {{site.data.keyword.cloudaccesstrailfull}} 服務來追蹤使用者及應用程式如何與 {{site.data.keyword.Bluemix}} 中的裸機伺服器互動。帳戶擁有者以及與帳戶鏈結的使用者，可以觸發 {{site.data.keyword.cloudaccesstrailshort}} 中所記載的裸機伺服器事件。
{:shortdesc}

{{site.data.keyword.cloudaccesstrailshort}} 服務會記錄由使用者起始並且會變更 {{site.data.keyword.Bluemix_notm}} 中服務狀態的活動。如需相關資訊，請參閱[關於 {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov )。

若要開始監視使用者的動作，請參閱[開始使用 IBM Cloud Activity Tracker](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started#getting-started)。

起始者可以是使用者、服務或應用程式。若要讓使用者產生事件，使用者必須能夠在 {{site.data.keyword.Bluemix}} 主控台中存取**基礎架構**資源。
{: tip}

## 裸機伺服器實例事件
{: #bare-metal-events}

您可以使用 {{site.data.keyword.cloudaccesstrailshort}} 服務，在裸機伺服器的生命週期裡加以審核。

下表列出會產生事件的動作：

|動作 |說明 |
|----------|---------|
| `audit-log.bare-metal.provision`             |起始者佈建裸機伺服器時產生事件。|
| `audit-log.bare-metal-port.disable`          |起始者停用裸機伺服器的埠時產生事件。|
| `audit-log.bare-metal-port.enable`           |起始者啟用裸機伺服器的埠時產生事件。|
| `audit-log.bare-metal-port-speed.update`     |起始者更新裸機伺服器的埠速度時產生事件。|
| `audit-log.bare-metal.power-off`             |起始者關閉裸機伺服器的電源時產生事件。|
| `audit-log.bare-metal.reboot`                |起始者將裸機伺服器重新開機時產生事件。|
| `audit-log.bare-metal.soft-reboot`           |起始者執行裸機伺服器的正常重新開機時產生事件。|
| `audit-log.bare-metal.hard-reboot`           |起始者執行裸機伺服器的強迫重新開機時產生事件。|
| `audit-log.bare-metal.power-on`              |起始者開啟裸機伺服器的電源時產生事件。|
| `audit-log.bare-metal.rename`                |起始者將裸機伺服器重新命名時產生事件。|
| `audit-log.bare-metal.rescue`                |起始者救援裸機伺服器時產生事件。|
| `audit-log.bare-metal.reload`                |起始者執行裸機伺服器的作業系統 (OS) 重新載入時產生事件。|
{: caption="表 2. 裸機動作" caption-side="top"}


## 檢視事件
{: #bm-view-events}

{{site.data.keyword.cloudaccesstrailshort}} 事件提供於事件產生所在之 {{site.data.keyword.Bluemix_notm}} 地區中可用的 {{site.data.keyword.cloudaccesstrailshort}} **帳戶網域**。如需相關資訊，請參閱[檢視帳戶事件](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events)。

{{site.data.keyword.cloudaccesstrailshort}} 事件會自動轉遞至動作發生所在之相同地區的 {{site.data.keyword.cloudaccesstrailshort}} 服務中。
