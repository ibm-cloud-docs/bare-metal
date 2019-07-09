---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-03"

keywords: set up bare metal server

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Configurando um Bare Metal Server
{: #bm-set-up}

É possível configurar um Bare Metal Server como um servidor dedicado.
{:shortdesc}

## Antes de Come╬ar
* Navegue para o menu de dispositivos do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Assegure-se de que você tenha as permissões de conta e o acesso ao dispositivo necessários. Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões.

Para obter mais informações sobre as permissões, consulte [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/bare-metal?topic=virtual-servers-managing-device-access).

## Configurando um Bare Metal Server

Use as etapas a seguir para configurar um Bare Metal Server:

1. No menu, clique em **Dispositivos** > **Lista de dispositivos** e localize seu sistema. Todos os seus dispositivos são detalhados na Lista de dispositivos, na qual é possível gerenciar e atualizar dispositivos ou gerar gráficos de uso da largura da banda.

2. Escolha para gerenciar seu servidor de uma das maneiras a seguir:
  * Clique na seta Nome do dispositivo para visualizar um resumo e gerenciar seus
dispositivos a partir da visualização Captura instantânea.
  * Clique no Nome do Dispositivo do servidor para visualizar uma lista detalhada e gerencie seus dispositivos por meio da tela Detalhes do dispositivo.

3. Registre o endereço IP e as credenciais para o servidor em um local seguro para que você possa acessar os detalhes rapidamente sem precisar efetuar login no Portal do Cliente toda vez que precisar deles. É possível registrar esses detalhes para um dispositivo individual e para todos os dispositivos associados à sua conta:
  * Visualizar IPs de dispositivo individual da Lista de dispositivos.
  * Visualizar senhas raiz de dispositivo individual na Visualização de captura instantânea para o dispositivo.
  * Visualize vários IPs de dispositivo usando a opção **Fazer download do CSV** na **Lista de dispositivos**. Em seguida, selecione **Fazer download do CSV** na engrenagem **Configurações** para fazer download de uma lista completa de dispositivos e detalhes no formato de planilha.

4. Atualize as credenciais para sistemas operacionais e outro software. Todo o software que foi carregado em seu dispositivo durante o processo de fornecimento foi designado a credenciais temporárias. É possível visualizar e gerenciar essas credenciais na guia Senhas de cada dispositivo no Portal do Cliente. Use essas credenciais provisórias para acessar seu software pela primeira vez. Em seguida, mude a senha para seu software seguindo as práticas de senha forte. Crie uma
senha que consista em uma combinação de letras, números e símbolos. Opcionalmente, é possível armazenar atualizações de senha na guia Senhas de cada dispositivo. No entanto, quando você armazena senhas no portal do cliente, qualquer pessoa com acesso
à conta e permissões apropriadas pode visualizar as senhas que estão armazenadas na tela
Senhas.

5. Acesse seu servidor na rede privada. É possível usar a rede privada de
infraestrutura do {{site.data.keyword.cloud_notm}} para interagir
com seus dispositivos por meio da área de trabalho remota (RDP) usando SSH e KVM
sobre IP. É possível usar a ferramenta de Acesso à VPN para conexão de rede privada ao terminal da VPN SSL mais próximo ou ao terminal de sua escolha. O acesso à VPN também é necessário para interagir com vários serviços. Para acessar a rede privada, edite o acesso à VPN do usuário na Lista de usuários. Para acessar a Lista de usuários, clique em **Conta** > **Usuários** > **Lista de usuários**. Use a página [Rede Privada Virtual ![Ícone de link externo](../icons/launch-glyph.svg)](https://www.softlayer.com/VPN-Access){:new_window} para conectar-se a uma das várias opções de VPN.

6. Configure o monitoramento para verificar o status de seu servidor e saber quando escalar. É possível usar o monitoramento padrão ou serviços de monitoramento Nimsoft. É possível usar monitoramento padrão, ou básico, no método executar ping e responder usando um ping lento ou de serviço do portal do cliente. Também é possível usar o Nimsoft, ou avançado, monitoramento do portal do cliente ou em 1
de 3 camadas: básica, avançada e premium.

7. Proteja seu sistema. Use os firewalls de hardware disponíveis para proteger seu
dispositivo. É possível provisionar firewalls de hardware sob demanda sem tempo de inatividade, se as regras estiverem estabelecidas corretamente, para proteger seu servidor contra atividade indesejada. Depois de pedir o firewall, ele deve ser ativado e as regras devem ser configuradas.

8. Planeje backups para assegurar que seus dados sejam armazenados com segurança
fora de seu dispositivo e capazes de recarregar quaisquer dados perdidos. É possível escolher entre vários serviços de backup para armazenar seus dados em um local seguro:
  * O IBM Cloud Backup é um sistema de backup automatizado e baseado em agente. O
IBM Cloud Backup é uma solução "set-and-forget" para gerenciar seu dispositivo. Ele é
compatível com o software Microsoft, como Exchange e SQL, por meio de plug-ins extras. Os
usuários do IBM Cloud Backup interagem com esse serviço por meio do aplicativo WebCC
baseado na web do IBM Cloud Backup.
  * O R1Soft Continuous Data Protection (CDP) pode ser instalado em seu servidor ou na máquina virtual autogerenciada. Ele é recomendado se você está procurando uma única interface para gerenciar todos os seus backups. Você interage com o R1Soft CDP por meio de seu sistema de gerenciamento proprietário, que
permite que os agentes sejam instalados em máquinas virtuais e oferece plug-ins de banco
de dados para funcionalidade extra.
