---

copyright:
  years: 2014, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Perguntas mais frequentes: servidores bare metal

## Por que o meu BIOS está solicitando uma senha?

Atualmente, o {{site.data.keyword.cloud}} não fornece acesso direto ao BIOS por uma série de motivos. No entanto, é possível alterar o BIOS. 
Se algo precisar ser modificado no BIOS, incluindo a ordem de inicialização, crie um chamado em Suporte > Incluir chamado por
meio do [Portal do cliente](https://control.softlayer.com/) e solicite as mudanças específicas necessárias.

\*\*NOTA\*\* Isso requer a reinicialização do servidor, portanto, esteja pronto para aprovar uma
reinicialização e/ou forneça um prazo para quando desejar que a mudança seja feita.

## Você fornece recarregamentos complementares do OS?

Os recarregamentos automatizados do OS são grátis e podem ser executados por meio do [Portal do Cliente](https://control.softlayer.com/). Eles incluem os recarregamentos customizados do S.O. (mudança de sistemas operacionais, adição/remoção de painéis de controle/edição de partição e assim por diante).  
Para obter mais informações sobre como executar um Recarregamento do S.O., consulte o
[Procedimento de recarregamento de S.O.](../vsi/vsi_perform_os_reload.html).


## A unidade primária no meu servidor bare metal aparece como /dev/sdb. O que está errado?

Isso pode ser causado pelo disco virtual do IPMI que está assumindo o slot /dev/sda. É possível ser desativado com
segurança conectando-se ao IPMIView e navegando até a guia Mídia virtual. Selecione **Opções> Desativar** e clique no botão **Aplicar** para fazer a mudança. Quando os {{site.data.keyword.baremetal_short}} forem reinicializados em seguida, a unidade primária exibirá /dev/sda.


## Por que a velocidade da CPU está errada?

Se você efetuar login em um servidor para verificar as informações da CPU e observar que a velocidade dos processadores estava incorreta. Essa discrepância pode ser devido a Enhanced Intel SpeedStep Technology (EIST). EIST é o nome Intel para a tecnologia de ajuste de escala de frequência dinâmica.  Essa tecnologia também é chamada de *regulagem de CPU* ou *giro de barramento* em sistemas mais velhos.  
Alguns sistemas AMD possuem tecnologias semelhantes que são chamadas de *Cool'N'Quiet* ou *PowerNow!*. 
Embora essas tecnologias não sejam todas iguais, elas têm o mesmo objetivo, que é reduzir o consumo de energia e a produção de
calor quando o processador não está sob uso pesado, reduzindo a velocidade da CPU. Quando o servidor estiver de volta sob carga, ele aumentará a velocidade do clock conforme necessário.

Se desejar saber se o processador Intel do servidor suporta o SpeedStep, use esse procedimento do portal do cliente:
1. Clique em **Dispositivos**.
* Identifique o seu servidor na lista.
* Clique no nome do servidor para visualizar **Detalhes do dispositivo**.
* Localize a subseção intitulada **Hardware** para localizar o número do modelo de sua velocidade de CPU de processadores do servidor.
* Com o número do modelo do processador do servidor, acesse o [Intel Processor Finder](http://processorfinder.intel.com/) e use este número para localizar mais informações sobre o processador e se ele suporta Enhanced Intel SpeedStep Technology.

EIST é uma tecnologia estabelecida. Não é comum precisar desligar o EIST. No entanto, se você decidir que não deseja usar esse recurso, abra um chamado com a Equipe de suporte para desativar esse recurso.  
Para desativar esse recurso, o servidor é reinicializado.


## E se o firmware do Bare Metal Server estiver desatualizado?

Como atualizações de software, é importante manter o firmware atualizado para assegurar compatibilidade e estabilidade ideais do dispositivo. Se um firmware do {{site.data.keyword.baremetal_short}} estiver desatualizado, uma atualização de firmware poderá ser iniciada durante o processo de [Recarregamento de S.O.](../infrastructure/software/vsi_reload_os.html) dentro do [Portal do cliente](https://control.softlayer.com).

Também é possível atualizar o firmware selecionando o Bare Metal Server na lista de dispositivos e selecionando
**Atualizar firmware** no menu Ação.

## O que acontece com as unidades em Bare Metal Servers quando um cliente as conclui?

Após o cancelamento, um servidor é movido automaticamente para uma VLAN de recuperação por um tempo de espera configurado. 
Depois de concluído, os processos de recuperação iniciam e a unidade é limpa usando os algoritmos DOD 5220.22-M. A
recuperação é controlada usando o número de série na unidade. Após a conclusão, o servidor é movido para o fornecimento para redesignação. 
Um mau funcionamento de unidade requer intervenção manual e as unidades são configuradas para o término de vida.

O processo de término de vida é iniciado quando ocorre mau funcionamento ou a idade ou o tamanho está além do suporte. Assim
que qualquer uma dessas condições ocorre, as unidades são limpas, conforme descrito anteriormente. Após a conclusão do
processo de limpeza, a unidade é fisicamente destruída por quebra, esmagamento ou trituração do dispositivo. O processo de
destruição física é controlado usando o número de série da unidade.
