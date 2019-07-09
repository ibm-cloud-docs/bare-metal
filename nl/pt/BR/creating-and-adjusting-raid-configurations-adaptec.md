---

copyright:
  years: 2017, 2019
lastupdated: "2018-07-10"

keywords: raid, adaptec, ipmi, raid bios, raid array, RAID configuration

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Criando e ajustando as configurações do Adaptec RAID
{: #bm-create-raid-config}

O BIOS do RAID Adaptec permite definir e gerenciar a configuração do RAID. Utilize esse BIOS se estiver usando a nossa opção
[Nenhum S.O.](/docs/bare-metal?topic=bare-metal-the-no-os-option) e desejar definir uma configuração de unidade específica.

## Acessando o dispositivo IPMI para interagir com o BIOS do RAID
{: #bm-access-ipmi}

Independentemente de sua máquina ter um controlador Adaptec ou um controlador LSI, é necessário acessar o servidor que usa o IPMI para interagir com o BIOS do RAID. Para interagir com o IPMI, é necessário primeiro se conectar à VPN {{site.data.keyword.cloud}} do Adaptec.
1. Efetue login na VPN por meio de [SSL](/docs/infrastructure/iaas-vpn?topic=VPN-setup-ssl-vpn-connections#setup-ssl-vpn-connections) ou PPTP.
* Acesse a Lista de dispositivos no [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/){: new_window}. Consulte [Acessar a lista de dispositivos](/docs/infrastructure/vsi?topic=virtual-servers-managing-virtual-servers).
* Clique no dispositivo que deseja acessar.
* Selecione a guia Gerenciamento remoto para localizar os detalhes de acesso do IPMI do servidor.
* Coloque o IP de seu dispositivo IPMI no navegador e efetue login.
* Para iniciar a interação com o console remoto, clique em **Controle remoto > Redirecionamento do console**.

## Criando matrizes RAID
{: #bm-create-raid-array}

Durante o processo de início, pressione **Ctrl+A** para acessar o BIOS do RAID.

Para iniciar a configuração do RAID, abra a Configuração do dispositivo lógico (primeira opção). Essa opção varre a topologia das unidades e exibe um menu no qual é possível gerenciar e criar as matrizes, e concluir as outras tarefas de administração da unidade.

O exemplo a seguir mostra como criar uma matriz. Uma lista de unidades disponíveis para uso é apresentada a você ao criar sua matriz RAID.

1. Para selecionar as unidades, pressione a barra de espaço para preencher a caixa *Unidades selecionadas*.
* Depois de selecionar todas as unidades que você gostaria de usar em sua matriz, pressione ENTER para acessar a etapa de configuração do RAID.
* Escolha o tipo de RAID que deseja usar. Se precisar de assistência para descobrir qual configuração de RAID melhor se adéqua às suas necessidades, veja as [Perguntas frequentes do Adaptec ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://www.adaptec.com/en-us/_common/compatibility/_education/raid_level_compar_wp.htm){: new_window}a seguir.
* Forneça um Rótulo de matriz durante a configuração. É uma boa prática incluir o tipo de RAID no rótulo (por exemplo: RAID10-A).
* Pressione **Enter** para acessar as configurações restantes. Use os valores padrão.

Depois de concluir a configuração, selecione Pronto e o RAID é criado. É possível ver a nova Matriz selecionando 'Gerenciar matrizes' no menu principal. Para sair do utilitário de configuração, pressione a tecla ESC até que você seja solicitado a Sair do BIOS do Adaptec.

## Removendo matrizes RAID existentes
{: #bm-remove-raid-array}

Se for necessário remover uma matriz existente, acesse **Gerenciar matrizes**, selecione a matriz a ser removida, pressione **Excluir** e confirme.

## Configurações de exemplo
{: #bm-example-config}

1. Em um servidor com seis unidades totais, é possível configurar duas SSDs em um RAID 0 para o sistema operacional e mais quatro unidades em um RAID 10 para os dados reais. Use essa configuração para recarregar rapidamente o S.O. do servidor sem restaurar os dados do site ou de serviço se eles estiverem na matriz secundária.

* Em um servidor cPanel, é possível ter /var e /home em Matrizes RAID SSD separadas. Como os diretórios são os dois diretórios de E/S mais intensivos em um servidor do cPanel, é possível diminuir potencialmente o tempo de resposta do site com as configurações a seguir:
  * RAID0 (2 unidades SATA) - /
  * RAID0 (2 unidades SSD) - /var
  * RAID0 (2 unidades SSD) - /home
  * RAID10 (4 unidades SATA) - /backup

* Use uma única matriz RAID para configurar múltiplas partições lógicas. Por exemplo, use duas unidades de 4 TB configuradas em um RAID 1. É possível particionar o RAID para atender às suas necessidades. Veja o exemplo a seguir:
  * Partição primária de 100 GB para o sistema operacional
  * Segunda partição de 500 GB para os dados
  * Terceira partição do espaço restante para backups
