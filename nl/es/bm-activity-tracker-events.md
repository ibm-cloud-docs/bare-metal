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


# Sucesos de Activity Tracker
{: #bm-at-events}

Como responsable de seguridad, auditor o gestor, puede utilizar el servicio {{site.data.keyword.cloudaccesstrailfull}} para realizar el seguimiento de cómo interactúan los usuarios y las aplicaciones con los servidores nativos en {{site.data.keyword.Bluemix}}. El propietario de la cuenta y los usuarios vinculados a la cuenta pueden activar sucesos de servidor nativo que se registran en {{site.data.keyword.cloudaccesstrailshort}}.
{:shortdesc}

El servicio {{site.data.keyword.cloudaccesstrailshort}} registra las actividades iniciadas por el usuario que cambian el estado de un servicio en {{site.data.keyword.Bluemix_notm}}. Para obtener más información, consulte [Acerca de {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov ).

Para empezar a supervisar las acciones del usuario, consulte [Iniciación a IBM Cloud Activity Tracker](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started#getting-started).

Un iniciador puede ser un usuario, un servicio o una aplicación. Para que un usuario genere sucesos, el usuario debe tener acceso a los recursos de **Infraestructura** en la consola de {{site.data.keyword.Bluemix}}.
{: tip}

## Sucesos de instancia de servidor nativo
{: #bare-metal-events}

Puede auditar una instancia de servidor nativo durante su ciclo de vida mediante el servicio {{site.data.keyword.cloudaccesstrailshort}}.

En la tabla siguiente se listan las acciones que generan un suceso:

| Acción | Descripción |
|----------|---------|
| `audit-log.bare-metal.provision`             | Se genera un suceso cuando un iniciador suministra un servidor nativo.  |
| `audit-log.bare-metal-port.disable`          | Se genera un suceso cuando un iniciador inhabilita un puerto en un servidor nativo. |
| `audit-log.bare-metal-port.enable`           | Se genera un suceso cuando un iniciador habilita un puerto en un servidor nativo. |
| `audit-log.bare-metal-port-speed.update`     | Se genera un suceso cuando un iniciador actualiza la velocidad de puerto en un servidor nativo. |
| `audit-log.bare-metal.power-off`             | Se genera un suceso cuando un iniciador apaga un servidor nativo.  |
| `audit-log.bare-metal.reboot`                | Se genera un suceso cuando un iniciador reinicia un servidor nativo. |
| `audit-log.bare-metal.soft-reboot`           | Se genera un suceso cuando un iniciador realiza un reinicio (soft reboot) de un servidor nativo. |
| `audit-log.bare-metal.hard-reboot`           | Se genera un suceso cuando un iniciador reinicia (hard reboot) un servidor nativo. |
| `audit-log.bare-metal.power-on`              | Se genera un suceso cuando un iniciador enciende un servidor nativo. |
| `audit-log.bare-metal.rename`                | Se genera un suceso cuando un iniciador cambia el nombre de un servidor nativo. |
| `audit-log.bare-metal.rescue`                | Se genera un suceso cuando un iniciador rescata un servidor nativo. |
| `audit-log.bare-metal.reload`                | Se genera un suceso cuando un iniciador realiza una recarga de sistema operativo (SO) para un servidor nativo. |
{: caption="Tabla 2. Acciones de servidor nativo" caption-side="top"}


## Visualización de sucesos
{: #bm-view-events}

Los sucesos de {{site.data.keyword.cloudaccesstrailshort}} están disponibles en el **dominio de la cuenta** de {{site.data.keyword.cloudaccesstrailshort}} que está disponible en la región de {{site.data.keyword.Bluemix_notm}} en la que se generan los sucesos. Para obtener más información, consulte [Visualización de sucesos de cuenta](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events).

Los sucesos de {{site.data.keyword.cloudaccesstrailshort}} se reenvían automáticamente al servicio {{site.data.keyword.cloudaccesstrailshort}} en la misma región en la que se produce la acción.
