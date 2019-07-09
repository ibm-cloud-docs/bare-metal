---

copyright:
  years: 2014, 2019
lastupdated: "2019-06-18"

keywords: manage bare metal port control

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Gerenciando o Controle de Porta para um Dispositivo
{: #bm-manage-port-control}

Cada dispositivo associado a uma conta possui duas portas de rede que recebem tráfego de entrada: uma para o tráfego de
rede pública e uma para o tráfego de rede privada. É possível ativar ou desativar essas portas a qualquer momento para controlar o
tráfego de rede que um dispositivo recebe. Conclua as etapas a seguir para atualizar as configurações de controle de porta para um dispositivo.

## Antes de Come╬ar
* Navegue para o menu de dispositivos do console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/bare-metal?topic=virtual-servers-navigating-devices).
* Assegure-se de que você tenha as permissões de conta e o acesso ao dispositivo necessários. Somente o proprietário da conta ou um usuário com a permissão de infraestrutura clássica **Gerenciar usuários** pode ajustar as permissões.

Para obter mais informações sobre as permissões, consulte [Permissões de infraestrutura clássica](/docs/iam?topic=iam-infrapermission#infrapermission) e [Gerenciando o acesso ao dispositivo](/docs/bare-metal?topic=virtual-servers-managing-device-access).

## Gerencie o controle de porta para um dispositivo

1. Acesse a **Lista de dispositivos** e selecione o
**Nome do dispositivo** a ser atualizado.  
2. Clique na lista suspensa **Ações** para o dispositivo.
3. Selecione  ** Controle de Porta **.
4. Atualize as caixas suspensas *Rede pública* e/ou *Rede privada* concluindo uma das seguintes
ações:
   * Selecione a velocidade desejada para ativar o acesso à rede.
   * Selecione Desconectado para desativar o acesso à rede.
5. Clique no botão Atualizar.
6. Clique no botão Fechar para fechar a janela.

## Próximas Etapas

Se você selecionou **Desativado**, o acesso à rede para a porta desativada cessará para a interface do
dispositivo. Se você selecionou **Ativado**, o acesso à rede estará disponível para a porta ativada. O controle
de porta permanece na configuração selecionada até que seja mudado manualmente.
