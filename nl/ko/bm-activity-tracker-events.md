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


# Activity Tracker 이벤트
{: #bm-at-events}

보안 담당자, 감사자 또는 관리자인 경우에는 {{site.data.keyword.cloudaccesstrailfull}} 서비스를 사용하여 사용자와 애플리케이션이 {{site.data.keyword.Bluemix}}에서 베어메탈 서버와 상호작용하는 방법을 추적할 수 있습니다. 계정와 연결된 계정 소유자와 사용자는 {{site.data.keyword.cloudaccesstrailshort}}에 로깅된 베어메탈 서버 이벤트를 트리거할 수 있습니다.
{:shortdesc}

{{site.data.keyword.cloudaccesstrailshort}} 서비스는 {{site.data.keyword.Bluemix_notm}}에서 서비스의 상태를 변경하는 사용자 시작 활동을 기록합니다. 자세한 정보는 [{{site.data.keyword.cloudaccesstrailshort}} 정보](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov )를 참조하십시오.

사용자 조치의 모니터링을 시작하려면 [IBM Cloud Activity Tracker 시작하기](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started#getting-started)를 참조하십시오.

개시자는 사용자, 서비스 또는 애플리케이션일 수 있습니다. 사용자가 이벤트를 생성하려면 사용자가 {{site.data.keyword.Bluemix}} 콘솔에서 **인프라** 리소스에 대한 액세스 권한을 보유해야 합니다.
{: tip}

## 베어메탈 서버 인스턴스 이벤트
{: #bare-metal-events}

{{site.data.keyword.cloudaccesstrailshort}} 서비스를 사용하여 라이프사이클 중에 베어메탈 서버를 감사할 수 있습니다.

다음 표에는 이벤트를 생성하는 조치가 나열되어 있습니다.

| 조치 |설명 |
|----------|---------|
| `audit-log.bare-metal.provision`             | 개시자가 베어메탈 서버를 프로비저닝할 때 이벤트가 생성됩니다. |
| `audit-log.bare-metal-port.disable`          | 개시자가 베어메탈 서버의 포트를 사용 안함으로 설정할 때 이벤트가 생성됩니다. |
| `audit-log.bare-metal-port.enable`           | 개시자가 베어메탈 서버의 포트를 사용으로 설정할 때 이벤트가 생성됩니다. |
| `audit-log.bare-metal-port-speed.update`     | 개시자가 베어메탈 서버의 포트 속도를 업데이트할 때 이벤트가 생성됩니다. |
| `audit-log.bare-metal.power-off`             | 개시자가 베어메탈 서버의 전원을 끌 때 이벤트가 생성됩니다. |
| `audit-log.bare-metal.reboot`                | 개시자가 베어메탈 서버를 재부팅할 때 이벤트가 생성됩니다. |
| `audit-log.bare-metal.soft-reboot`           | 개시자가 베어메탈 서버에서 소프트 재부팅을 수행할 때 이벤트가 생성됩니다. |
| `audit-log.bare-metal.hard-reboot`           | 개시자가 베어메탈 서버에서 하드 재부팅을 수행할 때 이벤트가 생성됩니다. |
| `audit-log.bare-metal.power-on`              | 개시자가 베어메탈 서버의 전원을 켤 때 이벤트가 생성됩니다. |
| `audit-log.bare-metal.rename`                | 개시자가 베어메탈 서버의 이름을 바꿀 때 이벤트가 생성됩니다. |
| `audit-log.bare-metal.rescue`                | 개시자가 베어메탈 서버를 구제할 때 이벤트가 생성됩니다. |
| `audit-log.bare-metal.reload`                | 개시자가 베어메탈 서버의 운영 체제(OS) 재로드를 수행할 때 이벤트가 생성됩니다. |
{: caption="표 2. 베어메탈 조치" caption-side="top"}


## 이벤트 보기
{: #bm-view-events}

{{site.data.keyword.cloudaccesstrailshort}} 이벤트는 이벤트가 생성된 {{site.data.keyword.Bluemix_notm}} 지역에서 사용 가능한 {{site.data.keyword.cloudaccesstrailshort}} **계정 도메인**에서 사용될 수 있습니다. 자세한 정보는 [계정 이벤트 보기](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events)를 참조하십시오.

{{site.data.keyword.cloudaccesstrailshort}} 이벤트는 조치가 발생한 동일 지역의 {{site.data.keyword.cloudaccesstrailshort}} 서비스로 자동 전달됩니다.
