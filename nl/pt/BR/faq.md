---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-05"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# FAQs: servidores bare metal

## Por que o meu BIOS está solicitando uma senha?

Atualmente, o {{site.data.keyword.cloud}} não fornece acesso direto ao BIOS. Isso ocorre por vários motivos, mas isso não quer dizer que você não possa fazer mudanças no BIOS. Se precisar modificar alguma coisa no BIOS, incluindo a ordem de inicialização, crie um chamado sob Suporte > Incluir chamado por meio do [Portal do cliente](control.softlayer.com) e solicite as mudanças específicas que você precisa.

\*\*NOTA\*\* Isso irá requerer uma reinicialização do seu servidor, portanto esteja pronto para aprovar uma reinicialização e/ou fornecer um prazo de quando gostaria que a mudança fosse feita.

## Você fornece recarregamentos complementares do OS?

Os recarregamentos automatizados do OS são grátis e podem ser executados por meio do [Portal do Cliente](control.softlayer.com). Eles incluem os recarregamentos customizados do S.O. (mudança de sistemas operacionais, adição/remoção de painéis de controle/edição de partição e assim por diante). Para obter informações detalhadas sobre como executar um Recarregamento de OS, consulte o [Procedimento de Recarregamento de OS](../vsi/vsi_perform_os_reload.html).


## A unidade primária no meu servidor bare metal aparece como /dev/sdb. O que está errado?

Isso pode ser causado pelo Disco virtual do IPMI ocupar o slot /dev/sda. Isso pode ser desativado com segurança conectando ao IPMIView e navegando até a guia Mídia virtual. Selecione **Opções> Desativar** e clique no botão **Aplicar** para fazer a mudança. Quando os {{site.data.keyword.baremetal_short}} forem reinicializados em seguida, a unidade primária exibirá /dev/sda.


## Por que a velocidade da CPU está errada?

Se você efetuar login em um servidor para verificar as informações da CPU e observar que a velocidade dos processadores estava incorreta. Essa discrepância pode ser devido a Enhanced Intel SpeedStep Technology (EIST). EIST é o nome Intel para a tecnologia de ajuste de escala de frequência dinâmica.  Essa tecnologia também é chamada de *regulagem de CPU* ou *giro de barramento* em sistemas mais velhos.  Em alguns sistemas AMD, existem tecnologias semelhantes que são chamadas *Cool'N'Quiet* ou *PowerNow!*.  Embora estas tecnologias não sejam todas iguais, elas têm o mesmo objetivo, que é reduzir o consumo de energia e de produção de calor quando o processador não estiver sob uso pesado reduzindo a velocidade de CPU.  Quando o servidor estiver de volta sob carga, ele aumentará a velocidade do clock conforme necessário.

Se você gostaria de saber se o processador Intel em seu servidor suporta SpeedStep, portal do cliente: 
1. Clique em **Dispositivos**.
* Identifique o seu servidor na lista.
* Clique no nome do servidor para visualizar **Detalhes do dispositivo**.
* Localize a subseção intitulada **Hardware** para localizar o número do modelo de sua velocidade de CPU de processadores do servidor.
* Com o número do modelo do processador do servidor, acesse o [Intel Processor Finder](http://processorfinder.intel.com/) e use este número para localizar mais informações sobre o processador e se ele suporta Enhanced Intel SpeedStep Technology.

EIST é uma tecnologia estabelecida. Você não deve ter um motivo para desligar EIST. No entanto, se você decidir que não deseja usar esse recurso, abra um chamado com a Equipe de suporte para desativar esse recurso.  Para desativar esse recurso, o servidor será reinicializado.


## E se o meu servidor bare metal tiver firmware desatualizado?

Como atualizações de software, é importante manter o firmware atualizado para assegurar compatibilidade e estabilidade ideais do dispositivo. Se um firmware do {{site.data.keyword.baremetal_short}} estiver desatualizado, uma atualização de firmware poderá ser iniciada durante o processo de [Recarregamento de S.O.](../infrastructure/software/vsi_reload_os.html) dentro do [Portal do cliente](https://control.softlayer.com).

Também é possível atualizar o firmware selecionando o servidor bare metal na lista de dispositivos e selecionando **Atualizar firmware** no menu suspenso de ação.
