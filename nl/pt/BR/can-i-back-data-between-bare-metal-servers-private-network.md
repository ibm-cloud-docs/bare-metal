---

copyright:
  years: 1994, 2019
lastupdated: "2019-05-02"

keywords: back up, recovery, IBM Cloud Backup, r1soft

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Backup e recuperação
{: #sm-back-up-recovery}

O {{site.data.keyword.Bluemix_notm}} fornece uma variedade de [soluções de backup e armazenamento ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/cloud/storage){: new_window} escaláveis para atender a seus requisitos de backup. No entanto, o {{site.data.keyword.Bluemix_notm}} não conclui os backups de dispositivos do cliente. Um usuário em sua conta deve iniciar todos os backups planejados e únicos em seus dispositivos.

Se existirem dois ou mais {{site.data.keyword.baremetal_short}} em uma conta, os dados de um dispositivo poderão ser submetidos a backup no outro. Nenhum limite de largura da banda é imposto ao tráfego de rede privada, portanto, os dados podem ser transferidos entre quaisquer dispositivos que compartilhem uma conta ou podem ser submetidos a backup para esses dispositivos a qualquer momento. Várias soluções de backup estão disponíveis para os {{site.data.keyword.baremetal_short}}, incluindo as soluções a seguir:

* O [IBM Cloud Backup](/docs/infrastructure/Backup?topic=Backup-getting-started#getting-started) é uma solução de backup corporativo que pode automatizar backups em múltiplos servidores. Os dados são armazenados em uma SAN (rede de área de armazenamento) corporativa.
* [Network Attached Storage (NAS)](/docs/infrastructure/network-attached-storage?topic=network-attached-storage-GettingStarted#GettingStarted) é um padrão de mercado e fornece armazenamento fora do servidor para dados críticos. Os dados são armazenados em uma SAN (rede de área de armazenamento) corporativa.
* O [R1Soft CDP](/docs/infrastructure/software?topic=software-ordering-r1soft#ordering-r1soft) fornece um backup de servidor de disco para disco de alto desempenho que apresenta um gerenciamento central e um repositório de dados. O CDP do R1Soft protege dados em nível de bloco e blocos de disco exclusivo no servidor são armazenados apenas uma vez em todos os pontos de recuperação, aumentando a eficiência de armazenamento.
