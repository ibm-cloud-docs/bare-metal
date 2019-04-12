---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# A opção Sem S.O.
{: #bm-no-os}

Sem S.O. é uma opção para pedir um servidor bare metal sem um sistema operacional.

## Como pedir um servidor bare metal sem S.O.?

Inicie colocando uma ordem para um servidor bare metal por meio do [SoftLayer.com](https://www.softlayer.com) ou do [Portal do cliente](https://control.softlayer.com).

1. Selecione **Outro** em **Configuração do sistema > Sistema operacional**.
2. Selecione **Sem sistema operacional**.

## Como instalar um sistema operacional em um servidor Sem S.O.?

Há dois métodos para instalar um sistema operacional em um servidor bare metal sem sistema operacional.

### Opção 1: servidor PXE

Um servidor bare metal sem sistema operacional pode ser configurado para inicializar e carregar o S.O. de uma configuração do PXE (veja [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) para obter mais informações). Basta implementar o servidor bare metal em um ambiente de rede com uma configuração do PXE (isso envolve geralmente a execução dos daemons DHCP e TFTP) e configurar o novo BIOS do servidor bare metal para ser inicializado por meio do adaptador de rede. 
Para que a opção Nenhum S.O. funcione corretamente, a configuração do PXE precisa estar na mesma VLAN que o Bare Metal Server ou o
encaminhamento DHCP precisará ser usado.

**Nota:** pode ser necessário abrir um chamado de suporte para solicitar que as portas do comutador
sejam reagrupadas no modo básico para que essa opção funcione. Isso porque o protocolo PXE não requer compatibilidade com a agregação
de link (isto é, LACP; consulte [Agregação de link](http://en.wikipedia.org/wiki/Link_aggregation)), que agora é
um recurso padrão para fornecer redundância. Outra opção é solicitar o servidor com uplinks não ligados (sem agregação de link) e,
então, mudá-los para uplinks redundantes após o S.O. ter sido instalado.

### Opção 2: dispositivo IPMI

Instale um sistema operacional em um servidor bare metal sem sistema operacional, inicializando por meio de um ISO via dispositivo IPMI incluído. Clique [aqui](mount-iso-bare-metal-server.html) para obter informações adicionais sobre como inicializar por meio de um ISO.
