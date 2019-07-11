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


# Activity Tracker-Ereignisse
{: #bm-at-events}

Als Sicherheitsbeauftragter, Auditor oder Manager können Sie den {{site.data.keyword.cloudaccesstrailfull}}-Service verwenden, um zu verfolgen, wie Benutzer und Anwendungem mit Bare-Metal-Servern in {{site.data.keyword.Bluemix}} interagieren. Der Kontoeigner und Benutzer, die mit dem Konto verknüpft sind, können Bare-Metal-Server-Ereignisse auslösen, die in {{site.data.keyword.cloudaccesstrailshort}} protokolliert werden.
{:shortdesc}

Der {{site.data.keyword.cloudaccesstrailshort}}-Service zeichnet von Benutzern initiiert Aktivitäten auf, die den Status eines Service in
{{site.data.keyword.Bluemix_notm}} ändern. Weitere Informationen finden Sie unter
[Informationen zu {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov ).

Eine Einführung in die Überwachung der Aktionen Ihrer Benutzer finden Sie unter [Einführung in IBM Cloud Activity Tracker](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started#getting-started).

Ein Initiator kann ein Benutzer, ein Service oder eine Anwendung sein. Damit ein Benutzer Ereignisse generieren kann, benötigt er Zugriff auf **Infrastrukturressourcen** in der {{site.data.keyword.Bluemix}}-Konsole.
{: tip}

## Bare-Metal-Server-Instanzereignisse
{: #bare-metal-events}

Sie können einen Bare-Metal-Server während seines Lebenszyklus mithilfe des {{site.data.keyword.cloudaccesstrailshort}}-Service auditieren.

In der folgenden Tabelle werden die Aktionen aufgelistet, die ein Ereignis generieren:

| Aktion | Beschreibung |
|----------|---------|
| `audit-log.bare-metal.provision`             | Ein Ereignis wird generiert, wenn ein Initiator einen Bare-Metal-Server bereitstellt. |
| `audit-log.bare-metal-port.disable`          | Ein Ereignis wird generiert, wenn ein Initiator einen Port auf einem Bare-Metal-Server inaktiviert. |
| `audit-log.bare-metal-port.enable`           | Ein Ereignis wird generiert, wenn ein Initiator einen Port auf einem Bare-Metal-Server aktiviert. |
| `audit-log.bare-metal-port-speed.update`     | Ein Ereignis wird generiert, wenn ein Initiator die Portgeschwindigkeit auf einem Bare-Metal-Server aktualisiert. |
| `audit-log.bare-metal.power-off`             | Ein Ereignis wird generiert, wenn ein Initiator einen Bare-Metal-Server ausschaltet. |
| `audit-log.bare-metal.reboot`                | Ein Ereignis wird generiert, wenn ein Initiator einen Bare-Metal-Server neu startet. |
| `audit-log.bare-metal.soft-reboot`           | Ein Ereignis wird generiert, wenn ein Initiator einen Warmstart auf einem Bare-Metal-Server durchführt. |
| `audit-log.bare-metal.hard-reboot`           | Ein Ereignis wird generiert, wenn ein Initiator einen Kaltstart auf einem Bare-Metal-Server durchführt. |
| `audit-log.bare-metal.power-on`              | Ein Ereignis wird generiert, wenn ein Initiator einen Bare-Metal-Server einschaltet. |
| `audit-log.bare-metal.rename`                | Ein Ereignis wird generiert, wenn ein Initiator einen Bare-Metal-Server umbenennt. |
| `audit-log.bare-metal.rescue`                | Ein Ereignis wird generiert, wenn ein Initiator einen Bare-Metal-Server rettet. |
| `audit-log.bare-metal.reload`                |Ein Ereignis wird generiert, wenn ein Initiator ein Betriebssystem für einen Bare-Metal-Server neu lädt. |
{: caption="Tabelle 2. Bare-Metal-Aktionen" caption-side="top"}


## Ereignisse anzeigen
{: #bm-view-events}

Die {{site.data.keyword.cloudaccesstrailshort}}-Ereignisse sind in der {{site.data.keyword.cloudaccesstrailshort}}-**Kontodomäne** verfügbar, die in der {{site.data.keyword.Bluemix_notm}}-Region verfügbar sind, in der die Ereignisse generiert werden. Weitere Informationen finden Sie unter [Kontoereignisse anzeigen](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events).

{{site.data.keyword.cloudaccesstrailshort}}-Ereignisse werden automatisch an den {{site.data.keyword.cloudaccesstrailshort}}-Service in derselben Region, in der die Aktion auftritt, weitergeleitet.

