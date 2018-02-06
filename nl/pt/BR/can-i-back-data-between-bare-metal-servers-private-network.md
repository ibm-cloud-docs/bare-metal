---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Backup e recuperação

O {{site.data.keyword.Bluemix_notm}} fornece uma variedade de [soluções de backup e armazenamento](https://www.softlayer.com/cloud-storage) escaláveis para atender aos seus requisitos de backup. No entanto, nós não concluímos backups de dispositivos de cliente. Um usuário em sua conta deve iniciar todos os backups planejados e únicos em seus dispositivos.

Se existirem dois ou mais {{site.data.keyword.baremetal_short}} em uma conta, os dados de um dispositivo poderão ser submetidos a backup no outro. Não há limite de largura da banda para o tráfego de Rede privada, então os dados podem ser transferidos ou submetidos a backup para qualquer dispositivo que compartilha uma conta a qualquer momento.
Há várias soluções de backup disponíveis para o {{site.data.keyword.baremetal_short}}, incluindo as seguintes:

1. [Backup de evault](/infrastructure/backup/index.html) é uma solução de backup corporativo que pode automatizar os backups ao longo de múltiplos servidores. Os dados são armazenados em uma SAN (rede de área de armazenamento) corporativa.
* [Network Attached Storage (NAS)](/infrastructure/network-attached-storage/nas.html) é um padrão de mercado e fornece armazenamento fora do servidor para dados críticos. Os dados são armazenados em uma SAN (rede de área de armazenamento) corporativa.
* [CDP do R1Soft](/infrastructure/backup/r1soft.html) fornece backup de servidor de disco para disco de alto desempenho apresentando um gerenciamento central e um repositório de dados. O CDP do R1Soft protege dados em nível de bloco e blocos de disco exclusivo no servidor são armazenados apenas uma vez em todos os pontos de recuperação, aumentando a eficiência de armazenamento.
