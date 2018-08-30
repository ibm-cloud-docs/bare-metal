---

copyright:
  years: 1994, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Backup e recuperação

O {{site.data.keyword.Bluemix_notm}} fornece uma variedade de [soluções de backup e armazenamento](https://www.softlayer.com/cloud-storage) escaláveis para atender aos seus requisitos de backup. 
No entanto, o {{site.data.keyword.Bluemix_notm}} não conclui os backups de dispositivos do cliente. Um usuário em sua conta deve iniciar todos os backups planejados e únicos em seus dispositivos.

Se existirem dois ou mais {{site.data.keyword.baremetal_short}} em uma conta, os dados de um dispositivo poderão ser submetidos a backup no outro. 
Nenhum limite de largura da banda é imposto ao tráfego de rede privada, portanto, os dados podem ser transferidos entre quaisquer
dispositivos que compartilhem uma conta ou podem ser submetidos a backup para esses dispositivos a qualquer momento. Várias soluções de backup estão
disponíveis para os {{site.data.keyword.baremetal_short}}, incluindo as soluções a seguir:

1. [Backup de evault](../infrastructure/backup/index.html) é uma solução de backup corporativo que pode automatizar os backups ao longo de múltiplos servidores. Os dados são armazenados em uma SAN (rede de área de armazenamento) corporativa.
* [Network Attached Storage (NAS)](../infrastructure/network-attached-storage/nas.html) é um padrão de mercado e fornece armazenamento fora do servidor para dados críticos. Os dados são armazenados em uma SAN (rede de área de armazenamento) corporativa.
* O [R1Soft CDP](../infrastructure/backup/r1soft.html) fornece um backup de servidor de disco para disco de
alto desempenho que apresenta um gerenciamento central e um repositório de dados. O CDP do R1Soft protege dados em nível de bloco e blocos de disco exclusivo no servidor são armazenados apenas uma vez em todos os pontos de recuperação, aumentando a eficiência de armazenamento.
