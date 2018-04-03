---
copyright:
  years: 1994, 2017
lastupdated: "2017-08-29"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Criando e ajustando as configurações do Adaptec RAID

O BIOS do Adaptec RAID permite configurar e gerenciar a configuração do RAID. Use esse BIOS se você estiver usando a opção [Sem S.O.](introduction-no-os.html) e deseja definir uma configuração de unidade específica.

## Acessando o dispositivo IPMI para interagir com o BIOS do RAID

Independentemente de sua máquina tem um controlador Adaptec ou um controlador LSI, você precisará acessar o servidor usando o IPMI para interagir com o BIOS do RAID. Para interagir com IPMI, você precisará primeiro se conectar à VPN {{site.data.keyword.IBM&reg; Cloud}} do Adaptec.
1. Efetue login na VPN por meio de [SSL](/infrastructure/vpn/ssl-vpn-connections.html) ou PPTP. Consulte a [página do tópico VPN](/infrastructure/vpn/index.html).
* Acesse a Lista de dispositivos no [Portal do cliente](https://control.softlayer.com/). Consulte [Acessar a lista de dispositivos](../vsi/vsi_managing.html).
* Clique no dispositivo que você deseja acessar.
* Selecione a guia Gerenciamento remoto para localizar os detalhes de acesso ao IPMI dos servidores.
* Coloque o IP de seu dispositivo IPMI no navegador e efetue login.
* Para iniciar a interação com o console remoto, clique em Controle remoto > Redirecionamento do console.

## Criando matrizes RAID

Durante o processo de inicialização, pressione Ctrl + A para acessar o BIOS do RAID.

Para iniciar a configuração do RAID, entre em Configuração do dispositivo lógico (primeira opção). Isso varre a topologia de suas unidades e exibe um menu no qual é possível gerenciar matrizes, criar matrizes e concluir outras tarefas de administração de unidade.

O exemplo a seguir mostra como criar uma matriz. Uma lista de unidades disponíveis para uso é apresentada a você ao criar sua matriz RAID.

1. Para selecionar as unidades, pressione a barra de ESPAÇO para preencher a caixa *Unidades selecionadas*.
* Depois de selecionar todas as unidades que você gostaria de usar em sua matriz, pressione ENTER para acessar a etapa de configuração do RAID.
* Escolha o tipo de RAID que você gostaria. Se precisar de assistência para descobrir qual configuração do RAID melhor se adequa às suas necessidades, veja as [FAQs do Adaptec](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm) a seguir.
* Forneça um Rótulo de matriz durante a configuração. É uma boa prática incluir o tipo de RAID no rótulo (por exemplo: RAID10-A).
* Pressione Enter para navegar nas configurações restantes. Use os valores padrão.

Depois de concluir a configuração selecione Pronto e o RAID será criado. É possível ver sua nova Matriz selecionando 'Gerenciar matrizes' no Menu principal. Para sair do utilitário de configuração, pressione a tecla ESC até que você seja solicitado a Sair do BIOS do Adaptec.

## Removendo matrizes existentes

Se precisar remover uma matriz existente, você acessará Gerenciar matrizes > Selecionar a matriz a ser removida e pressionará Excluir e confirmará.

## Configurações de exemplo

1. Em um servidor com 6 unidades totais, é possível configurar 2 SSDs em um RAID0 para seu Sistema operacional e 4 unidades adicionais em um RAID10 para seus dados reais. Isso permitirá recarregar rapidamente o S.O. de servidores sem restaurar seu site ou dados de serviço se ele estiver localizado na matriz secundária.

* Em um servidor cPanel, é possível ter /var e /home em Matrizes RAID SSD separadas. Como esses são os 2 diretórios com E/S mais intensiva em um servidor cPanel, é possível diminuir potencialmente o tempo de resposta do site com as configurações a seguir:
  * RAID0 (2 unidades SATA) - /
  * RAID0 (2 unidades SSD) - /var
  * RAID0 (2 unidades SSD) - /home
  * RAID10 (4 unidades SATA) - /backup

* Use uma única matriz RAID para configurar múltiplas partições lógicas. Por exemplo, use duas unidades de 4 TB configuradas em um RADI1. É possível particionar a RAID para ajustar às suas necessidades. Por
exemplo:
  * Partição primária de 100 GB para seu Sistema operacional
  * Segunda partição de 500 GB para seus dados
  * Terceira partição do espaço restante para backups
