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


# Eventos de rastreador de atividade
{: #bm-at-events}

Como responsável pela segurança, auditor ou gerente, você pode usar o serviço
{{site.data.keyword.cloudaccesstrailfull}} para rastrear como usuários e
aplicativos interagem com servidores bare metal no {{site.data.keyword.Bluemix}}. O
proprietário da conta e os usuários que estão vinculados com a conta podem acionar
eventos de servidor bare metal que estão registrados no
{{site.data.keyword.cloudaccesstrailshort}}.{:shortdesc}

O serviço {{site.data.keyword.cloudaccesstrailshort}} registra atividades iniciadas pelo usuário que mudam o estado de um serviço no {{site.data.keyword.Bluemix_notm}}. Para obter mais informações, consulte [Sobre o {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-activity_tracker_ov#activity_tracker_ov ).

Para começar a monitorar as ações do usuário, consulte
[Introdução
ao IBM Cloud Activity Tracker](/docs/services/cloud-activity-tracker?topic=cloud-activity-tracker-getting-started#getting-started).

Um inicializador pode ser um usuário, um serviço ou um aplicativo. Para que um usuário gere eventos, ele deve ter acesso aos recursos de **Infraestrutura** no console do {{site.data.keyword.Bluemix}}.
{: tip}

## Eventos de instância do servidor bare metal
{: #bare-metal-events}

É possível auditar um servidor bare metal por meio de seu ciclo de vida usando o
serviço {{site.data.keyword.cloudaccesstrailshort}}.

A tabela a seguir lista as ações que geram um evento:

| Ação | Descrição |
|----------|---------|
| `audit-log.bare-metal.provision`             | Um evento é gerado quando um inicializador provisiona um servidor bare metal.  |
| `audit-log.bare-metal-port.disable`          | Um evento é gerado quando um inicializador desativa uma porta em um servidor bare metal. |
| `audit-log.bare-metal-port.enable`           | Um evento é gerado quando um inicializador ativa uma porta em um servidor bare metal. |
| `audit-log.bare-metal-port-speed.update`     | Um evento é gerado quando um inicializador atualiza a velocidade da porta em um servidor bare metal. |
| `audit-log.bare-metal.power-off`             | Um evento é gerado quando um inicializador desliga um servidor bare metal.  |
| `audit-log.bare-metal.reboot`                | Um evento é gerado quando um inicializador reinicializa um servidor bare metal. |
| `audit-log.bare-metal.soft-reboot`           | Um evento é gerado quando um inicializador faz uma reinicialização normal em um servidor bare metal. |
| `audit-log.bare-metal.hard-reboot`           | Um evento é gerado quando um inicializador faz uma reinicialização forçada em um servidor bare metal. |
| `audit-log.bare-metal.power-on`              | Um evento é gerado quando um inicializador liga um servidor bare metal. |
| `audit-log.bare-metal.rename`                | Um evento é gerado quando um inicializador renomeia um servidor bare metal. |
| `audit-log.bare-metal.rescue`                | Um evento é gerado quando um inicializador resgata um servidor bare metal. |
| `audit-log.bare-metal.reload`                | Um evento é gerado quando um inicializador executa um recarregamento do sistema operacional (OS) para um servidor bare metal. |
{: caption="Tabela 2. Ações de bare metal" caption-side="top"}


## Visualizando Eventos
{: #bm-view-events}

Os eventos do {{site.data.keyword.cloudaccesstrailshort}} estão disponíveis no **domínio
da conta** do {{site.data.keyword.cloudaccesstrailshort}} que
está disponível na região do {{site.data.keyword.Bluemix_notm}} em que os eventos são gerados. Para obter mais informações, consulte [Visualizando eventos
de conta](/docs/services/cloud-activity-tracker/how-to/manage-events-ui?topic=cloud-activity-tracker-view_acc_events#account_events).

Os eventos do {{site.data.keyword.cloudaccesstrailshort}} são encaminhados automaticamente para o serviço
do {{site.data.keyword.cloudaccesstrailshort}} na mesma região em que a ação acontece.
