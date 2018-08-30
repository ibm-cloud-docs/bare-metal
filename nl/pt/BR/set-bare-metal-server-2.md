---

copyright:

  years: 2017, 2018
lastupdated: "2018-04-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Configurando um Bare Metal Server
{: #customerportal_setupbaremetal}

É possível configurar um Bare Metal Server como um servidor dedicado.
{:shortdesc}

Use as etapas a seguir para configurar um Bare Metal Server:

1. Efetue login no portal do cliente do {{site.data.keyword.BluSoftlayer_full}} com suas credenciais exclusivas.

2. No menu, clique em **Dispositivos** > **Lista de dispositivos** e localize seu sistema. Todos os seus dispositivos são detalhados na Lista de dispositivos, na qual é possível gerenciar e atualizar dispositivos ou gerar gráficos de uso da largura da banda.

3. Escolha para gerenciar seu servidor de uma das maneiras a seguir:
  * Clique na seta ao lado do Nome do Dispositivo para visualizar um resumo e gerencie seus dispositivos por meio da visualização Captura instantânea.
  * Clique no Nome do Dispositivo do servidor para visualizar uma lista detalhada e gerencie seus dispositivos por meio da tela Detalhes do dispositivo.

4. Registre o endereço IP e as credenciais para o servidor em um local seguro para que você possa acessar os detalhes rapidamente sem precisar efetuar login no Portal do Cliente toda vez que precisar deles. É possível registrar esses detalhes para um dispositivo individual e para todos os dispositivos associados à sua conta:
  * Visualizar IPs de dispositivo individual da Lista de dispositivos.
  * Visualizar senhas raiz de dispositivo individual na Visualização de captura instantânea para o dispositivo.
  * Visualizar múltiplos IPs de dispositivo usando a opção **Fazer download do CSV** da **Lista de dispositivos**. Em seguida, selecione **Fazer download do CSV** na engrenagem **Configurações** para fazer download de uma lista completa de dispositivos e detalhes no formato de planilha.

5. Atualize as credenciais para sistemas operacionais e outro software. Todo o software que foi carregado em seu dispositivo durante o processo de fornecimento foi designado a credenciais temporárias. É possível visualizar e gerenciar essas credenciais na guia Senhas de cada dispositivo no Portal do Cliente. Use essas credenciais temporárias para acessar seu software pela primeira vez e, em seguida, mude a senha para seu software usando uma senha forte que seja composta por uma combinação de letras, números e símbolos. Opcionalmente, é possível armazenar atualizações de senha na guia Senhas para cada dispositivo; no entanto, quando você armazena senhas no portal do cliente, qualquer pessoa com acesso à conta e permissões apropriadas pode visualizar as senhas que são armazenadas na tela Senhas.

6. Acesse seu servidor na rede privada. É possível usar a rede privada da infraestrutura do {{site.data.keyword.BluSoftlayer_notm}} para interagir com seus dispositivos por meio da área de trabalho remota (RDP) usando SSH e KVM sobre IP. É possível usar a ferramenta de Acesso à VPN para conexão de rede privada ao terminal da VPN SSL mais próximo ou ao terminal de sua escolha. O acesso à VPN também é necessário para interagir com vários serviços. Para acessar a rede privada, edite o acesso à VPN do usuário na Lista de usuários. Para acessar a Lista de usuários, clique em **Conta** > **Usuários** > **Lista de usuários**. Use a página [Rede Privada Virtual ![Ícone de link externo](../icons/launch-glyph.svg)](https://www.softlayer.com/VPN-Access){:new_window} para conectar-se a uma das várias opções de VPN.

7. Configure o monitoramento para verificar o status de seu servidor e saber quando escalar. É possível usar o monitoramento padrão ou serviços de monitoramento Nimsoft. É possível usar monitoramento padrão, ou básico, no método executar ping e responder usando um ping lento ou de serviço do portal do cliente. Também é possível usar monitoramento Nimsoft, ou avançado, do portal do cliente ou em uma das três camadas: básico, avançado e premium.

8. Proteja seu sistema. Use os firewalls de hardware disponíveis para assegurar que seu dispositivo esteja seguro em todos os momentos. É possível provisionar firewalls de hardware sob demanda sem tempo de inatividade, se as regras estiverem estabelecidas corretamente, para proteger seu servidor contra atividade indesejada. Depois de pedir o firewall, ele deve ser ativado e as regras devem ser configuradas.

9. Planeje backups para assegurar que seus dados sejam armazenados com segurança fora de seu dispositivo e para ser capaz de recarregá-los se forem perdidos. É possível escolher entre uma variedade de serviços de backup para armazenar seus dados em um local seguro:
  * EVault Backup é um sistema de backup automatizado baseado em agente. Essa é uma solução "configurar e esquecer" popular para gerenciar seu dispositivo. Ela é compatível com o software Microsoft, incluindo Exchange e SQL por meio de plug-ins adicionais. Os usuários do EVault interagem com esse serviço por meio do aplicativo baseado na web WebCC do EVault.
  * O R1Soft Continuous Data Protection (CDP) pode ser instalado em seu servidor ou na máquina virtual autogerenciada. Ele é recomendado se você está procurando uma única interface para gerenciar todos os seus backups. Você interage com o R1Soft CDP por meio de seu sistema de gerenciamento proprietário, que permite que os agentes sejam instalados em máquinas virtuais e oferece plug-ins de banco de dados para funcionalidade adicional.
