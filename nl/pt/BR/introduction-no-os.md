---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-24"

keywords: bare metal, no os, no operating system

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:note: .note}

# A opção Sem S.O.
{: #bm-no-os}

**Nenhum S.O.** é uma opção para solicitar o {{site.data.keyword.baremetal_long}} sem um sistema operacional.

## Solicitando o {{site.data.keyword.baremetal_short}} sem S.O.
{: #ordering-no-os}

1. Use as etapas descritas em
[Construindo um
servidor bare metal customizado](/docs/bare-metal?topic=bare-metal-ordering-baremetal-server) para solicitar seu servidor.
2. Selecione **Nenhum S.O.** em **Imagem**.
3. Conclua o pedido do servidor. 

## Mudando para nenhum S.O.
{: #changing-to-no-os}

Um servidor pode ser reconfigurado para não ter nenhum S.O. A reconfiguração é
feita por meio de um recarregamento do S.O. Para obter informações de mor, consulte
[Recarregando o
S.O.](/docs/infrastructure/software?topic=software-reloading-the-os).

1. Clique em **Dispositivos** > **Lista de dispositivos**.
2. Selecione o servidor que deve ser reconfigurado sem S.O.
3. Clique em **Recarregamento do S.O.** e insira as informações
aplicáveis.

## Instalando um sistema operacional em um servidor sem S.O.
{: #installing-os-on-no-os-server}

Há dois métodos para instalar sistemas operacionais no {{site.data.keyword.baremetal_short}} sem nenhum sistema operacional.

### Opção 1: servidor PXE
{: #option-1}

O {{site.data.keyword.baremetal_short}} sem nenhum sistema operacional pode
ser configurado para inicializar e carregar um S.O. a partir de uma configuração de
PXE.<!--(see [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) for more information)--> Implemente o {{site.data.keyword.baremetal_short}} em um ambiente de rede com uma
configuração de PXE (isso geralmente envolve a execução de um daemon DHCP e TFTP) e
configure o novo BIOS de servidores para inicializar por meio do adaptador de rede. Para
que a opção nenhum S.O. funcione corretamente, a configuração de PXE precisa estar na
mesma VLAN que o {{site.data.keyword.baremetal_short}} ou o encaminhamento do
DHCP precisa ser usado.

Pode ser necessário abrir um chamado de suporte para solicitar que as portas do
comutador sejam reagrupadas no modo básico para que essa opção funcione. O motivo disso
é porque o protocolo PXE não requer compatibilidade com agregação de link (LACP),
<!--see [Link Aggregation](http://en.wikipedia.org/wiki/Link_aggregation))-->
que agora é um recurso padrão para fornecer redundância. Outra opção é solicitar o servidor com uplinks não ligados (sem agregação de link) e,
então, mudá-los para uplinks redundantes após o S.O. ter sido instalado.
{: note}

### Opção 2: dispositivo IPMI
{: #option-2}

Instale os sistemas operacionais no {{site.data.keyword.baremetal_short}}
sem sistemas operacionais inicializando a partir de um ISO por meio do dispositivo IPMI
incluído. Para obter mais informações sobre como inicializar a partir de um ISO, consulte
[Montando
um ISO em um servidor bare metal](/docs/bare-metal?topic=bare-metal-mounting-an-iso-on-a-bare-metal-server).
