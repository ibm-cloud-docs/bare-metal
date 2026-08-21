---

copyright:
  years: 2016, 2026
  lastupdated: "2026-08-21"

keywords: activity tracker, at events, activity tracker events

subcollection: bare-metal

---

{{site.data.keyword.attribute-definition-list}}

# Activity Tracker events
{: #bm-at-events}

As a security officer, auditor, or manager, you can use {{site.data.keyword.cloudaccesstrailfull}} to track how users and
applications interact with bare metal servers in {{site.data.keyword.cloud}}. The account owner and users that are linked
with the account can trigger bare metal server events that are logged in {{site.data.keyword.cloudaccesstrailshort}}.
{: shortdesc}

The {{site.data.keyword.cloudaccesstrailshort}} service records user-initiated activities that change the state of a service in
{{site.data.keyword.cloud_notm}}.
An initiator can be a user, a service, or an application. For a user to generate events, the user must have access to **Infrastructure** resources in {{site.data.keyword.cloud}} console.
{: tip}

## Bare metal server instance events
{: #bare-metal-events}

You can audit a bare metal server through its life cycle by using {{site.data.keyword.cloudaccesstrailshort}}.

The following table lists the actions that generate an event:

| Action | Description |
|----------|---------|
| `audit-log.bare-metal.provision`             | An event is generated when an initiator provisions a bare metal server.  |
| `audit-log.bare-metal-port.disable`          | An event is generated when an initiator disables a port in a bare metal server. |
| `audit-log.bare-metal-port.enable`           | An event is generated when an initiator enables a port in a bare metal server. |
| `audit-log.bare-metal-port-speed.update`     | An event is generated when an initiator updates the port speed in a bare metal server. |
| `audit-log.bare-metal.power-off`             | An event is generated when an initiator powers off a bare metal server.  |
| `audit-log.bare-metal.reboot`                | An event is generated when an initiator reboots a bare metal server. |
| `audit-log.bare-metal.soft-reboot`           | An event is generated when an initiator does a soft reboot on a bare metal server. |
| `audit-log.bare-metal.hard-reboot`           | An event is generated when an initiator does a hard reboot on a bare metal server. |
| `audit-log.bare-metal.power-on`              | An event is generated when an initiator powers on a bare metal server. |
| `audit-log.bare-metal.rename`                | An event is generated when an initiator renames a bare metal server. |
| `audit-log.bare-metal.rescue`                | An event is generated when an initiator rescues a bare metal server. |
| `audit-log.bare-metal.reload`                | An event is generated when an initiator performs an operating system (OS) reload for a bare metal server. |
{: caption="Bare metal actions" caption-side="top"}


## Viewing events
{: #bm-view-events}

The {{site.data.keyword.cloudaccesstrailshort}} events are available in the {{site.data.keyword.cloudaccesstrailshort}} **account domain** that
is available in the {{site.data.keyword.cloud_notm}} region where the events are generated.

{{site.data.keyword.cloudaccesstrailshort}} events are automatically forwarded to the {{site.data.keyword.cloudaccesstrailshort}} service
in the same region where the action happens.
