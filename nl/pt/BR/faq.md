---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-16"

keywords: bare metal, faq, {{site.data.keyword.cloud}}

subcollection: bare-metal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# FAQs: servidores bare metal
{: #bm-faq}

## O que é modo de inicialização UEFI?
{: faq}
O Unified Extensible Firmware Interface (UEFI) é uma especificação para a interface de software entre um sistema operacional e firmware.

O suporte do IBM Cloud para o modo de inicialização do BIOS está sendo descontinuado em favor do UEFI.

Para obter mais informações sobre o UEFI, consulte a documentação do fabricante do hardware ou acesse [https://uefi.org/](https://uefi.org/)

## Por que o meu BIOS está solicitando uma senha?
{: faq}

Atualmente, o {{site.data.keyword.cloud}} não fornece acesso direto ao BIOS por uma série de motivos. No entanto, é possível alterar o BIOS. Se você precisar que algo seja modificado no BIOS, incluindo a ordem de inicialização, crie um chamado em Suporte > Incluir chamado por meio do [{{site.data.keyword.slportal}}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/){: new_window} e solicite as mudanças específicas necessárias.

\*\*NOTA\*\* Isso requer a reinicialização do servidor, portanto, esteja pronto para aprovar uma reinicialização e/ou forneça um prazo para quando desejar que a mudança seja feita.

## Você fornece recarregamentos complementares do OS?
{: faq}

Os recarregamentos automatizados do S.O. são livres e podem ser executados por meio do [{{site.data.keyword.slportal}}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/){: new_window}. Eles incluem os recarregamentos customizados do S.O. (mudança de sistemas operacionais, adição/remoção de painéis de controle/edição de partição e assim por diante).  Para obter mais informações sobre como executar um Recarregamento do S.O., consulte o
[Procedimento de recarregamento de S.O.](/docs/infrastructure/software?topic=software-reloading-the-os).


## A unidade primária no meu servidor bare metal aparece como /dev/sdb. O que está errado?
{: faq}

Isso pode ser causado pelo disco virtual do IPMI que está assumindo o slot /dev/sda. É possível ser desativado com segurança conectando-se ao IPMIView e navegando até a guia Mídia virtual. Selecione **Opções> Desativar** e clique no botão **Aplicar** para fazer a mudança. Quando os {{site.data.keyword.baremetal_short}} forem reinicializados em seguida, a unidade primária exibirá /dev/sda.


## Por que a velocidade da CPU está errada?
{: faq}

Se você efetuar login em um servidor para verificar as informações da CPU e observar que a velocidade dos processadores estava incorreta. Essa discrepância pode ser devido a Enhanced Intel SpeedStep Technology (EIST). EIST é o nome Intel para a tecnologia de ajuste de escala de frequência dinâmica.  Essa tecnologia também é chamada de *regulagem de CPU* ou *giro de barramento* em sistemas mais velhos.  Alguns sistemas AMD possuem tecnologias semelhantes que são chamadas de *Cool'N'Quiet* ou *PowerNow!*.  Embora essas tecnologias não sejam todas iguais, elas têm o mesmo objetivo, que é reduzir o consumo de energia e a produção de calor quando o processador não está sob uso pesado, reduzindo a velocidade da CPU.  Quando o servidor estiver de volta sob carga, ele aumentará a velocidade do clock conforme necessário.

Se desejar saber se o processador Intel do servidor suporta o SpeedStep, use esse procedimento do portal do cliente:
1. Clique em **Dispositivos**.
* Identifique o seu servidor na lista.
* Clique no nome do servidor para visualizar **Detalhes do dispositivo**.
* Localize a subseção intitulada **Hardware** para localizar o número do modelo de sua velocidade de CPU de processadores do servidor.
* Com o número do modelo do processador do servidor, acesse o [Intel Processor Finder ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://processorfinder.intel.com/){: new_window} e use esse número para localizar mais informações sobre o processador e se ele suporta o Enhanced Intel SpeedStep Technology.

EIST é uma tecnologia estabelecida. Não é comum precisar desligar o EIST. No entanto, se você decidir que não deseja usar esse recurso, abra um chamado com a Equipe de suporte para desativar esse recurso.  Para desativar esse recurso, o servidor é reinicializado.


## E se o firmware do Bare Metal Server estiver desatualizado?
{: faq}

É importante manter o firmware atualizado para garantir que seu servidor bare metal tenha a compatibilidade e a estabilidade ideais do dispositivo. Se uma versão de firmware do {{site.data.keyword.baremetal_short}} estiver desatualizada, o firmware poderá ser atualizado selecionando o servidor bare metal na lista de dispositivos e selecionando **Atualizar firmware** no menu de ação.

É possível inicializar uma atualização de firmware durante o processo de [Recarregamento do S.O.](/docs/infrastructure/software?topic=software-reloading-the-os) dentro do [{{site.data.keyword.slportal}}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/){: new_window}.

## O que acontece com as unidades em Bare Metal Servers quando um cliente as conclui?
{: faq}

Após o cancelamento, um servidor é movido automaticamente para uma VLAN de recuperação por um tempo de espera configurado. Depois de concluído, os processos de recuperação iniciam e a unidade é limpa usando os algoritmos DOD 5220.22-M.  A recuperação é controlada usando o número de série na unidade. Após a conclusão, o servidor é movido para o fornecimento para redesignação. Um mau funcionamento de unidade requer intervenção manual e as unidades são configuradas para o término de vida.

O processo de término de vida é iniciado quando ocorre mau funcionamento ou a idade ou o tamanho está além do suporte. Assim que qualquer uma dessas condições ocorre, as unidades são limpas, conforme descrito anteriormente. Após a conclusão do processo de limpeza, a unidade é fisicamente destruída por quebra, esmagamento ou trituração do dispositivo.  O processo de destruição física é controlado usando o número de série da unidade.

## Posso ver quais servidores bare metal estão disponíveis para compra?
{: faq}

Sim! Agora é possível ver quais servidores estão disponíveis em qual centro de dados quando você provisiona um servidor bare metal. Mas essa opção está disponível somente para a oferta horária. Não é possível ver a disponibilidade do servidor com a oferta mensal. Para obter mais informações sobre o fornecimento de um servidor bare metal, consulte [Selecionando entre servidores de fornecimento rápido](/docs/bare-metal?topic=bare-metal-bm-select-popular-servers#bm-select-popular-servers).

## O que está incluído no meu servidor bare metal reservado?
{: faq}

CPU, RAM, unidade de disco e RAID estão incluídos na reserva pelo prazo contratado. Se você precisar de largura de banda de rede mais alta, maior capacidade de armazenamento, sistema operacional e software de terceiros, esses complementos serão cobrados mensalmente.

## O que acontece no término do meu contrato de servidor bare metal reservado?
{: faq}

Seu serviço de nuvem continua em um período de serviço mensal no preço em vigor na expiração do seu contrato.
