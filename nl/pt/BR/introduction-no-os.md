---
copyright:
  years: 1994, 2017
lastupdated: "2017-06-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# A opção Sem S.O.

Sem S.O. é uma opção para pedir um servidor bare metal sem um sistema operacional.

## Como pedir um servidor bare metal sem S.O.?

Inicie colocando uma ordem para um servidor bare metal por meio do [SoftLayer.com](softlayer.com) ou do [Portal do cliente](https://control.softlayer.com).

1. Selecione **Outro** em **Configuração do sistema > Sistema operacional**.
2. Selecione **Sem sistema operacional**.

## Como instalar um sistema operacional em um servidor Sem S.O.?

Há dois métodos para instalar um sistema operacional em um servidor bare metal sem sistema operacional.

### Opção 1: servidor PXE

Um servidor bare metal sem sistema operacional pode ser configurado para inicializar e carregar o S.O. de uma configuração do PXE (veja [Preboot_Execution_Environment](http://en.wikipedia.org/wiki/Preboot_Execution_Environment) para obter mais informações). Basta implementar o servidor bare metal em um ambiente de rede com uma configuração do PXE (isso envolve geralmente a execução dos daemons DHCP e TFTP) e configurar o novo BIOS do servidor bare metal para ser inicializado por meio do adaptador de rede. Para que isso funcione de forma adequada, esteja ciente de que a configuração do PXE precisa estar na mesma VLAN que a configuração do PXE ou o encaminhamento de DHCP precisará ser usado.

**Nota:** pode ser necessário abrir um chamado de suporte solicitando que as portas do comutador sejam reagrupadas no modo básico para que essa opção funcione. Isso é devido ao fato de que o protocolo PXE não requer compatibilidade com agregação de link (ou seja, LACP, veja [Agregação de link](http://en.wikipedia.org/wiki/Link_aggregation)), que agora é um recurso padrão para fornecer redundância. Outra opção é pedir o servidor com uplinks Sem ligação (sem agregação de link) e, em seguida, mudá-los para uplinks redundantes depois de ter o S.O. instalado.

### Opção 2: dispositivo IPMI

Instale um sistema operacional em um servidor bare metal sem sistema operacional, inicializando por meio de um ISO via dispositivo IPMI incluído. Clique [aqui](mount-iso-bare-metal-server.html) para obter informações adicionais sobre como inicializar por meio de um ISO.
