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


# Eventi del programma di traccia dell'attività 
{: #bm-at-events}

Come gestore, revisore o responsabile della sicurezza, puoi utilizzare il servizio {{site.data.keyword.cloudaccesstrailfull}} per tenere traccia di come gli utenti e le applicazioni
interagiscono con i server bare metal in {{site.data.keyword.Bluemix}}. Gli utenti e il proprietario dell'account collegati all'account
possono attivare gli eventi del server bare metal registrati in {{site.data.keyword.cloudaccesstrailshort}}.
{:shortdesc}

Il servizio {{site.data.keyword.cloudaccesstrailshort}} registra le attività avviate dall'utente che modificano lo stato di un servizio in
{{site.data.keyword.Bluemix_notm}}. Per ulteriori informazioni, vedi
[Informazioni su {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov ).

Per iniziare a monitorare le azioni del tuo utente, vedi [Introduzione al Programma di traccia dell'attività IBM Cloud](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started#getting-started).

Un iniziatore può essere un utente, un servizio o un'applicazione. Perché un utente possa generare gli eventi, deve avere l'accesso alle risorse dell'**Infrastruttura** nella console {{site.data.keyword.Bluemix}}.
{: tip}

## Eventi dell'istanza del server bare metal
{: #bare-metal-events}

Puoi controllare un server bare metal tramite il suo ciclo di vita utilizzando il servizio {{site.data.keyword.cloudaccesstrailshort}}.

La seguente tabella elenca le azioni che generano un evento: 

|Azione|Descrizione|
|----------|---------|
| `audit-log.bare-metal.provision`             | Viene generato un evento quando un iniziatore esegue il provisioning di un server bare metal.  |
| `audit-log.bare-metal-port.disable`          | Viene generato un evento quando un iniziatore disabilita una porta in un server bare metal. |
| `audit-log.bare-metal-port.enable`           | Viene generato un evento quando un iniziatore abilita una porta in un server bare metal. |
| `audit-log.bare-metal-port-speed.update`     | Viene generato un evento quando un iniziatore aggiorna la velocità della porta in un server bare metal. |
| `audit-log.bare-metal.power-off`             | Viene generato un evento quando un iniziatore spegne un server bare metal.  |
| `audit-log.bare-metal.reboot`                | Viene generato un evento quando un iniziatore riavvia un server bare metal.  |
| `audit-log.bare-metal.soft-reboot`           | Viene generato un evento quando un iniziatore effettua un riavvio a caldo di un server bare metal. |
| `audit-log.bare-metal.hard-reboot`           | Viene generato un evento quando un iniziatore effettua un riavvio a freddo di un server bare metal. |
| `audit-log.bare-metal.power-on`              | Viene generato un evento quando un iniziatore accende un server bare metal.  |
| `audit-log.bare-metal.rename`                | Viene generato un evento quando un iniziatore ridenomina un server bare metal.  |
| `audit-log.bare-metal.rescue`                | Viene generato un evento quando un iniziatore recupera un server bare metal.  |
| `audit-log.bare-metal.reload`                | Viene generato un evento quando un iniziatore esegue un ricaricamento del sistema operativo (SO) per un server bare metal. |
{: caption="Tabella 2. Azioni bare metal" caption-side="top"}


## Visualizzazione degli eventi
{: #bm-view-events}

Gli eventi {{site.data.keyword.cloudaccesstrailshort}} sono disponibili nel **dominio dell'account** {{site.data.keyword.cloudaccesstrailshort}}
disponibile nella regione {{site.data.keyword.Bluemix_notm}} in cui vengono generati gli eventi. Per ulteriori informazioni, vedi [Visualizzazione degli
eventi dell'account](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events).

Gli eventi {{site.data.keyword.cloudaccesstrailshort}} vengono inoltrati automaticamente al servizio {{site.data.keyword.cloudaccesstrailshort}} nella stessa regione in cui si verifica l'azione.
